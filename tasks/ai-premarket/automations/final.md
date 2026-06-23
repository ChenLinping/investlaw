# 自动任务配置：复核版

| 字段 | 值 |
|---|---|
| Automation ID | `ai-2` |
| 名称 | 沪深主板 AI 盘前策略 复核版 |
| 状态 | ACTIVE |
| 时间 | A 股交易日 08:15 |
| 模型 | gpt-5.4 |
| 推理强度 | high |
| 执行环境 | local |
| 工作目录 | `/Users/chenlinping/Documents/investlaw` |

## 核心要求

- 先核验当日是否为 A 股交易日。
- 读取同日 `data/ai-premarket/runs/YYYY/MM/DD/early.md`。
- 重新检索最新权威来源并更新判断。
- 输出“早版 vs 复核版”的相同结论、不同结论、变化原因和最终可执行操作清单。
- 新增个股仅限沪深主板。
- 优先结合 `tasks/ai-premarket/portfolio/2026-06-22-holdings.md` 中的持仓和现金。
- 所有 A 股买卖建议必须按 100 股整数手给出可执行股数。
- 输出并保存到 `data/ai-premarket/runs/YYYY/MM/DD/final.md`。
- 运行结束后提交并推送本仓库。
