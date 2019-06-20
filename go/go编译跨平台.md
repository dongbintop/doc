###### go 编译跨平台 编译



```shell
64位系统

linux
GOOS=linux GOARCH=amd64 go build -ldflags "-w -s" -o web
windows
GOOS=windows GOARCH=amd64 go build -ldflags "-w -s" -o web
mac
GOOS=darwin GOARCH=amd64 go build -ldflags "-w -s" -o web

32位系统

linux
GOOS=linux GOARCH=amd32 go build -ldflags "-w -s" -o web
windows
GOOS=windows GOARCH=amd32 go build -ldflags "-w -s" -o web
mac
GOOS=darwin GOARCH=amd32 go build -ldflags "-w -s" -o web
```



