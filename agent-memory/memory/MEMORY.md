# MEMORY.md — 記憶管理員操作記憶

> 記錄記憶管理行為、GitHub 同步狀態、記憶異常等。

---

## Reddit 研究掃描（2026-04-08）

**資料來源**：Pushshift Reddit Archive（最後更新：約 2025-05，最大可取至 ~2024-09）
**說明**：Reddit 直接存取遭封鎖（403），使用 Pushshift 替代。資料落差不影響長期趨勢分析。

---

### 📊 r/arduino — 熱門主題與 Pain Points

**All-time 熱門專案**（依 score）：
1. 嬰兒教育書（7166票）— Arduino 應用於親子教育
2. 大學「全息投影」（6807票）— 3D 即時捕捉投影
3. Reddit 讚通知器（6672票）— LED 矩陣 + ESP8266 即時監控
4. 超音波懸浮裝置（5003票）— 60 顆超音馬達 + Arduino Nano
5. 摩托車傾角加速記錄儀（3917票）— 運動專用感測器
6. 聲波懸浮（3740票）— Arduino 控制相位移動粒子
7. BIOS 自動化設定工具（3657票）— 筆電工廠用途
8. 天氣站（3643票）— 常見 IoT 專案
9. 會大便的鳥形無人機（3273票）— 創意 Arduino 專案

**新貼文常見問題**（Pain Points）：
- Servo 馬達角度範圍對齊（與機器人機構 mismatch）
- ATtiny85 Bootloader 燒錄失敗
- 多模組供電問題（Nano + DFPlayer + Servo + NRF24 同時供電）
- ESP8266 WiFi 連線問題
- 初次使用者在 OSC 示波器與 Arduino 專案整合上的困惑
- OBD2 掃描器使用挫折（診斷工具體驗差）
- 入門者無所適從（Noobs overwhelmed by YouTube 教程）
- MOSFET 電路設計（Filament Dryer）
- Reset pin 能否用於關機
- Android 音量旋鈕（Pro Micro + Rotary Encoder）

**趨勢觀察**：
- ESP8266/ESP32 佔主導，但仍有大量 Nano/Uno 入門族群
- 多模組整合（馬達+RF+音效）是最大痛點
- IoT 資料視覺化需求旺（天氣站、遠端監控）
- 入門學習曲線仍是核心議題

---

### 📊 r/electronics — 熱門主題與 Pain Points

**All-time 熱門**（依 score）：
1. 錫球墜落 PCB（13560票）— 病毒式傳播的意外事故
2. Mixed Signals（6782票）— PCB 美學/電路藝術
3. 用膠帶揭露 IC 雷射刻印（4860票）— 實用技巧
4. 劣質錫線 + 老烙鐵頭 的完美體驗（4600票）
5. 144 顆 7 段顯示器時鐘（3688票）
6. 0.01 µH 電感（2999票）— 微型元件之美
7. 自製 CPU + 8bit 電腦（2964票）— 離散邏輯巔峰
8. 拾放機設計（2897票）— 開源硬體
9. 邏輯閘（2805票）
10. 自製智慧手表（ESP32）（2340票）— DIY 穿戴裝置

**新貼文常見問題**：
- 第一次做放大器（power amplifier）
- 太陽能板/ATX PSU 測試
- 微波爐磁控管波導結構疑問
- USB-C 連接器焊接
- 電容更換
- MOSFET 飽和區域操作
- BCI（腦機介面）設計
- 智慧眼鏡（給視障者用）

**趨勢觀察**：
- PCB 藝術/美學內容病毒傳播力強
- 自製 CPU/電腦 一直是長青熱門
- 開源硬體（Pick and Place）受關注
- DIY 智慧手表/穿戴裝置興趣增加
- 焊接技術討論（耗材品質）持續有共鳴

---

### 📊 r/maker — 熱門主題與 Pain Points

**All-time 熱門**（依 score）：
1. Adam Savage AMA（984票）— Maker 偶像級人物
2. 貓咪地毯（434票）— 創意手工
3. 筆記型電腦連接埠標籤（268票）— 實用日常改善
4. 自動多功能工具（260票）— 機構設計
5. 磁懸浮燈（256票）— 懸浮機構 + Arduino
6. 視障者用 Speak Caliper（251票）— 無障礙設計
7. 聲波懸浮（237票）— 與 r/arduino 跨社群熱門
8. 夾板電視櫃（kerf bending）（221票）— 木工技術
9. 鐵達尼號動態模型（220票）— 機構 + 控制
10. 訂製焊接站（軍事外殼）（180票）

**新貼文常見問題**（Pain Points）：
- 低成本模組化支撐系統（替代 Unistrut）
- 馬達整合（如何讓玩具可控）
- 3D 列印機構整合電子（頭髮夾/鳥/自拍棒）
- 自動烹飪機器人極難（香料分裝、精油、攪拌、溫控）
- ESP32 數位寵物（無雲端/無追蹤）
- 工作室電氣配置（230V/400V 規劃）
- 手機遊戲控制器（結合折疊手機）
- 冰箱套（液冷個人降溫）

**趨勢觀察**：
- 自動化烹飪是 maker 社群的重大挑戰/未解決問題
- 無障礙/通用設計（Universal Design）有穩定關注
- 木工 + 電子整合專案受歡迎
- 創意日常小物（ портатив 標籤、收納）有固定受眾
- 模組化系統需求（希望低成本的替代方案）

---

### 📊 r/InteractiveArt — 資料有限

**現有資料（2021年為主）**：
- 電話亭互動裝置
- PCD@Coimbra 2021 藝術徵件（anachronism 主題）
- 有限資料（僅 2 筆高分 post）

**說明**：此社群規模較小，Pushshift 存檔有限。建議直接瀏覽以獲得更完整圖像。

---

### 🔍 跨社群 Pain Points 總結

1. **供電/電源管理** — 多模組同時供電（Nano + Servos + RF + Audio）
2. **馬達控制** — Servo 角度對齊、步進馬達精度
3. **入門鴻溝** — YouTube 教程混亂，初學者無所適從
4. **MCU 選擇疲勞** — ESP8266 vs ESP32 vs Nano vs ATtiny  decision fatigue
5. **IoT 整合** — 資料視覺化、遠端監控、API 串接
6. **機構+電子整合** — 3D 列印與電路的協作設計
7. **焊接品質** — 耗材（錫線、烙鐵頭）極大影響體驗

### 🚀 跨社群趨勢觀察

1. **懸浮應用火熱** — 超音波懸浮、磁懸浮同時在 arduino/maker 發燒
2. **DIY 穿戴/個人裝置** — 智慧手表、智慧眼鏡、遊戲控制器
3. **癒合/健康導向** — 視障者工具、無障礙設計、個人降溫
4. **巨大型顯示器** — 144x 7段顯示器時鐘、LED 矩陣牆
5. **開源硬體風氣** — Pick and Place、Raspberry Pi / Arduino 相容設計
6. **自動化烹飪** — 社群認可「極難」但持續有人挑戰
7. **創客教育** — Arduino 嬰兒書、親子教程需求大

---

### ⚠️ 限制說明
- **即時資料缺口**：Pushshift 最新存檔約落後 6-12 個月
- **r/InteractiveArt**：資料嚴重不足（僅 2 筆有效 post）
- **建議**：若需更即時數據，建議設定 Reddit API 或 PRAW 以後繞過封鎖

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
| 2026-04-08 | 18:00 | 週期同步檢查 | ✅ 無新內容，確認同步完成 |

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

---

## GitHub 同步記錄（2026-04-08 21:00 UTC）

| 時間 | 操作 | 狀態 |
|------|------|------|
| 21:00 | 週期同步檢查 | ✅ 無新內容；aif-factory/hooks/memory_sync.js 已更新並推送 |

**檢查摘要**：
- workspace-memory/：目錄不存在（已停用）
- aif-memory/agent-memory/memory/：MEMORY.md、WINS.md、MISTAKES.md 均已同步（最後 commit: 313f664 @ 18:31:40 UTC）
- aif-factory/hooks/memory_sync.js：發現並推送修正（base path + 13 agents）
