## Atsez Ghoreyshinejad



I build at the intersection of engineering, financial markets and investment strategy, with a focus on models written from first principles and tested  against real data, from Nasdaq order books, Eurex option chains and UK gilts to German power prices and stress in a plate with a hole.

### Featured projects

**[Order-flow imbalance on Nasdaq and Binance tick data](https://github.com/atsez/lob-order-flow-imbalance)**
Replicates a published result that order-flow imbalance explains 65% of short-term price moves, getting 62.5% on a day of Nasdaq order book data and 68.9% on 24 days of Binance BTC futures (34 million events in total). A queue-position simulator built from Nasdaq order IDs shows that ignoring a quote's place in the queue overstates a market maker's fills by up to 3.75 times. A Polars and Plotly notebook rebuilds every feature independently and matches the original pipeline on all 2.19 million rows, which also caught a bug in how fractional BTC sizes were counted.
`Python` `C++` `Polars` `Plotly` `Jupyter` `pandas` `pytest`

**[Euro Stoxx 50 options market-making simulator](https://github.com/atsez/sx5e-options-market-making)**
Arbitrage-free volatility surface fitted to a real Eurex option chain, feeding a C++ Monte Carlo simulator of a market maker managing inventory risk and informed traders. Leaning quotes against inventory cut P&L volatility 59% and drawdown 65% at almost no cost to profit.
`C++` `Python` `OpenMP` `SciPy`

**[UK gilt 10s30s flattener](https://github.com/atsez/gilt-10s30s-flattener)**
A rates relative-value trade built from first principles. A gilt pricer written from the cash flows matches Bloomberg to five decimal places and shows the true carry is 38% worse than the usual spreadsheet shortcut, mostly from pull to par. Marked on Bank of England curve data since entry, the spread narrowed 27bp in three months for about 1.3 times the risk budget on paper. Ten years of history show the spread fails mean-reversion tests, so the win came from the discretionary case rather than a statistical edge.
`Python` `pandas` `SciPy` `statsmodels` `pytest`

**[QRT Data Challenge 2026](https://github.com/atsez/qrt-data-challenge-2026)**
Predicting whether systematic portfolios go up or down the next day (Qube Research & Technologies x Ecole Polytechnique). Found that overlapping return windows leak the target, rebuilt the shuffled timeline, and validated with purged, time-blocked cross-validation. The signal turned out to be cross-sectional, so the final model averages six LightGBM models built on same-day market and group context.
`Python` `LightGBM` `scikit-learn` `pandas` `pytest`

**[2D finite element solver with a Gaussian process surrogate](https://github.com/atsez/fea-stress-solver)**
Plane-stress solver written from scratch, converging at exactly the rate theory predicts and validated within 1.21% of handbook stress concentration data. A Gaussian process trained on 60 solver runs predicts unseen designs within 0.02%, about 88,790 times faster than a full solve.
`Python` `NumPy` `SciPy` `scikit-learn` `pytest`

**[German clean spark spread](https://github.com/atsez/de-clean-spark-spread)**
A Python pipeline that joins German day-ahead power, TTF gas and EUA carbon prices and computes the clean spark spread, the margin a benchmark gas plant earns after fuel and carbon costs. Across 620 trading days the spread averaged -EUR 12.38/MWh, so a standard plant ran at a loss on 70% of days. Splitting the latest recovery by leg shows it was driven by power prices, not gas or carbon.
`Python` `pandas` `matplotlib` `pytest`

### Other work

- Statistical arbitrage study on 435 mining and metal pairs, showing that cointegration without an economic link mostly picks up shared trends; trading only the 34 linked pairs gave a 0.56 Sharpe on held-out 2023-26 data, net of costs
- Programmed fully autonomous robots in Python and LabVIEW as captain of Iran's World Robot Olympiad delegation, top 24 of 84 countries

### Toolkit

Python (pandas, Polars, NumPy, SciPy, scikit-learn, LightGBM, PyTorch, Plotly) · Jupyter · C++ (OpenMP) · Git · Bloomberg Terminal

### Contact

[LinkedIn](https://www.linkedin.com/in/atsez-ghoreyshinejad-329727309) · s.atsez.gh@outlook.com
