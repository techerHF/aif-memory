# MEMORY_GOVERNANCE_V1.md — 記憶治理規範

> 本文件是 AIF v4 Phase 1.5 的核心產出。
> 所有 agent 必須遵守本規範，以避免記憶錯亂與架構漂移。

---

## 一、記憶分層規則

### 第 1 層：個人記憶（各 agent 私有）

| 檔案 | 用途 |
|------|------|
| `MEMORY.md` | 該 agent 的個人工作記憶、上下文、已完成事項 |
| `WINS.md` | 成功案例與有效方法 |
| `MISTAKES.md` | 失敗案例與教訓 |
| `FREE_THOUGHTS.md` | 探索性想法、猜測、不確定的觀察 |
| `STATUS.md` | 當前狀態（IDLE/BUSY/REVIEW）|
| `SKILLS_LOG.md` | 使用過的 skill 與執行結果 |

**規則：** 個人記憶只有該 agent 可以寫。

### 第 2 層：Shared 記憶（團隊共享）

| 檔案 | 用途 | 寫入權限 |
|------|------|---------|
| `TEAM_DECISIONS.md` | 重大團隊決策 | manager / secretary |
| `BEST_PRACTICES.md` | 成功案例與最佳實踐 | reward_evaluator（自動）|
| `CURIOSITY_POOL.md` | 好奇心觀察 | 所有 agent |
| `ACTION_ITEMS.md` | 待確認事項 | secretary |
| `FREE_BEHAVIOR.md` | FREE agent 行為邊界 | manager |
| `MEMORY_GOVERNANCE_V1.md` | 本規範 | main（小錢）|

**規則：** Shared 記憶任何人可讀，但寫入須符合下方「寫入責任規則」。

### 第 3 層：系統規範（最高權威）

| 檔案 | 優先順序 | 維護者 |
|------|---------|--------|
| `AIF_SPEC_V4_STATUS.md` | 最高 | main（小錢）|
| `Phase 1 Completion Report` | 次高 | main（小錢）|
| `MEMORY_GOVERNANCE_V1.md` | 第三 | main（小錢）|

---

## 二、寫入責任規則

### ✅ 可以直接寫入 Shared 的 agent

| Agent | 可寫入 |
|-------|--------|
| reward_evaluator | BEST_PRACTICES.md |
| secretary_brief | BRIEFINGS.md / ACTION_ITEMS.md |
| task_complete_hook | 各 agent 的 WINS/MISTAKES/STATUS |
| github_memory_rw | 任一 memory 檔（git sync 用途）|

### ⚠️ 需要提案才能寫入 Shared 的 agent

| Agent | 需提案至 |
|-------|---------|
| dreamer | CURIOSITY_POOL.md（可直接寫）|
| researcher | CURIOSITY_POOL.md |
| curiosity_contributor | CURIOSITY_POOL.md |
| 所有 FREE agent | BEST_PRACTICES.md（需通過 reward_evaluator）|

### ❌ 不得直接寫入 Shared 的 agent

- 任何 agent 不得直接修改 `TEAM_DECISIONS.md`
- 任何 agent 不得直接刪除其他 agent 的 WINS/MISTAKES
- 任何 agent 不得覆寫 AIF_SPEC 或本規範

---

## 三、衝突解決規則

### 規則 1：個人記憶 vs Shared 決策

**衝突時以 Shared 為準。**

範例：
- agent 個人 MEMORY.md 與 `TEAM_DECISIONS.md` 衝突 → 以 TEAM_DECISIONS 為準

### 規則 2：舊規範 vs 新規範

**衝突時以最新版本的 timestamp 為準。**

- AIF_SPEC v4 vs v3 → 以 v4 為準
- 本規範 vs 舊版 MEMORY_GOVERNANCE → 以 V1 為準

### 規則 3：跨 agent 對同一事實衝突

**以「被多數 agent 引用」者為準。**

若 writer 和 explorer 對同一事件記法不同：
1. 檢查 shared/BEST_PRACTICES.md 是否有記載
2. 檢查 TEAM_DECISIONS.md 是否有相關決策
3. 以較早 timestamp 為準（有更多時間沉澱）

---

## 四、規範優先順序（版本權威）

本系統的規範優先順序：

```
1. AIF_SPEC_V4_STATUS.md   ← 最高權威，架構藍圖
2. Phase 1 Completion Report ← 里程碑文件，Phase 1 終態
3. MEMORY_GOVERNANCE_V1.md  ← 記憶治理核心規範
4. TEAM_DECISIONS.md        ← 團隊決策記錄（低於 Phase 1 Report）
5. BEST_PRACTICES.md         ← 實踐積累（動態更新）
6. 各 agent MEMORY.md         ← 個人參考（最低）
```

---

## 五、Phase 1.5 完成狀態

- ✅ 13-agent 完整 7 核心檔案建立
- ✅ 記憶分層規則建立
- ✅ 寫入責任規則建立
- ✅ 衝突解決規則建立
- ✅ 規範優先順序建立

---

_由小錢建立 — AIF Phase 1.5 — 2026-04-09_
