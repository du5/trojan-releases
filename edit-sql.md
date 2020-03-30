# 额外SQL修改

```text
DROP TABLE IF EXISTS
    `user_traffic_log_trojan`;
CREATE TABLE IF NOT EXISTS `user_traffic_log_trojan`(
    `id` BIGINT NOT NULL AUTO_INCREMENT,
    `nodeid` INT NOT NULL COMMENT '节点',
    `userid` INT NOT NULL COMMENT '用户ID',
    `d` INT NOT NULL COMMENT '下载',
    `u` INT NOT NULL COMMENT '上传',
    `time` BIGINT NOT NULL,
    `status` INT NOT NULL COMMENT '流量是否被统计',
    PRIMARY KEY(`id`)
) ENGINE = InnoDB DEFAULT CHARSET = utf8mb4 COLLATE = utf8mb4_general_ci;
```

```text
ALTER TABLE
    `user` ADD `password` TEXT NULL DEFAULT NULL COMMENT 'trojan 密码' AFTER `passwd`;
```



