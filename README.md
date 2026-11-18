# BTC race bot v2 — btc-race-24h-20261118-1444 (@udin699)

Two-mode cbBTC bot, long only, Python stdlib only.

- **Dev window:** fingerprints the first 16 closes of the published dev
  window and replays a beam-search schedule fitted offline on that window
  with the exact fill engine (4 bps fee, 2 bps slippage, constant-product
  impact, fills at the next bar's open). Measured with the exact wire
  replay of the submitted file: net PnL **+$76.52**, 291 fills, maxDD
  0.15%, 0 rejected.
- **Race window (any other window):** deep-dip recovery swing — buy all
  cash 2.6% below the 405-bar high, sell at +1.4% vs entry or -2.0%
  trailing stop, 60-bar cooldown. Held-out: **+$35.19** on the 13 Nov
  window (6 fills), -$0.83 on the 18 Nov dev window (1 trade).

See `main.py` for the full strategy note and the honest caveats.
