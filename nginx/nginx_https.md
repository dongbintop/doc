```shell
sudo openssl req -x509 -nodes -days 36500 -newkey rsa:2048 -keyout ssl.key -out ssl.crt

C：Country ，单位所在国家，为两位数的国家缩写，如： CN 就是中国
ST 字段： State/Province ，单位所在州或省
L 字段： Locality ，单位所在城市 / 或县区
O 字段： Organization ，此网站的单位名称;
OU 字段： Organization Unit，下属部门名称;也常常用于显示其他证书相关信息，如证书类型，证书产品名称或身份验证类型或验证内容等;
CN 字段： Common Name ，网站的域名;


```

