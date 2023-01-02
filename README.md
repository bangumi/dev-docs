# 开发文档

本仓库包含开发文档和 meta issue (如 [roadmap](https://github.com/bangumi/dev-docs/issues/1))。

## 仓库说明

[`bangumi/server`](https://github.com/bangumi/server) 仓库为新 api 后端。

[`bangumi/frontend`](https://github.com/bangumi/frontend) 仓库为新前端。

[`bangumi/api`](https://github.com/bangumi/api) 仓库包括 API 文档，用于第三方开发者查看。

[`bangumi/dev-env`](https://github.com/bangumi/dev-env) 仓库包含配置文件(docker-compose)和开发数据，用于后端开发和测试使用。

[`bangumi/img-proxy`](https://github.com/bangumi/img-proxy) 切图服务器。

[`bangumi/wiki-syntax-spec`](https://github.com/bangumi/wiki-syntax-spec) 为 wiki 语法的定义，用于未来扩展 wiki 功能。

不同的仓库拥有更具体的贡献要求，请阅读相关仓库的说明和贡献指南。

用于前端的私有 API 请查看 https://bangumi.github.io/dev-docs/

## API

`api.bgm.tv` 或 `next.bgm.tv` 域名下是正式运行的 api 地址，接入真实 bangumi 数据库。

https://dev.bgm38.com/ 是用于开发的 api 地址，后端接入的是 `bangumi/dev-env` 的数据库。

没有 CORS 检查。

包含几个账号

|   uid    |     昵称     |           邮箱            |      密码      |        备注        |
| :------: | :----------: | :-----------------------: | :------------: | :----------------: |
|   `2`    | `nickname 2` |       `2@bgm38.com`       | `lovemeplease` | 拥有 wiki 编辑权限 |
| `382951` |   `树洞1`    | `treeholechan@gmail.com`  | `lovemeplease` |                    |
| `318250` |   `树洞2`    | `treeholechan2@gmail.com` | `lovemeplease` |                    |

私有 API 文档 https://bangumi.github.io/dev-docs/
