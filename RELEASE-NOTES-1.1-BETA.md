# Noevrix 1.1 Beta
## Data Intelligence & Quant Research

Noevrix is a local-first AI assistant for thinking, research and data. This Windows pre-release extends 0.9 with a native data analysis workspace while retaining general chat and local document research.

## What's New

- **Data Intelligence:** inspect schemas, missing values, duplicates and outliers; produce traceable analysis plans and results.
- **Analysis Workspace:** open **+ → 分析工作区**, import your own CSV, choose a dataset and refine the analysis scope.
- **Natural-language analysis:** supported requests and contextual follow-ups share dataset and date-range context. Ambiguous tasks need explicit parameters or clarification.
- **Statistical analysis:** descriptive statistics, growth, category contributions, correlation, covariance, descriptive OLS, distributions and rolling statistics.
- **Quant Research:** compounded returns, equity and drawdown, volatility, frequency-aware annualization, Sharpe/Calmar and aligned benchmark comparison.
- **Basic factor research:** cross-sectional IC, Rank IC and grouped future returns with explicit availability and label-time checks. User-supplied timestamps still require verification.
- **Interactive charts:** native line, bar, histogram, scatter, correlation heatmap, equity, drawdown, rolling volatility and factor-group charts; hover, date range and horizontal zoom.
- **Contextual follow-up and export:** continue selected analysis in chat; export Markdown, CSV, JSON and the selected chart as PNG.

## Improvements

Calculations reuse reliable tools and the unified Dataset Registry. Numerical findings remain independently computed; the local AI can organize verified findings without rewriting their values. Analysis stays integrated in the native Windows client. Upgrade tests check that existing user data is preserved; back up important originals before upgrading.

## Installation and model dependency

Download **Noevrix-Setup-1.1-Beta.exe** and verify it with **SHA256SUMS.txt**. Target: Windows 10 22H2 / Windows 11, x64, .NET Framework 4.8. Ordinary users do not need Python or pip.

The installer includes the application runtime and a small local retrieval model. **Ollama and the language model are separate installations.** The current Noevrix identity uses Qwen2.5-7B-Instruct (Apache-2.0), not a foundation model trained from scratch. See [MODEL-SETUP.md](https://github.com/Noevrix/Noevrix/blob/main/MODEL-SETUP.md). Existing working models need not be recreated. Deterministic data tools do not require a running language model.

## Privacy and licensing

Local-first does not mean entirely offline: user-requested public webpage reading contacts those websites. Local chat, file parsing and CSV analysis do not automatically upload user files. No application analytics or automatic diagnostic upload is enabled. Experimental online market providers, search engines and online report downloads remain disabled in this public build.

Noevrix's own application remains proprietary/closed source. Third-party components retain their own rights and license texts, including required source archives supplied with the installer. See [EULA](https://github.com/Noevrix/Noevrix/blob/main/EULA.md), [Privacy](https://github.com/Noevrix/Noevrix/blob/main/PRIVACY.md) and [Third-party notices](https://github.com/Noevrix/Noevrix/blob/main/THIRD-PARTY-NOTICES.txt).

## Known Limitations

- **Beta, not Stable. Unsigned installer.** Windows may show an unknown-publisher/SmartScreen warning.
- **Clean Windows validation has not been completed.** Acceptance is on the development machine with isolated installation and user-data directories, not broad hardware certification.
- CSV: **4 MB / 20,000 rows / 32 columns**, registry quota 64 MB. No large-file streaming analysis.
- Up to eight numeric analysis columns, 4,096 equity observations (including the initial baseline), and 24 factor observation dates per request. Charts sample at most 400 points; calculations use the selected data.
- Hardware and model performance vary. Some requests require clarification. Missing financial observations, unknown price adjustment and incompatible frequency assumptions may block calculations.
- Research, education and data analysis only: no automated securities trading, investment-adviser service or guaranteed financial predictions. No full backtesting system.
- Scanned PDFs have no OCR; complex layouts and restricted or JavaScript-only webpages may not be readable.

## 中文说明

Noevrix 1.1 Beta 新增原生分析工作区、数据识别、统计与量化分析、基础因子研究、交互图表、连续追问和结果导出。入口为 **+ → 分析工作区**。CSV 限制为 4 MB、20,000 行；大文件流式处理尚未实现。计算在本机完成，解释使用可核验结果。联网阅读会访问用户提供的网站，公开版在线行情与搜索服务保持关闭。

这是未签名的测试版，不是稳定版；尚未完成纯净 Windows 验收。Ollama 和 Qwen 基础语言模型需单独准备，已有模型无需重新下载。自有软件保持闭源，第三方许可不受限制。金融功能仅用于研究、教育和数据分析，不提供交易执行或收益保证。

Feedback: [GitHub Issues](https://github.com/Noevrix/Noevrix/issues). Do not include private documents, credentials or personal chat logs in public issues.
