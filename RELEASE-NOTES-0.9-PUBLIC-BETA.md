# Axiom 0.9 Public Beta

## Highlights

A local-first AI assistant for thinking, research and data.
面向思考、研究与数据工作的本地优先 AI 助手。

本版提供 Windows 安装程序、用户说明、闭源 Beta 许可、完整第三方许可和隐私说明。保留已有聊天、研究与数据能力，没有新增训练或回测功能。

## Core Features

AI 聊天、深度思考、本地文件/PDF 阅读、研究问答、CSV 分析和白名单计算工具。公开链接阅读需要用户主动启用；搜索引擎查询当前关闭。

## Privacy

普通聊天、PDF、CSV 在本机处理；用户指定网页的 URL、IP 与请求信息发往目标网站。没有自动上传聊天、文件或诊断。详见 PRIVACY.md。

## Known Issues

纯净 Windows 验证待完成；Unsigned Beta Build 可能出现 SmartScreen 提示；硬件性能差异、网页可用性和 AI 错误仍需注意。扫描 PDF 无 OCR，复杂数据问题可能需要澄清。

## Disabled Experimental Features

Brave/Bing 搜索引擎查询、实验行情、联网研报下载、Trainer 和 Debug UI 在公共构建中关闭。已实现的开发功能保留在开发项目中。

## Model Information

语言模型通过本机 Ollama 使用 Qwen2.5 7B，Axiom 是产品身份与应用行为，不是从零预训练模型。安装包不含 Ollama、LLM 权重或 Adapter，仅附既有小型本地检索模型。已有生产模型无需重新训练或下载。

## Feedback

通过实际发布页面提供的反馈渠道提交系统版本、操作步骤及错误现象；需要时从“关于”导出诊断，先自行检查内容。不要公开聊天、原始文件或密钥。本软件不自动上传反馈。

## Clean-machine validation notice

Clean Windows validation has not yet been completed.
SKIPPED BY USER / PENDING。当前仅完成开发机回归与安装验收，不是 Fully validated release。

版本0.9.0-beta.2，Windows文件版本0.9.0.2，Build 20260914.2，channel beta，config schema 1。软件包准备完成不等于已经上传发布。
