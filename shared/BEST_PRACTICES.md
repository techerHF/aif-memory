# BEST_PRACTICES.md — aif-factory 團隊最佳實踐

> 本文件由全體 Agent 共同維護，記錄經過驗證的最佳工作方式。
> 更新規則：任何 Agent 發現值得推廣的做法，可提議加入；需 Manager 確認後生效。
> 最後更新：2026-04-07

---

## 1. API 使用規範

### Rate Limit 管理
- **Minimax**（1500次/5小時）：每次呼叫前必須查詢 `.rate-state/minimax.json`，確認剩餘額度
- **Gemma**（1500次/天）：高消耗任務（如長文生成）優先使用 Minimax，保留 Gemma 額度給掃描和審核
- 當任一 provider 剩餘額度 < 100 時，自動切換 fallback，並記錄到 MEMORY.md
- 不得在 rate limit 耗盡後強制重試，必須等待 window 重置

### API 呼叫最佳化
- 批次任務：能合併的請求盡量合併，減少總呼叫次數
- 快取結果：相同輸入的結果應快取，避免重複呼叫
- 超時設定：Minimax 30秒、Gemma 45秒，超時後重試最多 3 次

---

## 2. 任務交接格式標準

### Researcher → Manager
```json
{
  "scan_id": "SCAN-YYYYMMDD-001",
  "timestamp": "ISO8601",
  "candidates": [...],
  "scan_stats": {
    "platforms_scanned": 0,
    "total_found": 0,
    "passed_threshold": 0
  }
}
```

### Manager → Writer
使用 Markdown，必須包含以下章節：
- `## 任務描述`：客戶原始需求（不得修改）
- `## 交付規格`：格式、字數、語言、風格
- `## 完成標準`：QA 評分會依據此標準
- `## 截止時間`
- `## 參考資料`（可選）

### QA → Manager（退件時）
```json
{
  "task_id": "...",
  "decision": "REJECT",
  "must_fix": ["具體問題1", "具體問題2"],
  "retry_allowed": true
}
```

---

## 3. 記憶體更新規則

| 觸發條件 | 更新檔案 | 更新 Agent |
|---------|---------|-----------|
| 任務完成 | MEMORY.md、WINS.md | 執行任務的 Agent |
| 發生錯誤 | MISTAKES.md | 發生錯誤的 Agent |
| 發現新模式 | BEST_PRACTICES.md | 任何 Agent（需 Manager 確認）|
| 重大決策 | TEAM_DECISIONS.md | Manager |
| 每週 | 全部 Agent 的 MEMORY.md | 各自 Agent |

---

## 4. 錯誤處理流程

```
錯誤發生
    ↓
記錄到 MISTAKES.md（含錯誤類型、原因、時間）
    ↓
判斷是否可自動恢復？
    ├─ 是 → 執行恢復邏輯，記錄恢復結果
    └─ 否 → 通知 Manager，暫停當前任務
                ↓
            Manager 診斷並決定：重試 / 放棄 / 人工介入
```

### 常見錯誤類型與處理
- `API_RATE_LIMIT`：等待，切換 fallback provider
- `API_TIMEOUT`：重試（最多3次），記錄延遲
- `QA_REJECTION`：分析反饋，定向修正，最多重試2次
- `PLATFORM_ERROR`：記錄，通知 Manager，嘗試備用交付方式
- `PARSE_ERROR`：記錄原始輸出，請求重新生成

---

## 5. 閉環條件定義（核心共識）

一個任務被視為「閉環」必須滿足：
1. **可驗證**：完成後客戶能明確確認是否達標
2. **可交付**：輸出物是具體的檔案、文字或行動結果
3. **可計費**：有明確的報酬或等值回報
4. **時程確定**：有截止日期，我們能在期限內完成
5. **技術可行**：現有工具鏈可以執行，不依賴未知能力

閉環分數 < 0.75 的任務：Researcher 不得推薦，Manager 不得接受。
