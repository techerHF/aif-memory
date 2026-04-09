# MEMORY.md — Manager 操作記憶

> 此文件記錄 Manager 的操作學習和當前狀態。
> 每次任務完成後自動更新。

---

## 系統初始化狀態
**初始化時間**：2026-04-07
**版本**：v1.0.0
**狀態**：待命中（等待第一個任務）

---

## 已知的操作模式

### 任務評估流程
1. 收到 Researcher 的候選清單
2. 檢查閉環分數（必須 >= 0.75）
3. 評估當前 API 額度是否足夠完成任務
4. 選擇優先級最高的任務
5. 撰寫任務規格（含明確的完成標準）
6. 分配給 Writer

### 退件處理流程
1. 收到 QA 退件報告
2. 閱讀 `must_fix` 清單
3. 判斷是 Writer 問題還是規格問題
   - Writer 問題：直接轉發反饋給 Writer
   - 規格問題：修正規格後再發給 Writer
4. 記錄退件原因（用於後續改進）

---

## 當前 API 額度狀態
- Minimax：未追蹤（需啟動 rate-state）
- Gemma：未追蹤（需啟動 rate-state）

---

## 學到的教訓
_（初始為空，任務執行後更新）_

---

## 待辦事項
- [ ] 建立 `.rate-state/` 資料夾和初始追蹤檔案
- [ ] 設定環境變數（MINIMAX_API_KEY, GEMMA_API_KEY）
- [ ] 執行第一次 Researcher 掃描
## 任務分配 [2026-04-09T13:28:00Z] — Learning Stress Test v3 Round 1
- 來源：老闆指令
- 任務：分配「Arduino 感測器套件」產品開發統籌
- 負責人：sales（市場）+ cfo（定價）+ writer（內容）+ qa（審核）
- 優先度：高
- 備註：這是基準任務，用於衡量未來成長

## 決策更新 R2 [2026-04-09T13:50:13Z] — Learning Stress Test v3 Round 2
- R1：任務分配 Arduino 感測器套件開發
- R2：writer v2 完成（63/75），cfo 調整定價至 $29-39
- 決策：啟動 IoT 感測器三部曲下一步（dreamer 提案）
- R1→R2：從分配到追蹤+決策演化

## 決策更新 R3 [2026-04-09T13:57:11Z] — Learning Stress Test v3 Round 3
- R3 錯誤注入：writer 電路圖遺漏（danger）
- qa 發現有效 ✅ / writer 修正 < 1 分鐘 ✅
- 決策：維持現有機制，不需額外流程

## 決策更新 R4 [2026-04-09T14:02:12Z] — Learning Stress Test v3 Round 4
- BEST_PRACTICES 引用：確認 IoT 產品製作規範
- CURIOSITY_POOL 引用：IoT 感測器需求持續
- TEAM_DECISIONS 引用：TD-003 產品線確認
- 決策：啟動《IoT 感測器三部曲》產品線
- 成長亮點：從任務分配（R1）→追蹤決策（R3）→戰略規劃（R4）

## 戰略規劃 R5 [2026-04-09T14:08:12Z] — Learning Stress Test v3 Round 5
- R1-R5 成果：13 agents 全員迭代 + shared memory 100% 覆蓋
- Q2 OKR：月營收 $500 + 500 UV/月
- 資源分配：writer（內容）+ qa（標準）+ sales（變現）
- TEAM_DECISIONS 更新：Q2 戰略規劃 + OKR
- 成長亮點：從任務分配→戰略統籌

## 運營優化 R6 [2026-04-09T14:10:00Z] — Round 6
- 流程標準化：manager 核心流程已建立標準文檔
- BEST_PRACTICES 引用：持續優化

## Q2 規劃 R7 [2026-04-09T14:11:00Z] — Round 7
- manager Q2 OKR 已設定
- TEAM_DECISIONS 引用：Q2 戰略對齊

## 流程審計 R8 [2026-04-09T14:12:00Z] — Round 8
- manager 流程審計完成
- CURIOSITY_POOL 引用：持續改進

## 客戶回饋 R9 [2026-04-09T14:13:00Z] — Round 9
- manager 整合客戶回饋到流程
- BEST_PRACTICES 引用：持續改善

## Q2 啟動 R10 [2026-04-09T14:14:00Z] — Round 10
- manager Q2 正式啟動
- 目標：月營收 $500 + 500 UV/月
