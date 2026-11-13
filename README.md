# Live Rate & Charts

A single-page tool that converts Bitcoin (BTC) and gold (XAU) to US dollars at the live market rate, with price charts from the last hour to the last year.

**Live demo:** https://shainyhsu.github.io/markets/

## Features

- **Live converter**: type an amount of BTC or XAU and see its USD value, updated in real time as trades come in.
- **BTC and gold (XAU)**: switch between the two with one tap.
- **8 price charts (USD)**: last 1 hour, 24 hours, 3 days, 7 days, 30 days, 3 months, 6 months, and 1 year. The 1-hour chart keeps growing live.
- **Crosshair readout**: tap or drag on any chart to read the exact price and time at that point.
- **Time zone toggle**: show chart times in Taipei (TPE) or New York (NYC).
- **Language toggle**: Traditional Chinese or English.
- **Light/dark theme**: dark by default; your choice is remembered.
- **Responsive layout**: one column on phones, two columns on wide screens, and four chart columns on very wide screens.

## How to use

1. Open https://shainyhsu.github.io/markets/ in any modern browser. Nothing to install or sign up for.
2. Pick **BTC** or **XAU** at the top and type an amount; the USD value updates live.
3. Tap or drag on a chart to see the price at a given moment.
4. Use the top-right buttons to switch time zone (TPE/NYC), theme (light/dark), and language (zh/en). Your choices are saved in the browser.

**Note:** all data comes straight from Binance's public API. Binance may be unavailable in some regions (for example, the United States), in which case the price and charts will not load there.

## Tech

- One static `index.html` hosted on GitHub Pages; no build step and no backend.
- Live prices via Binance WebSocket trade streams: spot market for BTC (BTCUSDT), futures market for gold (XAUUSDT).
- Chart history via Binance REST candlestick (klines) endpoints, spot and futures.
- Charts drawn with [Chart.js](https://www.chartjs.org/) loaded from a CDN, with a custom crosshair.
- Settings (asset, language, time zone, theme) stored in the browser's `localStorage`.

## Version history

Newest first. Times are Taiwan time (UTC+8). Also kept in [CHANGELOG.md](CHANGELOG.md).

- V18 | 2026-11-13 09:20 | Added a tab icon and an "All tools" link in the footer; the chart library loads without holding up the page, and the amount boxes have labels for screen readers.
- V17 | 2026-11-12 23:40 | On a phone, charts now leave the page free to scroll: a quick tap or swipe scrolls, and you hold a finger still on a chart for half a second to show a price, then slide to move it
- V16 | 2026-11-11 10:07 | New license terms: free to use in a browser for personal, work, school or club use, and the results you make are yours to share; copying, paid services built on it, and AI training need written permission. A License link sits at the bottom of the page
- V15 | 2026-11-10 00:18 | Added a link-preview image (1200×630) so shared links show a picture in LINE, Facebook and other apps.
- V14 | 2026-11-09 11:24 | Wide-screen columns mirrored: the 1-hour chart sits top right and the 1-year chart bottom left.
- V13 | 2026-11-09 10:25 | Corrected the search and link-preview description: USD conversion only, listing all eight chart ranges.
- V12 | 2026-11-09 10:16 | Added 30-day, 3-month, 6-month and 1-year charts, plus a wide-screen layout with the converter and charts in two columns (four chart columns on very wide screens).
- V11 | 2026-11-09 09:23 | Added a light/dark theme toggle in the top-right corner (dark by default) and tightened the layout on small phones.
- V10 | 2026-11-08 20:28 | Improved how the page appears in search results and link previews, and re-enabled pinch-to-zoom on phones.
- V9 | 2026-11-03 07:49 | Minor fixes: the crosshair readout is now see-through so it no longer hides the line, and it stays on the chosen point while the live chart updates.
- V8 | 2026-11-03 07:05 | Added a crosshair readout (tap or drag a chart to see the exact price and time) and a Taipei/New York time-zone toggle.
- V7 | 2026-11-03 06:44 | Added gold (XAU) with a BTC/XAU switch, and moved to a dark theme.
- V6 | 2026-11-03 06:22 | Added a Chinese/English language toggle.
- V5 | 2026-11-03 06:01 | Switched to live Binance data: the price now updates in real time with a "live" indicator, and the 1-hour chart grows as new trades arrive.
- V4 | 2026-11-03 05:02 | The 1-hour chart now refreshes more often and ends at the current price.
- V3 | 2026-10-27 21:55 | Added a 1-hour price chart and kept charts cached for up to an hour to reduce loading errors.
- V2 | 2026-10-27 21:42 | Minor fixes: prices are briefly cached in the browser so reloading the page no longer runs into rate limits, with clearer error messages.
- V1 | 2026-10-27 21:00 | First public release: a BTC-to-USD converter with 24-hour, 3-day and 7-day price charts.

## License

Copyright (c) 2026 Shainy Hsu. All rights reserved. See [LICENSE](LICENSE).

You may use the published website for personal use in a browser. No copying, reproducing, modifying, redistributing, mirroring, scraping, or using any part of this work to train or evaluate AI/machine-learning models without prior written permission from the author.
