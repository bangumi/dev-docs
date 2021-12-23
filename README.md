# 开发文档

## 仓库说明

本仓库包含开发文档和 meta issue (如 roadmap)。

[`bangumi/server`](https://github.com/bangumi/server) 仓库为新 api 后端。

[`bangumi/dev-env`](https://github.com/bangumi/dev-env) 仓库包含当前 bangumi 的 MySQL 数据表。

[`bangumi/wiki-syntax-spec`](https://github.com/bangumi/wiki-syntax-spec) 为 wiki 语法的定义，用于未来扩展 wiki 功能。

## 贡献代码

在 [roadmap](https://github.com/bangumi/dev-docs/issues/1) 中选择当前阶段你感兴趣的的任务。

1. 确保 `bangumi/dev-env` 中已有相关的表和数据。如果对应表定义和数据缺失请联系 @Trim21 进行导出。
2. [Fork server](https://github.com/bangumi/server/fork) 仓库并提交 PR。
3. 本仓库中添加对应表的说明。

有部分字段（比如人物表的`prsn_position`）在数据库中保存为了 int，对应旧代码库中的一个 enum，请联系 @Trim21 进行导出。
