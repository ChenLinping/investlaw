# 自动任务配置：早版

| 字段 | 值 |
|---|---|
| Automation ID | `ai` |
| 名称 | 沪深主板 AI 盘前策略 早版 |
| 状态 | ACTIVE |
| 时间 | A 股交易日 07:50 |
| 模型 | gpt-5.4 |
| 推理强度 | high |
| 执行环境 | local |
| 工作目录 | `/Users/chenlinping/Documents/investlaw` |

## 核心要求

- 先核验当日是否为 A 股交易日。
- 检索并引用最新权威来源。
- 分析前一交易日 A 股、隔夜美股和半导体指数、宏观政策、地缘政治，以及 NVIDIA、AMD、Intel、Google、台积电等 AI 产业链动态。
- 新增个股仅限沪深主板。
- 优先结合 `tasks/ai-premarket/portfolio/2026-06-22-holdings.md` 中的持仓和现金。
- 所有 A 股买卖建议必须按 100 股整数手给出可执行股数。
- 输出并保存到 `data/ai-premarket/runs/YYYY/MM/DD/early.md`。
- 运行结束后提交并推送本仓库。
