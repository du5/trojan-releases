---
description: Welcome Page
---

# 欢迎

此处是 trojan 多用户后端的 wiki 页面

如果需要授权, 请 Telegram 联系 [@elrepo](https://t.me/elrepo) 。

## 特性

* [x] 审计拦截上报
* [x] 在线IP上报
* [x] 支持倍率计算
* [x] 机器负载上报
* [x] Docker 一键部署
* [x] WEBAPI 对接
* [ ] 节点限速\(计划中
* [ ] 用户限速\(计划中

## 优化

> 相比原版 trojan 我们优化的部分

| 修改后 | 原版 |
| :--- | :--- |
| 用户授权缓存并一分钟无阻塞更新 | 无缓存，同一用户不同请求均验证，服务器与数据库校验过慢 |
| 流量数据缓存并一分钟上传一次流量 | 无缓存，每个请求结束后都上传一次流量 |
| 审计规则支持并三十分钟刷新一次审计（被拦截的审计一分钟上传一次 | 无支持 |
| 上传当前在线用户数量 | 无支持 |
| 可查看累计链接用户数量 | 无支持 |
| WEBAPI对接 | 无支持 |

## 演示站点

地址: [https://demo.trojan.today/auth/login](https://demo.trojan.today/auth/login)

