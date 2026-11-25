# 00_INTERFACE_CONTRACT.md（BTC & Gold Live Rates：黑盒契約與選擇性讀取索引）

- 頁面：https://shainyhsu.github.io/markets/ ；主檔 index.html（811 行），單一檔案、無建置步驟。
- 索引核對：2026-11-25，theme-meta 分支（V21，PR 待合併）。行號會隨改版漂移，以函數名稱為準：`grep -n "function 名稱" index.html` 重新定位，再更新本索引。
- 短上下文紅線（SSSM）：不整檔貼上，一律「函數定位＋局部片段（≤150 行／6,000 字元）」。

## 函數索引（index.html）

- applyLang() L402–407
- applyTz() L409–418
- updateTexts() L420–436
- switchSymbol() L441–467
- connectWebSocket() L472–493
- updateRates() L495–503
- fetchKlines() L506–513
- loadCharts() L515–530
- appendTo1hChart() L532–539
- getDateInTz() L541–543
- formatLabel() L545–559
- formatFullTime() L561–569
- repositionCrosshair() L599–651
- setupCrosshair() L653–722
- handlePointer() L657–680
- cancelHold() L689
- endTouch() L713
- renderChart() L724–794
- gridColor() L796
- sync() L809
