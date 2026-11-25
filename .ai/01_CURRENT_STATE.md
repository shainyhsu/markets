# 01_CURRENT_STATE.md（SSSM 語義狀態空間快照）

- 最後更新：2026-11-25 08:28（台灣時間）

## 1. 逐字任務目標（Verbatim Objective & Done Criteria）

- 當前唯一原子任務：MWG 修正。Shainy 2026-11-25 08:04 逐字：「開始修正，在不改變或降低安全、ui、計算、效能的前提下（可變好，不可變差）。」
- 完成驗收條件：畫面與結果不變（main 與分支逐字、逐像素比對）；外部腳本雜湊與 npm 原檔一致；一個分支、一個 PR，Shainy 說合併才合併。

## 2. 已驗證事實（Verified Facts）

- 版本：main 為 V19（2026-11-13 09:36）；本分支 V20。〔程式碼核對〕
- 價格資料：Binance 現貨與合約 REST（api.binance.com/api/v3/、fapi.binance.com/fapi/v1/）與 WebSocket（stream.binance.com、fstream.binance.com）；connectWebSocket()、fetchKlines()。〔程式碼核對〕
- Chart.js：V19 載入未鎖版本的 https://cdn.jsdelivr.net/npm/chart.js（2026-11-25 解析為 4.6.2 的 dist/chart.umd.min.js）；V20 改鎖同一檔案並加 SRI，位元組相同，sha384 與 npm 套件原檔一致。〔雜湊比對〕
- 狀態存 localStorage：btc_lang、live_symbol、live_tz、theme；無 Service Worker、manifest、IndexedDB。〔程式碼核對〕
- 圖表十字線拖曳用 mouse 與 touch 兩套事件（setupCrosshair() 內），未用 Pointer Events。〔程式碼核對〕

## 3. 未驗證想法與待確認假設（Unverified，不得當作已實作）

- 待 Shainy 指定。

## 4. 已套用變更與下一步唯一動作（Applied Changes & Immediate Next Action）

- 已修改檔案（2026-11-25，09:01 合併上線）：index.html（Chart.js 鎖 4.6.2＋SRI；螢幕閱讀器用的隱藏 h1 由 clip: rect() 改 clip-path: inset(50%)）、README.md、CHANGELOG.md（V20）、AGENTS.md（Popover 說明、改指向 .ai/）、新建 .ai/00–02。
- 下一步唯一動作：待 Shainy 指定。
