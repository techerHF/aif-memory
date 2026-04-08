# MEMORY.md — 記憶管理員操作記憶

> 記錄記憶管理行為、GitHub 同步狀態、記憶異常等。

---

## 初始化狀態
**初始化時間**：2026-04-08
**工廠生日**：2026-04-08（與老闆同一天 🎂）
**狀態**：正式上線

---

## 系統架構

### 記憶層次結構
```
Level 1：瞬時記憶（Context Window）
 → 當前任務的工作記憶

Level 2：短期記憶（記憶管理員日誌）
 → 當天的記憶同步記錄

Level 3：長期記憶（GitHub: techerHF/aif-memory）
 → MEMORY.md / WINS.md / MISTAKES.md，永久保存

Level 4：集體記憶（shared/ 目錄）
 → BEST_PRACTICES.md / TEAM_DECISIONS.md，全員共享
```

### 倉庫結構
```
techerHF/aif-memory/
 ├── agent-memory/
 │   ├── memory/        ← 記憶管理員
 │   ├── manager/       ← 經理
 │   ├── secretary/     ← 秘書
 │   ├── researcher/
 │   ├── writer/
 │   ├── seo/
 │   ├── publisher/
 │   ├── sales/
 │   ├── qa/
 │   ├── explorer/
 │   ├── cfo/
 │   └── counselor/
 │   └── dreamer/
 └── shared/
     ├── BEST_PRACTICES.md
     ├── TEAM_DECISIONS.md
     └── CURIOSITY_LOG.md
```

---

## GitHub 同步記錄

| 日期 | 時間 | 操作 | 狀態 |
|------|------|------|------|
| 2026-04-08 | — | 初始化建立 | ✅ |

---

## 記憶同步排程

- **每任務完成後**：自動同步該 Agent 的記憶到 GitHub
- **每天 00:00 UTC**：全量記憶備份
- **每週一**：記憶整理（壓縮、歸檔）
- **每次系統重啟後**：驗證記憶完整性

---

## 已知 Agent 清單

| Agent ID | 名稱 | 狀態 | 最後同步 |
|----------|------|------|----------|
| memory | 記憶管理員 | 上線 | — |
| manager | 經理 | 待建立 | — |
| secretary | 秘書 | 待建立 | — |
| researcher | 研究員 | 待建立 | — |
| writer | 寫手 | 待建立 | — |
| seo | SEO分析師 | 待建立 | — |
| publisher | 發佈員 | 待建立 | — |
| sales | 銷售員 | 待建立 | — |
| qa | 品質管控 | 待建立 | — |
| explorer | GitHub探索員 | 待建立 | — |
| cfo | 財務員 | 待建立 | — |
| counselor | 心理諮商師 | 待建立 | — |
| dreamer | 做夢員 | 待建立 | — |

---

## 待辦
- [x] 建立記憶管理員 workspace
- [ ] 設定 GitHub 連線驗證
- [ ] 建立 shared/ 目錄結構
- [ ] 等待其他 Agent 上線後，建立他們的初始記憶檔案
- [ ] 設定每日自動同步排程
