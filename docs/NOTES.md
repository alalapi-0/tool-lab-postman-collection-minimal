# 学习笔记（NOTES）

## Collection v2.1 是啥

导入 Postman 的 JSON `schema` 指向 `collection/v2.1`，这是目前桌面端兼容性最好的一条主干。

## 为什么要拆「公有 Demo」与「本地 Express」两套

学习目标分成两层：先会用 Postman UI 与变量，再学与真实本机后端联调。断网或对 Stage 3 不熟时仍可完成前半。

## 「Environment」vs「Collection Variables」

本仓库仅用 **Collection Variables** 降低心智负担；团队在真实项目里常把密钥放到 **Environment**，避免误提交入库。
