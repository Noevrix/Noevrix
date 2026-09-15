# 准备 Noevrix 本地模型

当前客户端使用 Ollama + Noevrix:latest，基础模型为 Qwen2.5 7B。安装包包含客户端运行组件和既有文档检索模型；不包含 Ollama 或 4.7GB 语言模型。模型缺失不影响 Calculator / CSV 工具。

1. 从 https://ollama.com/download/windows 下载并安装 Ollama，随后启动它。Noevrix 不静默安装第三方软件。
2. 检查磁盘空间。当前模型约 4.7GB，Ollama 安装及运行还需要额外空间；建议为这些组件预留至少 10GB，可根据官方安装器提示调整。
3. 目前Public Beta提供以下手动模型准备步骤；在 PowerShell 中执行前确认愿意下载。普通用户不需要安装 Python、pip 或 CUDA。

```powershell
ollama pull qwen2.5:7b
ollama create Noevrix:latest -f "安装目录\config\Noevrix.Modelfile"
```

把“安装目录”替换成 Noevrix 的实际位置，例如 %LOCALAPPDATA%\Programs\Noevrix。已有 Noevrix 模型时先检查，不要无意覆盖自行修改的版本。回到 Noevrix 的“关于 → 检测环境”重新检测。

当前基础模型来自 Qwen2.5-7B-Instruct，采用 Apache-2.0 许可。原始模型和 Ollama 标签可能更新，重新准备的模型不一定与已有模型字节一致。Noevrix 是产品品牌，不是宣称基础模型从零训练。现有模型正常时无需重新创建。

## 硬件与常见问题

目标环境为 64 位 Windows 10 22H2 / Windows 11、.NET Framework 4.8 及安装包内的运行组件。CPU 可运行 Ollama；没有独显可能明显较慢。8GB RAM 不建议长上下文，16GB 以上更适合当前 7B，32GB 更利于文档任务；这是保守产品建议，不是全部硬件已实测的保证。显卡支持和驱动要求以 https://docs.ollama.com/windows 和 https://docs.ollama.com/gpu 为准。

- Ollama 未连接：启动 Ollama 后重新检测；勿对公网开放模型端口。
- 模型缺失：完成上述自愿下载步骤；不要把等待画面当作下载已开始。
- 超时/内存不足：关闭占内存的软件，缩短问题或上下文，重新发起请求。Noevrix 保留已保存历史。
- 检索组件缺失：使用 Noevrix 安装包修复，无需自行 pip install。

## 从旧版升级

Noevrix 优先使用 `%LOCALAPPDATA%\Noevrix`；新目录不存在而旧 `%LOCALAPPDATA%\Axiom` 存在时，继续读取旧目录，不删除或复制原聊天和文件。旧目录名称属于兼容约定。环境变量优先 `NOEVRIX_USER_DATA`，并兼容 `AXIOM_USER_DATA`。

已有旧版模型时，无需再次下载权重。可执行 `ollama create Noevrix:latest -f "安装目录\config\Noevrix.Modelfile"`；本机已缓存 Qwen2.5 7B 时重用缓存。旧 Axiom 模型不会删除。创建新的品牌身份层不等于重新训练。
