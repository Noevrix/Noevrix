# Noevrix

<img src="https://raw.githubusercontent.com/Noevrix/Noevrix/main/assets/noevrix.svg" width="80" alt="Noevrix" />

**A local-first AI assistant for thinking, research and data.**

Current version: **Noevrix 1.1 Beta — Data Intelligence & Quant Research** (Windows x64, pre-release).

[Download 1.1 Beta](https://github.com/Noevrix/Noevrix/releases/tag/v1.1.0-beta) · [Release notes](RELEASE-NOTES-1.1-BETA.md) · [Model setup](MODEL-SETUP.md) · [Known issues](KNOWN-ISSUES.md) · [Feedback](https://github.com/Noevrix/Noevrix/issues)

## Install

Download `Noevrix-Setup-1.1-Beta.exe` and `SHA256SUMS.txt` from the release page. Verify the installer hash with PowerShell `Get-FileHash` before running it. The installer is **unsigned**. Target platforms are Windows 10 22H2 and Windows 11 x64 with .NET Framework 4.8; clean Windows certification remains pending.

The runtime and local retrieval model are bundled. Ollama and the language model are **not** bundled: follow [model setup](MODEL-SETUP.md). The Noevrix identity currently uses Qwen2.5-7B-Instruct, not a foundation model trained from scratch. No Python or pip setup is needed for the installed app. Model speed and memory requirements depend on your hardware. Existing working Noevrix models do not need to be replaced. First-time model preparation currently requires the manual PowerShell steps in the guide; there is no one-click setup yet.

Allow approximately 3 GB for application installation/update and at least 10 GB separately for Ollama, the roughly 4.7 GB language model and download cache. 16 GB RAM or more is preferable for the current 7B model; CPU-only inference can be slow. These are planning guidelines, not broad hardware certification.

## General AI and research

Native desktop chat, local-model reasoning, local PDF/text document research, citations and reliable calculation tools. Public webpage reading is available for user-provided links; search engines and experimental online market providers remain disabled.

## New in 1.1: Data Intelligence

Open **+ → 分析工作区** to import CSV, inspect schemas and data quality, ask supported natural-language questions and review verifiable calculations. The unified Dataset Registry connects chat and the native Analysis Workspace. Follow-up questions retain the selected dataset and analysis scope. Statistical tools cover distributions, growth, contributions, correlations, covariance, descriptive regression and rolling statistics.

## Quant Research

Analyze explicit price/NAV or decimal-return data: compounded returns, equity, drawdown, volatility, frequency-aware annualization, Sharpe/Calmar and aligned benchmark comparisons. Basic factor research supports IC, Rank IC and grouped future returns, with explicit availability/label timing checks. Units, frequency and financial assumptions must be specified; unknown values are not invented.

This is a research and data-analysis assistant, not a securities trading platform or investment-adviser service. It does not execute trades, guarantee predictions or provide a complete backtesting system.

## Workspace and visualizations

Native line, bar, histogram, scatter, correlation heatmap, equity, drawdown, rolling-volatility and factor-group charts. Hover over values, filter dates and zoom. Continue an analysis in chat or export Markdown, CSV, JSON and the selected chart as PNG. See the [workspace guide](NOEVRIX-1.1-FEATURES.md).

## Data and privacy

Local chat, imported PDFs/CSV, retrieval and calculations run on the device. Analysis explanations receive bounded verified findings rather than entire large tables. User-requested webpage reading contacts the target website: **local-first does not mean fully offline**. There is no automatic application telemetry or diagnostic upload. Data defaults to `%LOCALAPPDATA%\Noevrix`, with legacy directory compatibility; uninstall preserves user data. See [Privacy](PRIVACY.md).

## Current limits

- Beta, not Stable; unsigned; no completed clean Windows validation. Hardware performance varies.
- CSV: **4 MB / 20,000 rows / 32 columns**; 64 MB registry. No large-file streaming.
- At most eight numeric analysis columns, 4,096 equity observations and 24 factor observation dates per request; charts display at most 400 sampled points.
- Supported natural-language rules may require clarification. Incorrect inputs and AI explanations require human review.
- Online market data/search engines/report downloads disabled; scanned PDF OCR unsupported. See [Known issues](KNOWN-ISSUES.md).

## Licensing and repository scope

This is the **closed-source product documentation and distribution repository**. Noevrix's proprietary application source, training data, adapters and user records are not published here. [LICENSE](LICENSE) and [EULA](EULA.md) govern Noevrix-owned software; no open-source license is assigned to that code.

Third-party software and models retain their original licenses and rights, independently of Noevrix terms. [Third-party notices](THIRD-PARTY-NOTICES.txt) identify components; full license texts and required source archives ship in the installer. Qwen2.5-7B-Instruct uses Apache-2.0; Ollama is separately installed. See also the [financial disclaimer](FINANCIAL-DISCLAIMER.md).

## 中文概要与反馈

1.1 相比 0.9 新增数据分析工作区、统计与量化研究、基础因子分析和交互图表，保留通用聊天布局。通过 **+ → 分析工作区** 导入自己的 CSV，核验分析口径，再导出结果。软件自有源码保持闭源，不公开训练或用户资料；第三方许可独立适用。

[提交反馈 / Issues](https://github.com/Noevrix/Noevrix/issues)：请说明版本、系统和复现步骤，不要上传密钥、私人聊天或商业研报。历史 [0.9 Public Beta](https://github.com/Noevrix/Noevrix/releases/tag/v0.9.0-beta) 继续保留。
