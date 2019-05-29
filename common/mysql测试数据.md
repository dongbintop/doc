#### 创建数据库表

```mysql
CREATE TABLE `demo` (
  `id` bigint(20) unsigned NOT NULL,
  `name` varchar(100) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=Innodb DEFAULT CHARSET=utf8
```

#### 创建存储过程

```mysql
CREATE DEFINER=`root`@`localhost` PROCEDURE `generate`(IN num INT)
BEGIN   
	DECLARE id int UNSIGNED;
	set id=1;
	DELETE from demo;
	WHILE id <= num DO
		INSERT into demo VALUES (id,UUID());
		set id = id + 1;
	END WHILE;
END
```

