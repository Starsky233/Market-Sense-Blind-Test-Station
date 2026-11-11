# Market Sense Blind Test

[中文](README.md)

**Try it: <https://starsky233.github.io/Market-Sense-Blind-Test-Station/>**

Test your trading instincts in the browser. The site picks a random moment from historical M1 data and shows the chart only up to that moment, with the date hidden. You call long, short or no trade. After a few hundred questions, the stats show what your calls are worth after spread and slippage, compared with random direction at the same moments.

## How to use

1. Open the link above and click "Load one year of USDJPY M1", or choose your own M1 CSV.
2. Make a call: Short (S), No trade (N) or Long (L), and set your confidence with 1, 2 or 3.
3. After each answer the page reveals what happened next: the return after 15, 30 and 60 minutes, and the result with a take-profit and stop-loss.
4. Click Stats at the top right for the summary. You can export your records as CSV.

## Features

- Timeframes: M1, M5, M15
- Indicators: EMAs (add several, any period), Bollinger Bands, volume, RSI and MACD, all with editable parameters
- Drawing tools: trend lines, horizontal lines, Fibonacci retracements
- Take-profit and stop-loss as ATR multiples or fixed pips, held until one side is hit, with no time limit
- Sampling: random moments or spikes only, optionally limited to chosen server hours
- Stats: gross and net returns, excess over random direction, t-values and 95% intervals
- Chinese and English interface, picked from your system language on first visit and switchable at the top right

## Data

`USDJPY_M1_last_year.csv` in this repository is USDJPY M1 data exported from MT5, from 2025-11-11 to 2026-11-10, about 370,000 bars, with the columns `time, open, high, low, close, tick_volume, spread, spread_px, real_volume`.

You can also use your own data in the CSV formats exported by MT5 or pandas. Files are read in your browser and never uploaded. Data and records are stored only in your own browser.

## Files

| File | Description |
| --- | --- |
| `index.html` | The whole site in one file, no build step |
| `USDJPY_M1_last_year.csv` | Sample USDJPY M1 data |

Opening `index.html` straight from disk also works, but the "Load one year of USDJPY M1" button is hidden there, so choose a CSV file instead.
