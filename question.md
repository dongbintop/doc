namespace delete is not work

kubectl patch crd clusters.rook.io -p '{"metadata":{"finalizers": []}}' --type=merge



![image-20190617111403052](/Users/dongbin/Library/Application Support/typora-user-images/image-20190617111403052.png)





alter table dbrds_snapshot add column engine      varchar(64) DEFAULT NULL

alter table dbrds_snapshot add column version       varchar(255) DEFAULT NULL COMMENT '数据库版本'