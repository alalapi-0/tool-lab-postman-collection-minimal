# 运行记录

## 本机环境

- 操作系统：macOS 26.3.1（darwin）
- Postman 版本（About）：_（请在你本机导入后填写）_
- Node：`v25.6.1`（本仓库 A 章不强制使用）
- Python：3.14.3（仅用于机器侧 JSON 自检）
- 是否需要账号：否（本实验公有请求不需要）
- 是否需要 API Key：否

## 运行步骤（记录你实际做过的）

```
python3 -c "import json; json.load(open('postman_collection.json'))"
curl -s "https://jsonplaceholder.typicode.com/posts/1" | head -c 200
# Postman GUI：导入 postman_collection.json → 跑 A 章；（可选）启 Stage3 Express 后跑 B 章
```

## 运行结果

（2026-05-19）`postman_collection.json` 可被标准库 `json` 解析；`curl` 成功返回 `posts/1` JSON 片段。**A/B 章在 Postman 内点 Send** 请你在本机 GUI 完成并补记状态码与响应摘要。

## 报错记录

无（机器侧 JSON + curl 自检）。

## 我是否真正理解了这个工具的一句话总结

Postman Collection 把「重复的 HTTP 调用」固化成可变量、可分享的请求树，让调试与协作不再依赖临时记 URL。
