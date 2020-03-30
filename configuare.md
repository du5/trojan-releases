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

### 完整配置文件示例

```text
{
    "node_id": "203",
    "node_class":"1",
    "node_group":"1",
    "run_type": "server",
    "local_addr": "0.0.0.0",
    "local_port": 443,
    "remote_addr": "127.0.0.1",
    "remote_port": 80,
    "password": [
        "password1",
        "password2"
    ],
    "log_level": 1,
    "ssl": {
        "cert": "/path/to/certificate.crt",
        "key": "/path/to/private.key",
        "key_password": "",
        "cipher": "ECDHE-ECDSA-AES128-GCM-SHA256:ECDHE-RSA-AES128-GCM-SHA256:ECDHE-ECDSA-AES256-GCM-SHA384:ECDHE-RSA-AES256-GCM-SHA384:ECDHE-ECDSA-CHACHA20-POLY1305:ECDHE-RSA-CHACHA20-POLY1305:DHE-RSA-AES128-GCM-SHA256:DHE-RSA-AES256-GCM-SHA384",
        "cipher_tls13": "TLS_AES_128_GCM_SHA256:TLS_CHACHA20_POLY1305_SHA256:TLS_AES_256_GCM_SHA384",
        "prefer_server_cipher": true,
        "alpn": [
            "http/1.1"
        ],
        "alpn_port_override": {
            "h2": 81
        },
        "reuse_session": true,
        "session_ticket": false,
        "session_timeout": 600,
        "plain_http_response": "",
        "curves": "",
        "dhparam": ""
    },
    "tcp": {
        "prefer_ipv4": false,
        "no_delay": true,
        "keep_alive": true,
        "reuse_port": false,
        "fast_open": false,
        "fast_open_qlen": 20
    },
    "mysql": {
        "enabled": false,
        "server_addr": "127.0.0.1",
        "server_port": 3306,
        "database": "trojan",
        "username": "trojan",
        "password": "",
        "cafile": ""
    }
}

```

