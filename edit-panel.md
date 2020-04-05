---
description: 使用此项目前需要修改SSP面板的地方
---

# 面板的修改

Anankke 库已经完美兼容 MYSQL/WEBAPI [https://github.com/Anankke/SSPanel-Uim](https://github.com/Anankke/SSPanel-Uim)

Malio 库 PR 已经在本地了

{% hint style="warning" %}
如果使用面板以上未提及修改内容请自行比对，远程协助比对安装请额外支付 30 USDT
{% endhint %}

## 节点编辑

Server 格式: google.com;port=1443\|host=baidu.com

> google.com 改为你的真是机器解析IP或域名
>
> port 改为你后端开启的端口
>
> baidu.com 改为你的 trojan 服务器证书 peer/sni 证书名

## 计划任务

```bash
*/1 * * * * php xcat checkjob > /dev/null
```

