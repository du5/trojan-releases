# 后端的安装

##  获取最后一个后端的版本

从 GitHub Releases 选择你需要的版本，下载二进制文件：

```
https://github.com/du5/trojan-releases/releases
```

守护进程

```text
cat <<EOF > /lib/systemd/system/trojan.service
[Unit]
Description=trojan
After=network.target
[Service]
ExecStart=$PWD/trojan -c $PWD/config.json
WorkingDirectory=$PWD
Restart=always
LimitNOFILE=512000
[Install]
WantedBy=multi-user.target
EOF
```

添加自启动

```text
systemctl enable trojan
```

{% hint style="info" %}
 如果你想通过 Docker 运行可以自己通过二进制文件构建或者使用 [gtary/trojan](https://hub.docker.com/r/gtary/trojan) 库
{% endhint %}

```bash
$ docker run -v /path/config:/config --name=trojan gtary/trojan
```


