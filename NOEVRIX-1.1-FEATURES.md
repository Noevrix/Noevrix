# Noevrix 1.1 Beta — Data Intelligence & Quant Research

Noevrix remains a local-first general AI assistant. Open **+ → 分析工作区** to use your own CSV files without a browser.

1. Import a general table with **导入表格 CSV**, or import strict price/return data with **行情 / 收益 CSV**. Select column units and frequency explicitly; unknown is a valid choice.
2. Select a dataset and ask **帮我全面分析一下这份数据**. Inspect the schema, missing values, duplicates, outliers, methods and numerical results.
3. Pick a chart, hover to inspect values, zoom horizontally or select a date range. Continue with **最近三个月呢？** or **把它画出来**.
4. Use **计算参数与研究口径** for columns, rolling window, annual periods, per-period risk-free rate, benchmark or factor/label names.
5. Export Markdown, result CSV and the current PNG chart. The export also contains structured JSON for verification. **在聊天中继续** starts an explicitly selected dataset discussion; subsequent analysis context belongs to that conversation.

## Supported analysis

- Descriptive statistics, missing/duplicate counts, IQR outlier flags, growth, category contributions, correlation, covariance, descriptive OLS, rolling mean/std and distributions.
- Price/NAV or explicitly declared decimal returns: compounded cumulative/total return, equity, drawdown, per-period volatility, rolling return/volatility/drawdown, aligned asset correlation and benchmark comparison. Annualization requires an explicit frequency and matching periods per year; Sharpe also requires a per-period risk-free rate. Calmar is undefined when observed drawdown is zero.
- Minimal factor research: distribution, factor/label correlation, cross-sectional IC, average-tie Rank IC and group mean future returns. Required columns: `symbol`, `date`, `available_date`, `label_start`, `label_end`, factor and future-return label. Declare the label unit `ratio`. Availability must not exceed observation date and label intervals must be strictly later. No intraday availability semantics or trading/backtesting.
- AI may select existing verified findings; it cannot rewrite numerical results. A deterministic report remains available when the local model is unavailable.

## Limits

CSV: 4MB, 20,000 rows, 32 columns, 64MB registry quota. General analysis selects at most eight numeric columns. Financial tools accept at most 4,096 equity observations including the initial baseline. Factor research handles at most 24 observation dates per request. Select a smaller time range or split larger files. This is bounded in-memory analysis, not out-of-core processing.

Charts sample at most 400 points; the full selected data is used for calculations. Correlation charts display bounded pairwise cells. Missing financial values, ambiguous dates, unknown price adjustment and incompatible annualization are rejected. General analysis retains duplicates and excludes missing cells only as disclosed. No imputation or silent deletion.

No new model, adapter training, LLM download, external file upload, trading API or online market entitlement is introduced. Public builds keep unlicensed market providers disabled. Qwen and all third-party license attribution remains applicable. Beta is not Stable; clean-machine certification and code signing remain outstanding.
