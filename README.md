# Noevrix

<img src="assets/noevrix.svg" width="80" alt="NOEVRIX" />

**0.9 Public Beta**

[下载 Windows 安装包](https://github.com/Noevrix/Noevrix/releases/download/v0.9.0-beta/Noevrix-Setup-0.9-Public-Beta.exe) · [校验文件](https://github.com/Noevrix/Noevrix/releases/download/v0.9.0-beta/Noevrix-SHA256SUMS.txt)

A local-first AI assistant for thinking, research and data.
面向思考、研究与数据工作的本地优先 AI 助手。

## Repository Notice

Noevrix is a proprietary, closed-source application. This public repository is the official hub for distribution, documentation, releases, issues and feedback; the proprietary application source code is not published here. Third-party components, models and libraries retain their original licenses. See [LICENSE](LICENSE) and [Third-party notices](THIRD-PARTY-NOTICES.txt).

## 仓库说明

Noevrix 是专有、闭源应用。本公开仓库用于官方分发、文档、版本发布、问题跟踪与反馈，不公开专有应用源代码。第三方组件、模型和库仍遵循各自的原始许可，详见 [LICENSE](LICENSE) 和[第三方声明](THIRD-PARTY-NOTICES.txt)。

## What is Noevrix

Noevrix 支持 AI 聊天、深度思考、本地文件阅读、研究与数据分析。AI 回答可能不准确，重要信息请核验原文。本版为 Beta，并非稳定版；Clean Windows validation has not yet been completed。

## System Requirements

| 项目 | 最低运行条件 / 预留空间 | 建议 |
|---|---|---|
| 系统 | 64 位 Windows 10 22H2（19045）或 Windows 11；.NET Framework 4.8 | 更新并受支持的 Windows 系统 |
| 内存 | 轻量工具建议至少 8GB；不保证 8GB 能顺畅运行当前 7B 模型 | 16GB 以上，长文档可考虑 32GB |
| 客户端磁盘 | 安装/更新预留约 3GB；安装组件约 1.1GB | 另为自己的资料预留空间 |
| 模型磁盘 | 语言模型约 4.7GB；Ollama 和下载缓存另占空间 | 单独预留至少 10GB |
| GPU | 可选，支持 CPU；CPU 推理可能很慢 | 受 Ollama 支持的独立显卡，容量按模型决定 |
| 模型运行器 | 本机 Ollama + 已准备的 Noevrix:latest | 使用已有模型，避免重复下载 |

开发机验收为 Windows 11、约16GB内存、RTX4060 Laptop 8GB；这些结果不是全硬件性能保证。无需安装 Python、pip、VSCode、CUDA 开发工具或训练环境。

## Installation

运行 Noevrix-Setup-0.9-Public-Beta.exe，阅读许可并按向导安装。默认目录为 %LOCALAPPDATA%\Programs\Noevrix，无需管理员权限。安装包未数字签名，可能显示 “Windows protected your PC” 或未知发布者；这是未签名 Beta 的状态说明，不建议关闭任何 Windows 安全功能。请确认下载来源并核对 SHA256SUMS.txt；来源不明时不要运行。

## First Launch

从开始菜单打开 Noevrix。欢迎页检测组件和本机模型；“关于”中可重新检测、查看许可/隐私、导出诊断。没有模型时，窗口会显示准备步骤；基础计算与 CSV 工具不依赖语言模型。

## Ollama / Model Setup

从 https://ollama.com/download/windows 安装并启动 Ollama。安装包不包含语言模型，也不静默下载。已有 Noevrix:latest 时直接使用，不必重复创建。

首次创建 Noevrix 模型别名，目前确实还没有一键入口，需要按 MODEL-SETUP.md 执行一次模型准备步骤；仅这一步需要 PowerShell，日常聊天不需要。模型指南随安装包提供。Noevrix 使用开放权重 Qwen2.5 7B 基础模型，不宣称从零训练。

## Main Features

聊天、深度思考、文件问答、PDF/文本研究、CSV 数据分析、计算器及基础金融工具。深度思考可与联网阅读同时开启，是分析和复核流程，不代表已训练新模型。

## File Analysis

点击输入框左侧“+”上传合法取得的 PDF、TXT、Markdown，选择文件问答、论文分析或研报分析。资料在本机解析和索引，不上传给网站。扫描 PDF 无 OCR，复杂排版可能提取不准，加密或损坏文件需要先处理。请核对引用原文。

## Web Search

Brave/Bing 搜索服务的商业集成条款尚未确认，本公共 Beta 默认关闭搜索查询，不能仅输入关键词搜索全网。开启“联网阅读”并粘贴你有权阅读的公开网页链接，可阅读该网页并提问。目标站能看到 URL、IP 和请求信息，请勿将机密数据放入链接。不能读取所有网站，不绕过登录、付费或验证码。实验行情和联网研报下载同样关闭。

## CSV Analysis

从“+ → 导入与分析数据”选择 CSV，确认日期、字段、频率和收益率单位。内部0.05表示5%，未知频率不会被猜测。可用白名单工具进行基础收益、波动和回撤等分析。模型只获得摘要、样本和工具结果，完整大型表格不直接进入模型；复杂表达或缺字段时可能需澄清。

## Privacy

Local-first，不宣传完全离线。聊天、文件、索引、CSV 和本机模型推理在本地；用户选择的网页请求会联网。没有应用 Analytics、自动上传聊天/文件或自动上传诊断。数据保存在 %LOCALAPPDATA%\Noevrix，未额外加密。详见 PRIVACY.md。

## Known Limitations

纯净 Windows 验证尚未完成；软件未签名；模型速度因硬件而异；网页可能不可用；AI 会出错；扫描 PDF 未提供 OCR。完整说明见 KNOWN-ISSUES.md。金融功能仅为研究、数据分析与教育，不提供个人买卖建议或收益保证。

## Uninstall

从 Windows“已安装的应用”卸载 Noevrix。默认保留聊天、导入资料与外部模型。若要清除全部应用数据，退出后备份所需资料，再通过资源管理器删除 %LOCALAPPDATA%\Noevrix；原始文件、导出、系统备份及 Ollama 模型须另行管理。

## Troubleshooting

- 模型未连接：启动 Ollama，在“关于”重新检测。
- 模型不存在：按 MODEL-SETUP.md 准备 Noevrix:latest；不要反复重装客户端。
- 仅输入关键词无法联网：公共版关闭了搜索服务，请提供公开链接。
- 文件读取失败：确认不是扫描、加密、损坏文件，检查列/日期和单位。
- 启动或组件异常：关闭程序，用安装器修复。用户数据默认保留。
- 配置损坏：原文件备份后恢复默认配置，聊天和资料不会因此清空。
- 查看日志：Win+R 输入 %LOCALAPPDATA%\Noevrix\logs；关于页可导出经过筛选的 diagnostics。请检查导出内容后，自行向发布者反馈，程序不会自动发送。反馈使用实际下载页面提供的渠道。


## Repository

https://github.com/Noevrix/Noevrix

沿用现有 v0.9.0-beta 发布记录；历史标签不重写。
