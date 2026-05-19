# tool-lab-postman-collection-minimal

用 **Postman Collection**（`postman_collection.json`）把一个或多个 HTTP 请求**固化成可复用的模板**：同一套请求可在团队间分享、改名、批量跑 Collection Runner。

<!-- 与同套实验一致 -->

## Collection 文件是什么

- **Postman** 最常见的玩法之一：导入 `*.json`，在左侧看到「文件夹 + 请求」。
- **Collection Variables**：本仓库预设 `demoBase`（公有 Demo API）与 `expressBase`（本机 Stage 3）。

## 这个最小实验验证什么

1. **不启动任何本地服务**：也能点对号（请求 `jsonplaceholder.typicode.com`）。
2. **可选**：你已跑起 `tool-lab-express-api-minimal` 时，可把 B 章请求发往 `localhost:3000`。

## 前置条件

- 安装 [Postman Desktop](https://www.postman.com/downloads/)（或兼容 Collection v2.1 的替代品）。
- 不需要账号即可跑本文件的「公有只读」请求。

## 使用步骤（Postman）

1. `导入` → 选择 `postman_collection.json`。
2. 打开 **Variables**（Collection / Environment 均可）；默认不用改：
   - `demoBase = https://jsonplaceholder.typicode.com`
   - `expressBase = http://localhost:3000`
3. 展开 **A. 公有只读 Demo**，点 **Send**。应返回 JSON（含 `title`、`body` 等字段）。
4. （可选）先启动 Stage 3 的 Express，再跑 **B** 章里的 `/health`、`/hello`。

## 失败后怎么办

| 现象 | 可能原因 |
| --- | --- |
| DNS / `Could not get response` | 本机断网或对 `jsonplaceholder.typicode.com` 不可达 |
| B 章全失败、`ECONNREFUSED` | 未启动 Stage 3 服务，或 `expressBase`/端口不一致 |
| 变量未替换 | Collection 未被选中或未导入到 Workspace |

## 与本套其它实验的关系

- **Stage 3** `tool-lab-express-api-minimal`：给 B 章提供后端。
- **同 Stage 4** `tool-lab-openapi-spec-minimal`：`openapi.yaml` 描述「契约」，Postman Collection 往往是「可点选执行手册」的补充。

笔记：[`docs/NOTES.md`](./docs/NOTES.md)。
