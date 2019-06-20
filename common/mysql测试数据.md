

```powershell
#!/bin/bash

set -ex;
HOST=$1
PROT=$2
USER=$3
PASSWORD=$4
for ((i=1; i<=10; i++))
do
DATABSENAME=dongbin$i

#create database
echo "Start create database $DATABSENAME"
mysql -h$HOST -P$PROT -u$USER -p$PASSWORD <<EOF 2>/dev/null
CREATE DATABASE $DATABSENAME;
USE $DATABSENAME;
CREATE TABLE demo (
  id bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  name varchar(100) NOT NULL,
  PRIMARY KEY (id)
) ENGINE=Innodb DEFAULT CHARSET=utf8;
INSERT into demo(name) value("dongbin");
DROP PROCEDURE IF EXISTS generate;
delimiter ;;
CREATE PROCEDURE generate(IN num INT)
BEGIN   
	DECLARE id int UNSIGNED;
	set id=1;
	WHILE id <= num DO
		INSERT into demo(name) select name from demo;
		set id = id + 1;
	END WHILE;
END;
;;
delimiter ;
call generate(24)
EOF
echo "End create database $DATABSENAME"
done
```

