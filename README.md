# 开发文档

本仓库包含开发文档和 meta issue (如 [roadmap](https://github.com/bangumi/dev-docs/issues/1))。

## 仓库说明

[`bangumi/frontend`](https://github.com/bangumi/frontend) 仓库为新前端。

[`bangumi/server`](https://github.com/bangumi/server) 仓库为新 api 后端，基于 Go，实现现有的公开 api。

[`bangumi/server-private`](https://github.com/bangumi/server-private) 仓库为新 api 后端，基于 TypeScript，实现现有的私有 API。

[`bangumi/api`](https://github.com/bangumi/api) 仓库包括 API 文档，用于第三方开发者查看。

[`bangumi/dev-env`](https://github.com/bangumi/dev-env) 仓库包含配置文件(docker-compose)和开发数据，用于后端开发和测试使用。

[`bangumi/img-proxy`](https://github.com/bangumi/img-proxy) 切图服务器。

[`bangumi/wiki-syntax-spec`](https://github.com/bangumi/wiki-syntax-spec) 为 wiki 语法的定义，用于未来扩展 wiki 功能。

不同的仓库拥有更具体的贡献要求，请阅读相关仓库的说明和贡献指南。

用于前端的私有 API 请查看 https://bangumi.github.io/dev-docs/

## API

目前 bangumi 拥有两种 HTTP API，公开 API 和 私有 API。

（下文提到的开发环境使用的是 `bangumi/dev-env` 包含的数据，不定时会进行重置）

### 公开 API

openapi 文档：https://bangumi.github.io/api/

使用 access token 进行用户认证，保证兼容性，GET 请求支持跨域。

生产环境域名 `api.bgm.tv`

开发环境域名 `api.bgm38.com` (仅支持路径 `/v0/` 下的路由)

文档位于 https://bangumi.github.io/api/

### 私有 API

由 bangumi 的新前端使用，无兼容性保证，不支持跨域。

使用 cookies session 进行用户认证，无兼容性保证。

生产环境域名 `next.bgm.tv`

开发环境域名 `next.bgm38.com`

文档位于 https://bangumi.github.io/dev-docs/ 或 https://next.bgm38.com/p1/


开发环境 `bangumi/dev-env` 所包含的账号：

|   uid    |     昵称     |           邮箱            |      密码      |        备注        |
| :------: | :----------: | :-----------------------: | :------------: | :----------------: |
|   `2`    | `nickname 2` |       `2@bgm38.com`       | `lovemeplease` | 拥有 wiki 编辑权限 |
| `382951` |   `树洞1`    | `treeholechan@gmail.com`  | `lovemeplease` |                    |
| `318250` |   `树洞2`    | `treeholechan2@gmail.com` | `lovemeplease` |                    |

