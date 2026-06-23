# AI 盘前策略数据

本目录归档“沪深主板 AI 盘前策略任务”产生的数据。

## 目录结构

```text
data/ai-premarket/
├── README.md
└── runs/
    └── YYYY/
        └── MM/
            └── DD/
                ├── YYYY-MM-DD-HHMMSS-early.md
                ├── YYYY-MM-DD-HHMMSS-final.md
                └── YYYY-MM-DD-HHMMSS-sources.md
```

文件名使用北京时间生成时刻，精确到秒。这样每天多次推送会形成累积记录，不覆盖历史文件。

## 数据原则

- 任务输出必须保留来源链接。
- 不保存券商账户、身份证明、截图原图等敏感信息。
- 持仓快照只保留任务所需字段：标的、代码、数量、成本、现金口径。
- 若数据来自过往快照，必须在报告中说明可能与实际账户存在偏差。
