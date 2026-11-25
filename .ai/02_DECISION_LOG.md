# 02_DECISION_LOG.md（架構決策與 Dead Ends 防呆庫）

- 最後核對：2026-11-25（V20）。

## 一、不可違背的架構決策（Immutable Decisions）

- [MWG 修正] 現代化寫法不得提高頁面現有的 Safari／iOS 最低版本（iOS 跟著系統，舊裝置停更就卡住；Chrome、Edge、Firefox 會自動更新，以 Baseline Widely available 為準）；畫面與結果不可變差（Shainy 2026-11-25：「可變好，不可變差」）。外部 CDN 腳本鎖版本並加 SRI。〔已核對：本 repo mwg-modernize PR〕
- 其餘待 Shainy 指定。

## 二、失敗死胡同（Dead Ends：接手 LLM 禁止重複嘗試）

- 無。
- （新增規則：任何 AI 寫出會報錯或邏輯崩壞的寫法，立刻以一行記在此處。）
