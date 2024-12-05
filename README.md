# 开发文档

本仓库包含开发文档和 meta issue (如 [roadmap](https://github.com/bangumi/dev-docs/issues/1))。

## 仓库说明

- 现有API相关
  - [`bangumi/server`](https://github.com/bangumi/server) 仓库为目前 bangumi 网站运作的新 api 后端，基于 Go，实现现有的公开 api。
- 新网站相关
  - [`bangumi/frontend`](https://github.com/bangumi/frontend) 仓库为新网站的前端。
  - [`bangumi/server-private`](https://github.com/bangumi/server-private) 仓库为新网站 api 后端，基于 TypeScript，实现私有 API，专为新网站前端使用。
- 开发相关
  - [`bangumi/dev-env`](https://github.com/bangumi/dev-env) 仓库包含配置文件(docker-compose)和开发数据，用于后端开发和测试使用。
  - [`bangumi/api`](https://github.com/bangumi/api) 仓库包括 API 文档，用于第三方开发者查看。
- 微服务
  - [`bangumi/img-proxy`](https://github.com/bangumi/img-proxy) 切图服务器。
- 其他
  - [`bangumi/wiki-syntax-spec`](https://github.com/bangumi/wiki-syntax-spec) 为 wiki 语法的定义，用于未来扩展 wiki 功能。
  - [`bangumi/common`](https://github.com/bangumi/common) 仓库包括 relation, platform, staff 等常量对应关系的 yaml 文件。

不同的仓库拥有更具体的贡献要求，请阅读相关仓库的说明和贡献指南。

## API

### 现有公开 API

目前 bangumi 网站实际提供的了两套 API

1. 旧的公开 API

   这套 API 是 bangumi 最老也是最开始提供的 API，由 sai 编写，未开源。目前此 API 已停止维护（修 BUG 加功能得找 sai，但 sai 精力有限）。

   `https://api.bgm.tv/subject/100` 这种 API 路径中没有 `/v0/` 版本信息的 API 就是旧有 API。

   很多有一点历史的第三方开源项目仍在使用此 API。出于兼容考虑旧 API 依旧能访问但已不推荐使用，相关 API 文档已隐藏。
2. 新的公开 API

   为了取代旧的公开 API，目前 bangumi 提供了另一套 API。`https://api.bgm.tv/v0/subject/100` 这种路径以 `/v0/` 开头的即新的公开API。

   此 API 代码开源，由 Go 编写任何人都可参与项目，代码仓库为 [`bangumi/server`](https://github.com/bangumi/server)。在使用 API 时如遇到BUG 或有新需求可提 issue，也欢迎提 PR 贡献代码。但因为新的公开 API 已经发布，需要保证兼容性，所以即便有功能变动也不会引入 break change。

   新公开 API 使用 access token 进行用户认证，GET 请求支持跨域。

   |                                                  | 信息                                           |
   | ------------------------------------------------ | ---------------------------------------------- |
   | OpenAPI 文档                                     | https://bangumi.github.io/api/                 |
   | OpenAPI 文档仓库                                 | [`bangumi/api`](https://github.com/bangumi/api) |
   | 生产环境Domain                                   | `api.bgm.tv`                                 |
   | 开发环境Domain``（仅支持路径 `/v0/` 下的路由） | `api.bgm38.com`                              |


   > 开发环境使用仓库 [`bangumi/dev-env`](https://github.com/bangumi/dev-env) 中包含的数据，不定时会进行重置
   >

### 新网站和私有 API

目前 bangumi 正在进行新网站的开发，基于 React/TypeScript/Vite。新网站也开源，前端仓库位于 [`bangumi/frontend`](https://github.com/bangumi/frontend)，欢迎提交代码。

新网站前端使用 API 与后端通信，前端所使用的 API 被称为私有 API。私有 API 与现有公开 API 不同，专为新网站前端使用而开发。使用 cookies session 进行用户认证，目前仍处于开发阶段，无兼容性保证，不支持跨域。仓库位于 [`bangumi/server-private`](https://github.com/bangumi/server-private) 。

|                | 信息                                                                    |
| -------------- | ----------------------------------------------------------------------- |
| OpenAPI 文档   | https://bangumi.github.io/dev-docs/`` https://next.bgm38.com/p1/ |
| 生产环境Domain | `next.bgm.tv`                                                         |
| 开发环境Domain | `next.bgm38.com`                                                      |

开发环境使用仓库 [`bangumi/dev-env`](https://github.com/bangumi/dev-env) 中包含的数据，不定时会进行重置。开发环境 `bangumi/dev-env` 所包含的账号如下：

|    uid    |      昵称      |            邮箱            |       密码       |        备注        |
| :--------: | :------------: | :-------------------------: | :--------------: | :----------------: |
|   `2`   | `nickname 2` |       `2@bgm38.com`       | `lovemeplease` | 拥有 wiki 编辑权限 |
| `382951` |   `树洞1`   | `treeholechan@gmail.com` | `lovemeplease` |                    |
| `318250` |   `树洞2`   | `treeholechan2@gmail.com` | `lovemeplease` |                    |

## 公开 API 和私有 API 的关系

公开 API 主要为 APP 等客户端而开发，今后新网站发布后也依旧会持续维护和使用。 私有 API 专为新网站前端开发，为网站前端专用。今后新网站发布后将会同时存在两套 API 。
