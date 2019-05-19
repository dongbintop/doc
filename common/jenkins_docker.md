```shell
jenkins 安装步骤

1、mkdir your_home
2、chown -R 1000 your_home
3、docker run -d -p 8080:8080 -p 50000:50000 -v your_home:/var/jenkins_home --name jenkins jenkins/jenkins

```

