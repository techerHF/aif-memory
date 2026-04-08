# TEAM_DECISIONS.md — aif-factory 團隊決策記錄

> 本文件記錄影響整個 aif-factory 系統的重大決策。
> 每條決策必須包含：決策內容、決策理由、決策者、生效日期。
> 最後更新：2026-04-07

---

## [TD-001] 模型選擇：Minimax 主力 + Gemma 備用

**決策日期**：2026-04-07
**決策者**：系統初始化（Manager 確認）
**狀態**：生效中

**決策內容**：
- **Minimax**（MiniMax-M2.7）作為主力模型，用於 Manager（協調決策）和 Writer（內容生成）
- **Gemma**（google/gemma-4-31B-it）用於 Researcher（市場掃描）、QA（品質審核）、Publisher（發佈管理）
- Minimax 為全系統的 fallback 首選，Gemma 為備用

**決策理由**：
- Minimax 在中文內容生成和邏輯推理上表現優秀，適合創意和決策類任務
- Gemma 成本效益高，適合結構化分析和執行類任務（掃描、審核、發佈）
- 兩個 provider 的 rate limit 特性互補（Minimax 5小時窗口 / Gemma 每日重置），可以平衡負載

**限制條件**：
- Minimax: 1500 次 / 5 小時
- Gemma: 1500 次 / 天（google/gemma-4-31B-it）

---

## [TD-002] Pipeline 順序：Researcher → Manager → Writer → QA → Publisher

**決策日期**：2026-04-07
**決策者**：Manager
**狀態**：生效中

**決策內容**：
任務處理流水線固定為：
1. **Researcher**：發現任務候選
2. **Manager**：評估、選擇、分配任務
3. **Writer**：執行內容生成
4. **QA**：品質審核（可退件回 Writer）
5. **Publisher**：最終交付

**決策理由**：
- 此順序確保每個任務在進入下一階段前都經過明確的閘門（gate）
- Manager 在 Researcher 和 Writer 之間作為「需求翻譯」，防止規格失真
- QA 在 Publisher 之前，確保零缺陷交付

**例外情況**：
- 緊急任務可由 Manager 直接指定 Writer，跳過 Researcher 環節
- 簡單重複任務（已有模板）可由 Manager 降低 QA 標準（最低分數線下調至 70）

---

## [TD-003] QA 通過門檻：80分

**決策日期**：2026-04-07
**決策者**：Manager + QA
**狀態**：生效中

**決策內容**：
- 總分 >= 80 分：通過，進入 Publisher
- 總分 < 80 分 或 任何單項 < 12 分：退件，回到 Writer 修正
- 最多允許退件 2 次；第 3 次退件升級至 Manager 決定是否放棄任務

**決策理由**：
- 80 分保證了「高於平均但不要求完美」的品質標準
- 允許 2 次修正機會，平衡品質和效率
- 第 3 次退件說明存在系統性問題，需要人工介入

---

## [TD-004] 閉環分數門檻：0.75

**決策日期**：2026-04-07
**決策者**：Manager + Researcher
**狀態**：生效中

**決策內容**：
Researcher 只推薦閉環分數 >= 0.75 的任務候選。

**決策理由**：
- 0.75 過濾掉需求模糊或技術不可行的任務
- 低於此門檻的任務平均退件率超過 60%，浪費 Writer 和 QA 資源
- 寧可掃描更多任務找到高品質候選，也不接低品質任務

---

## [TD-005] API Fallback 策略

**決策日期**：2026-04-07
**決策者**：Manager
**狀態**：生效中

**決策內容**：
- 主 provider 失敗（超時、rate limit、錯誤）時，自動切換到 fallback provider
- Fallback 鏈：`["minimax", "gemma"]`
- 切換時在 MEMORY.md 記錄切換原因和時間
- 若所有 provider 都不可用，暫停任務並等待 provider 恢復，不強制執行

**決策理由**：
- 單點故障保護
- 確保系統在高負載下的連續性

---

## [TD-006] 記憶體架構：個人記憶 + 共享記憶

**決策日期**：2026-04-07
**決策者**：全體 Agent
**狀態**：生效中

**決策內容**：
- 每個 Agent 有 4 個私有記憶檔案：SOUL.md / MEMORY.md / WINS.md / MISTAKES.md
- 共享記憶位於 `agent-memory/shared/`：BEST_PRACTICES.md / TEAM_DECISIONS.md
- 任何 Agent 都可以讀取共享記憶，但只有 Manager 可以確認寫入 TEAM_DECISIONS.md

**決策理由**：
- 私有記憶保留 Agent 的個性和專業學習
- 共享記憶確保團隊知識不因個別 Agent 重置而消失
- Manager 作為共享記憶的守門人，確保決策一致性
