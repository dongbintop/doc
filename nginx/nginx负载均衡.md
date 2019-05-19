```powershell
    #设定负载均衡的服务器列表
    upstream load_balance_server {
        #weigth参数表示权值，权值越高被分配到的几率越大
        server 192.168.1.111:80   weight=5;
        server 192.168.1.112:80   weight=1;
        server 192.168.1.113:80   weight=6;
    }
    
    location / {
    		proxy_pass  http://load_balance_server
    }
```

