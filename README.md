# 开发文档

## 仓库说明

本仓库包含开发文档和 meta issue (如 roadmap)。

[`bangumi/server`](https://github.com/bangumi/server) 仓库为新 api 后端。

[`bangumi/dev-env`](https://github.com/bangumi/dev-env) 仓库包含当前 bangumi 的 MySQL 数据表。

[`bangumi/wiki-syntax-spec`](https://github.com/bangumi/dev-env) 为 wiki 语法的定义，用于未来扩展 wiki 功能。

## 问题反馈

新 API 请在 [server](https://github.com/bangumi/server) 仓库进行反馈。

旧 API 在 [api](https://github.com/bangumi/api) 仓库进行反馈。

## 贡献代码

在 [roadmap](https://github.com/bangumi/dev-docs/issues/1) 中选择当前阶段你感兴趣的的任务。

1. 确保 `bangumi/dev-env` 中已有相关的表和数据。如果不存在对应的表则需要联系 sai 进行导出，并提交到 `dev-env` 仓库中。
2. [Fork server](https://github.com/bangumi/server/fork) 仓库并提交 PR。
3. 本仓库中添加对应表的说明。
