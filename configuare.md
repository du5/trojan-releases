---
description: 此页面仅介绍本项目需要的配置项目
---

# 对后端进行配置

## 配置项目

| 配置名称 | 简介 |
| :--- | :--- |
| node\_id | 必填，节点 ID，错误的 ID 可能导致节点流量无法结算 |
| node\_class | 必填，允许连接的用户等级 |
| node\_group | 必填，允许连接的用户分组 |
| run\_type | 固定 `server` |
| mysql.enabled | 固定 `true` |
| mysql.server\_addr | 必填，面板数据库 IP 地址 |
| mysql.server\_port | 必填，数据库端口 |
| mysql.database | 必填，数据库名称 |
| mysql.username | 必填，数据库用户名 |
| mysql.password | 选填，数据库密码 |
| mysql.cafile | 选填，数据库连接密钥 |

