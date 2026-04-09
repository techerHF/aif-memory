# §12 / §16 Whop 收入追蹤 — 權限解鎖說明

## 現狀

- revenue_tracker skill 已建立（commit `38c69a7`）
- 嘗試讀取 Whop API，結果：`401 Unauthorized`
- 原因：目前的 `WHOP_API_KEY` 是 `apik_...` 開頭的 **Affiliate Key**，只能做聯盟行銷，無法讀取商戶收入數據

## 需要老闆提供的資訊

### 選項 A：Whop Merchant API Key（推薦）

1. 登入 [Whop Dashboard](https://whop.com/dashboard)
2. 進入「開發者設定」或「API」頁面
3. 產生一組 Merchant API Key（不是 `apik_` 開頭的）
4. 將 key 設定至 `.env`：
   ```
   WHOP_API_KEY=your_merchant_api_key_here
   ```

### 選項 B：Whop Sales/Revenue API endpoint

如果 Whop 有公開的銷售數據 API，請提供：
- API endpoint URL
- 認證方式（Bearer token / API key / OAuth）
- 預期 response 格式

### 選項 C：手動收入數據（過渡方案）

如果暫時無法取得 API Key，可以：
- 每週一由老闆提供上週 Whop 收入數字
- 寫入 `agent-memory/cfo/MANUAL_REVENUE.md`
- revenue_tracker 改為讀取此檔案

## 驗證流程（key 拿到後）

1. 老闆將 key 寫入 `.env`
2. OpenClaw 執行：`node -e "require('./skills/revenue_tracker').revenue_tracker({}).then(r => console.log(r.report))"`
3. 確認 `mode: live` 且 `level` 非 `unknown`
4. 若成功， revenue_tracker 可正式接入 health_report / weekly_ops_report

---

_由小錢維護 — 2026-04-09_