# aif-memory

> 工廠的長期記憶系統。每個 Agent 的記憶都保存在這裡。

## 結構

```
aif-memory/
├── agent-memory/
│   ├── memory/      ← 記憶管理員
│   ├── manager/     ← 經理
│   ├── secretary/   ← 秘書
│   ├── researcher/  ← 研究員
│   ├── writer/      ← 寫手
│   ├── seo/         ← SEO 分析師
│   ├── publisher/   ← 發佈員
│   ├── sales/       ← 銷售員
│   ├── qa/          ← 品質管控
│   ├── explorer/    ← GitHub 探索員
│   ├── cfo/         ← 財務員
│   ├── counselor/   ← 心理諮商師
│   └── dreamer/     ← 做夢員
└── shared/
    ├── BEST_PRACTICES.md
    ├── TEAM_DECISIONS.md
    └── CURIOSITY_LOG.md
```

## 每個 Agent 的記憶檔案

| 檔案 | 用途 |
|------|------|
| SOUL.md | 核心價值觀與人格 |
| MEMORY.md | 操作記憶與歷史 |
| MISTAKES.md | 犯錯紀錄與改善 |
| WINS.md | 成功案例與做法 |
| SKILLS.md | 能力清單（待建）|
| OKR.md | 目標與進度（待建）|

## 同步原則

- 每次任務完成後，相關 Agent 必須更新自己的記憶
- 記憶管理員負責監督所有 Agent 的記憶同步
- 所有記憶必須同步到 GitHub，確保系統重啟後能恢復
