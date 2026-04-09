# TEAM_CONTEXT.md — 專案背景

> 這是 AIF-Factory 團隊的專案背景檔案。
> 只讀 current 標記 + 最近 15 筆。
> archived 項目視為歷史參考，不影響當前判斷。
> inferred 內容僅供內部參考，不代表團隊共識。

---

## current / archive 標記

| 標記 | 意義 |
|------|------|
| current | 目前仍有效的背景資訊 |
| archived | 已過期但保留參考 |

---

## 寫入模板

```markdown
## [日期] 背景更新：[主題]

**現況：** [當前狀態]
**約束條件：** [限制]
**來源：** 群組討論 / 老闆明確指令 / 觀察推斷
**信心等級：** confirmed / inferred
**狀態：** current
**相關決策：** [連結到 TEAM_DECISIONS]
**寫入時間：** [ISO 8601]
**記錄人：** Agent-AIF

備註：inferred 僅供內部參考，不代表團隊共識。
```

---

## 現有背景

---

## [2026-04-09] 背景更新：Telegram 群組 Bot 架構變更

**現況：** 4 個 bot（@AIF_HF_BOT、@AIF_Writer_BOT、@AIF_QA_BOT、@AIF_Secretary_BOT）已成功加入同一群組。Bot 隱私模式已關閉，bot 可在群組正常接收與回應訊息。
**約束條件：** Bot 無法自動看到其他 bot 的訊息（Telegram 原生限制），需靠 Agent-AIF 後端接棒。
**來源：** 群組討論
**信心等級：** confirmed
**狀態：** current
**相關決策：** #1（共享記憶機制 v1 建立）
**寫入時間：** 2026-04-09T19:08:00Z
**記錄人：** Agent-AIF

備註：inferred 僅供內部參考，不代表團隊共識。

