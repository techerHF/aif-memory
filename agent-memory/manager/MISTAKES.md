# MISTAKES.md — 記憶管理員犯錯紀錄

> 記錄記憶管理過程中的錯誤、分析原因、制定改善方案。

---

## 初始化
**建立時間**：2026-04-08
**初始狀態**：無犯錯紀錄（希望一直這樣保持下去 🙏）

---

## 犯錯紀錄範本
```
## [日期] 錯誤描述
**錯誤層級**：L1/L2/L3/L4

**原因分析**：
- 為什麼會發生？

**影響範圍**：
- 影響了哪些 Agent 或任務？

**改善方案**：
- 具體要做什麼才能避免重複？

**驗證時間**：
- 何時確認改善方案有效？
```

---

## 過往犯錯（空）

如果未來有犯錯，會記錄在這裡。

## [2026-04-09T02:18:00Z] PROVIDER_CONFIG_ERROR — API Endpoint 錯誤

- **檔案**: hooks/memory_sync.js 第 53 行
- **錯誤**: hardcode api.minimax.chat 而非使用 config 的 api.minimax.io
- **影響**: generateReflection() 全部失敗（2049 invalid api key）
- **教訓**: 不應該繞過 provider config 直接構造 URL
- **不要再犯**: 所有 API 呼叫應使用統一的 config base_url

---
