# Known Issues — Noevrix 1.1 Beta

- Clean-machine validation pending — 本轮仅在开发机隔离目录验收，未运行纯净 Windows 验收。
- Unsigned Beta Build：可能出现 SmartScreen / 未知发布者提示，未伪造签名。
- 搜索引擎、实验行情和联网研报下载在公共版关闭，来源商业条款未确认；可导入本地资料或提供公开网页链接。
- Hardware performance varies：长上下文和索引耗时取决于内存/CPU/GPU；不保证所有设备流畅。
- Online provider availability may vary：公开网页可能因限制、网络、JS 渲染或页面变化而无法读取。
- 扫描 PDF 无 OCR；复杂排版会影响文字提取；加密/损坏文件会拒绝读取。
- AI 会出现事实错误；复杂 CSV 问题或缺少日期/频率/单位时可能需澄清。
- 无权威交易日历，不能把未知数据频率当作已确认日频。

- CSV: 4 MB / 20,000 rows / 32 columns; bounded in-memory analysis, no large-file streaming. Registry quota: 64 MB.
- Charts sample at most 400 points; calculations use the selected data. At most eight numeric analysis columns, 4,096 equity observations and 24 factor observation dates.
- Natural-language analysis uses supported rules; ambiguous columns, units or financial assumptions require clarification. No backtesting, automated trading or guaranteed predictions.
