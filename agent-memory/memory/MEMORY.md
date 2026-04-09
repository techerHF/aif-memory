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

## Reddit/HN 研究掃描（2026-04-09）

**資料來源**：Hacker News（Reddit IP 被封鎖，改用 HN Algolia 搜尋 × 6 關鍵字 + HN Top 20）
**掃描時間**：2026-04-09T06:04 UTC
**說明**：Reddit 直接存取遭封鎖，改走 HN；關鍵字涵蓋 arduino、maker、electronics、interactive design、sensor、raspberry pi，加上 HN Top 20。

---

### 📊 本週 Pain Points（抽出 pain_point 的 post）

| # | 標題 | 來源 | Pain Point |
|---|------|------|------------|
| 1 | Git commands I run before reading any code | HN:top | Need efficient Git commands to quickly understand an unfamiliar codebase |
| 2 | I ported Mac OS X to the Nintendo Wii | HN:top | Curiosity about technical challenges of porting OS X to legacy hardware |
| 3 | LittleSnitch for Linux | HN:top | Need network monitoring/filtering tool for Linux to control outgoing connections |
| 4 | Who is Satoshi Nakamoto? | HN:top | Desire to uncover Bitcoin creator's true identity |
| 5 | John Deere to pay $99M right-to-repair settlement | HN:top | Concern about legal/practical implications of right-to-repair |
| 6 | USB for Software Developers | HN:top | Want to learn writing userspace USB drivers for custom hardware |
| 7 | Kalman filter with radar example | HN:top | Need clear, practical explanation of Kalman filter with radar example |
| 8 | Understanding Traceroute | HN:top | Need clear understanding of how traceroute works to diagnose network issues |
| 9 | Muse Spark: personal superintelligence | HN:top | Curious about scaling AI toward personal superintelligence |
| 10 | Six intuitions for KL divergence | HN:top | Seeking intuitive explanations for KL divergence in ML |
| 11 | Ask HN: Any interesting niche hobbies? | HN:top | Looking for novel niche hobbies that allow meaningful contribution |
| 12 | MegaTrain: Full Precision Training of 100B+ LLMs on 1 GPU | HN:top | Interested in training massive LLMs on a single consumer GPU |
| 13 | They're made out of meat (1991) | HN:top | Curious about this classic sci-fi short story |
| 14 | ML promises to be profoundly weird | HN:top | Curious about weird implications of ML |

---

### 📊 熱門硬體/技術討論（按 score 排序）

**Raspberry Pi 系列（持續 dominate）**：
- Raspberry Pi 400 Desktop PC（2594票，754留言）
- Raspberry Pi 4（2504票，837留言）
- Raspberry Pi 5（1674票，1022留言）
- Raspberry Pi Zero: $5 computer（1271票，513留言）
- Unbricking a $2k bike with $10 Raspberry Pi（967票）
- TinyPilot KVM over IP（756票）

**Arduino 動態**：
- Qualcomm to acquire Arduino（1340票，535留言）— 社群對開源掌控權的焦慮
- Arduino size of AA battery（528票）
- The Death of Arduino?（458票）— Arduino 開源相容性爭議
- Adafruit: Arduino's Rules 'Incompatible With Open Source'（437票）

**感測器/IoT 應用**：
- Building occupancy sensor with $5 ESP32 + serverless DB（670票）
- Inside a $1 radar motion sensor（612票）
- Monitoring home air quality with AirGradient DIY sensor（515票）
- IKEA Vindriktning Air Quality Sensor review（495票）
- ESP32 Buyer's Guide: Different Chips, Sensors（490票）
- Open source USB C camera with MIPI sensor, Lattice FPGA（482票）
- Tesla removes parking sensors, results terrible（472票）
- Spy camera detection using smartphone ToF sensors（812票）
- MacBook hinge angle sensor（1023票）

**Right to Repair（熱門且有法律進展）**：
- John Deere $99M settlement（258票，66留言）
- YouTube deleted electronics repair channel（775票）
- I Had My Electronics Seized by U.S. Customs（951票）
- Why We Must Fight for Right to Repair（866票）
- Hacking DRM to Fix Electronics Is Legal（924票）

**軟體開發者相關**：
- LittleSnitch for Linux（438票）— 網路監控工具需求
- USB for Software Developers: writing userspace USB drivers（254票）
- Expanding Swift's IDE Support（101票）

---

### 🔍 本週 Pain Points 總結

1. **Right to Repair 法律化** — John Deere 世紀大和解，DIY 電子維修的法律地位更穩，但電視/汽車巨頭仍被盯上
2. **IoT 室內環境監控** — ESP32 空氣品質、佔用感測、室內霧霾監測興趣持續高漲，DIY 方案受青睞
3. **低成本硬體資安** — $1 雷達感測器、ToF 感測器被拿來做間諜相機偵測，隱私與安全意識上升
4. **Raspberry Pi 持續统治** — Pi 400/5 是 maker 最常用主力機，生態系完整無懸念
5. **Arduino 開源爭議** — Qualcomm 收購後，社群對「Arduino 規則是否與開源相容」焦慮明顯
6. **Git/程式碼理解工具** — 工程師需要快速理解陌生 codebase 的工具（不只是看 code）
7. **USB 硬體程式設計** — 軟體開發者想學寫 userspace USB driver 來做自訂硬體互動
8. **感測器融合** — 雷達 + ToF + 麥克風陣列 多模態感測興趣增加（尤其 IoT 應用）

### 🚀 跨社群趨勢觀察

1. **Right to Repair 進入法律確認階段** — $99M John Deere 和解是重大里程碑，後續會有更多品牌被迫開放
2. **感測器平民化** — $1 雷達、$5 ESP32、空氣品質感測器價格帶已到大量採用臨界點
3. **DIY 空氣品質監控** — 空汙意識 + 疫情後遺症，家用室內空品監測剛需明確
4. **Apple 硬體封閉性被戰** — MacBook 軸承角度感測器被拿出来討論
5. **ML/AI 進入各領域** — 從 KL divergence 到 100B parameter training，開發者對 AI 工具需求全面提升
6. **Linux 桌面安全工具缺口** — LittleSnitch for Linux 熱門，反映 Linux 玩家對網路監控的強烈需求
7. **IoT + 雲端無服務器整合** — ESP32 + serverless DB 的室內感測案例，證明輕量化 IoT + 後端即服務已完全可行

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

## GitHub 同步記錄（2026-04-08 22:30 UTC）

| 時間 | 操作 | 狀態 |
|------|------|------|
| 22:30 | 週期同步檢查 | ✅ 無新內容；所有檔案與 HEAD 校對一致，md5 校對通過 |

**檢查摘要（22:30）**：
- workspace-memory/MEMORY.md：最後修改 18:08 UTC，無變更
- workspace-memory/WINS.md：最後修改 15:39 UTC，無變更
- workspace-memory/MISTAKES.md：最後修改 09:27 UTC，無變更
- aif-memory/agent-memory/memory/：三檔案均與 HEAD (2a3a02f) 完全一致
- Git working tree clean，無待提交變更

## 診斷記錄 [2026-04-09T02:18:00Z] — MiniMax API Key 2049 錯誤排查

### 錯誤分類：PROVIDER_CONFIG_ERROR

### 根本原因（已確認）
memory_sync.js 第 53 行 hardcode 了錯誤的 API endpoint：
- **錯誤值**：https://api.minimax.chat/v1/text/chatcompletion_v2
- **正確值**：https://api.minimax.io/v1/text/chatcompletion_v2

openclaw.config.json 中正確設定為 `base_url: "https://api.minimax.io/v1"`
但 hooks/memory_sync.js 直接構造完整 URL，繞過了 config

### 驗證結果
| 測試 | 結果 |
|------|------|
| api.minimax.chat | 2049 invalid api key |
| api.minimax.io | 200 OK，response valid |

### 受影響範圍
- memory_sync hook 的 generateReflection() 全部失敗
- 任何直接使用 api.minimax.chat 的程式碼

### 下一步
修正 memory_sync.js 的 API endpoint，或改用 provider config 的 base_url

---

## GitHub 同步檢查 [2026-04-09T04:00:00Z]

**執行者**：記憶管理員 cron job
**檢查範圍**：13 agents × 3 檔 (MEMORY.md / WINS.md / MISTAKES.md) + shared/ 5 檔

**結果**：✅ 全部 44 檔案與 GitHub HEAD 同步，無需更新

**Agents 狀態**（有實質內容）：manager, memory, cfo, counselor, writer
**Agents 狀態**（模板檔）：dreamer, explorer, publisher, qa, researcher, sales, secretary, seo

## 壓力測試寫入 [2026-04-09T11:53:21.161Z]
- 任務：Full-Team Stress Test Item 12
- Agent：memory

## 記憶同步 [2026-04-09T12:19:04Z] — Stress Test v2
- 同步範圍：manager/writer/qa/publisher/dreamer/secretary
- 同步內容：WINS/MISTAKES/MEMORY 增量
- 結果：✅ 全部同步完成
## 記憶同步 [2026-04-09T13:28:00Z] — Learning Stress Test v3 Round 1
- 同步範圍：manager / secretary / researcher / writer / seo / publisher / sales / qa / explorer / cfo
- 觀察：全部 10 個 agent 都有 R1 任務產出
- 品質：所有產出都有「備註：用於衡量未來成長」標記
- 備註：這是基準同步，用於衡量未來同步深度提升

## 記憶同步 R2 [2026-04-09T13:50:10Z] — Learning Stress Test v3 Round 2
- R1→R2 觀察：全部 agent 都有迭代產出
- 成長亮點：writer 從無引用 shared → 主動引用 BEST_PRACTICES
- 成長亮點：qa 從 55分 → 63分（+8）cross-agent 學習鏈驗證
- 成長亮點：secretary 從狀態描述 → 量化數據+鏈路追蹤

## 記憶同步 R3 [2026-04-09T13:57:05Z] — Learning Stress Test v3 Round 3
- R3 錯誤注入測試：writer 電路圖遺漏（danger）
- qa 發現危險等效：PENDING_ALERTS 寫入 ✅
- writer 自我修正：< 1 分鐘恢復 ✅
- counselor 處理：正確追蹤並結案 ✅
- 結論：危險→行動→恢復 鏈完整

## 記憶同步 R4 [2026-04-09T14:02:08Z] — Learning Stress Test v3 Round 4
- Shared Learning 驗證：全部 13 個 agent 都引用了至少 1 個 shared 檔案
- BEST_PRACTICES：被 5 個 agent 引用 ✅
- CURIOSITY_POOL：被 5 個 agent 引用 ✅
- TEAM_DECISIONS：被 5 個 agent 引用 ✅
- 成長亮點：R1=0 shared 引用 → R4=15 shared 引用

## 學習記錄建立 R5 [2026-04-09T14:08:08Z] — Learning Stress Test v3 Round 5
- R1-R5 成長軌跡記錄完成
- shared BEST_PRACTICES 更新：IoT 文章品質標準 + 四工具指南 + 多平台流程
- TEAM_DECISIONS 更新：SEO 季度目標 + Q2 OKR + 定價策略
- CURIOSITY_POOL 更新：CircuitLab 新工具發現
- 成長亮點：從被動同步→主動建立團隊學習記錄
