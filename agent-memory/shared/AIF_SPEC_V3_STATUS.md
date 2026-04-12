# AIF_SPEC_v1.0 對照表 v3
**階段驗收結果 — 2026-04-09 05:52 UTC**

---

## MVP 成立

| 章節 | 已有能力 | 關鍵 commit |
|------|---------|------------|
| §5 記憶系統 | github_memory_rw（讀/寫/追加/搜尋）| `3fb4164`, `a70ee01` |
| §5.3 反思 | reflection_writer skill（Minimax + fallback）| `6f5b612` |
| §7 獎懲機制 | reward_evaluator（等級判定 + 行動建議）| `58f6663` |
| §8 做夢探索 | dream_explorer skill（靈感提案）| `0c2e35b` |
| §8.3 好奇心系統 | curiosity_contributor（3 agents 真實寫入）| `80e086e` |
| §10 提案流程 | roundtable_proposer + decision_recorder → TEAM_DECISIONS | `516c8d4`, `492afd3`, `a963f97` |
| §11 健康報告 | health_reporter skill | `c3a53b2` |
| §13 Hook 整合 | task_complete_hook（自動串接 WINS/STATUS/MEMORY）| `af08509` + `51d8c3b`, `699ced3` |
| §14 Pipeline | reddit_scraper / writer / qa / publisher | 多筆 |

---

## 部分落地（有骨架，需深化）

| 章節 | 已有能力 | 下一步缺口 |
|------|---------|----------|
| §3.3 狀態機 | writer/qa/publisher STATUS.md 五態定義 | 自動化狀態更新、擴展至全 13 agent |
| §6.4 週報 | weekly_ops_report + send_weekly_ops_report.js | 自動 cron 排程（已具備手動觸發送達老闆能力）|
| §12/§16 收入追蹤 | revenue_tracker skill 骨架完成，WHOP_API_KEY 權限阻塞 | 需 Whop Merchant API Key 才能讀真實收入 |
| §18 Telegram | telegram_notifier（3 種格式）| 自然語言對話式互動 |

---

## 未落地（還沒開始）

| 章節 | 缺什麼 |
|------|--------|
| §9 SEO | 無關鍵字分析 / 搜尋優化 skill |
| §15 Whop 商業 | WHOP_BUSINESS_LOGIC.md 存在但未自動化 |
| §17 Secretary | 無議程整理 / 會議記錄 skill |
| §3.4 FREE 行為 | FREE 狀態無實質行動定義 |

---

## 下一階段優先順序

1. **§12 收入追蹤**：老闆提供 Whop Merchant API Key → 真實 revenue pull
2. **§3.3 狀態機自動化**：STATUS.md 更新接入 task_complete_hook
3. **§7 獎懲落地**：reward_evaluator 結果寫入 BEST_PRACTICES / 觸發 counselor
4. **§6.4 cron 排程**：weekly_ops_report 自動每週執行
5. **§8.3 深化**：dream_explorer 從 CURIOSITY_POOL 讀取並生成靈感提案

---

## 開發原則（自 2026-04-09 起生效）

1. 後續開發一律以本表優先順序為準
2. 不要隨意跳去做未排序的新功能
3. 每完成一項，更新一次對照表版本
4. 所有回報以 GitHub 可驗證內容為準

---

_本檔案為 AIF 團隊內部共識文件，由小錢維護_
