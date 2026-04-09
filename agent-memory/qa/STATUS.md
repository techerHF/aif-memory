# STATUS.md — qa Agent

## 狀態追蹤（§3.3 Agent 狀態機 — 3 Agent Pilot）

## 狀態定義

| 狀態 | 意義 |
|------|------|
| BUSY | 執行審核中 |
| IDLE | 無待審核任務 |
| FREE | 自由活動（§3.4）|

## 明確轉換規則（最小可運作版）

### qa：IDLE → BUSY → IDLE

| 觸發條件 | 轉換 | 說明 |
|---------|------|------|
| 接收 quality_scorer 任務 | IDLE → BUSY | 收到文章待審 |
| 審核完成（通過或退件）| BUSY → IDLE | 結果寫入，回覆 writer |

### 審核標準（門檻 70 分）
- word_count：800-3000 字
- structure：含 frontmatter + heading + body
- tech_content：≥3 個技術術語
- no_ghost_lines：無全空行 block
- originality（Gemma 評估）：需通過

## 當前狀態

- **狀態**：IDLE
- **最後變更**：2026-04-09T03:22:00Z

## 真實轉換日誌

| 時間戳 | 舊狀態 | 新狀態 | 觸發事件 |
|--------|--------|--------|---------|
| 2026-04-09T03:22:00Z | BUSY | IDLE | 審核完成，無新任務 |
| 2026-04-09T02:06:38Z | BUSY | IDLE | reflection-test-failure-001 退件（score < 70）|
| 2026-04-09T02:00:00Z | IDLE | BUSY | 接收 quality_scorer 任務 |
| 2026-04-08T16:00:00Z | BUSY | IDLE | github_memory_rw article 審核通過（score 85）|

---

_最後更新：2026-04-09_
