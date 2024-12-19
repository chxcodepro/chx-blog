---
title: Windows渗透常用命令
categories:
  - windows
  - 渗透
date: 2024-12-18 21:53:34
---

## windows

- 存放密码的目录

```bat
C:\Windows\System32\config\sam
```

- 存放host的目录

```bat
C:\Windows\System32\drivers\etc\hosts
```

- 查看端口8080

```bat
netstat -ano | findstr :8080
```

- 隐藏文件

```bat
attrib +s +h  xxx.txt ## 系统保护并且隐藏的文件
```

- 注销用户

```
logoff
```

## Docker命令

```sh
docker version		## 查看版本
docker info			## 详细信息
docker -h			## 帮助文档
docker images		## 查看所有镜像
docker pull 镜像名:{tar}		## 下载镜像
docker ps			## 查看正在运行的镜像
docker ps -a		## 查看所有正在运行的容器包括以前运行的
docker ps -n 3		## 查看前3个运行的容器
docker ps -l		## 查看上1个运行的容器
docker start 容器名称
docker stop 容器名称
```

