# 每日运行文件结构

每日输出目录：

```text
data/ai-premarket/runs/YYYY/MM/DD/
├── YYYY-MM-DD-HHMMSS-early.md
├── YYYY-MM-DD-HHMMSS-final.md
└── YYYY-MM-DD-HHMMSS-sources.md       # 可选：集中记录引用来源
```

文件名必须使用北京时间生成时刻，精确到秒。同一任务一天内多次运行时，不得覆盖旧文件。

## `YYYY-MM-DD-HHMMSS-early.md`

建议包含：

1. 生成时间；
2. 是否为 A 股交易日；
3. 盘前结论；
4. 市场评分；
5. 产业方向排序；
6. 存量持仓诊断；
7. 新增候选；
8. 仓位建议；
9. 盘中验证清单；
10. 关键来源。

## `YYYY-MM-DD-HHMMSS-final.md`

建议包含：

1. 生成时间；
2. 复核版最终结论；
3. 与早版相同的结论；
4. 与早版不同的结论；
5. 变化原因；
6. 今日最终操作清单；
7. 存量持仓诊断；
8. 新增候选；
9. 强势/震荡/弱势三套策略；
10. 来源链接。

复核版应读取同日目录中按文件名排序最新的 `*-early.md`，不得假设固定存在 `early.md`。
