# 额外SQL修改

```text
ALTER TABLE `user`
	ADD COLUMN `uuid` TEXT NULL DEFAULT NULL COMMENT 'uuid' AFTER `passwd`; 
```


