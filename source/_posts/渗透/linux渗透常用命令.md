---
title: linux渗透常用命令
categories:
  - linux
  - 渗透
date: 2024-12-18 21:53:46
---

# 系统用法

```sh
echo $0								## 切换sh
systemctl status firewalld.service 	## 查看防火墙服务
cat /etc/passwd | shadow			## 查看用户
history -c							## 清除bash历史记录
systemctl --type==service			## 查看系统所有服务
uname								## 查看系统版本
```

# 网卡设置

- 开启/关闭网卡

```sh
ifconfig eth0 down					## 关闭网卡
ifconfig eth0 up					## 开启网卡
```

# 配置系统代理

## 开启代理

- 创建 proxy_on.sh文件

```sh
touch proxy_on.sh
```

- 开启代理配置

```sh
#!/bin/bash
gsettings set org.gnome.system.proxy mode 'manual'
gsettings set org.gnome.system.proxy.http host '192.168.2.107'
gsettings set org.gnome.system.proxy.http port 10809
gsettings set org.gnome.system.proxy.https host '192.168.2.107'
gsettings set org.gnome.system.proxy.https port 10809
echo "系统代理已开启"
```

## 关闭代理

- 11 1docker version      ## 查看版本2docker info         ## 详细信息3docker -h           ## 帮助文档4docker images       ## 查看所有镜像5docker pull 镜像名:{tar}       ## 下载镜像6docker ps           ## 查看正在运行的镜像7docker ps -a        ## 查看所有正在运行的容器包括以前运行的8docker ps -n 3      ## 查看前3个运行的容器9docker ps -l        ## 查看上1个运行的容器10docker start 容器名称11docker stop 容器名称sh

```sh
touch proxy_off.sh
```

- 关闭代理配置

```sh
#!/bin/bash
gsettings set org.gnome.system.proxy mode 'none'
echo "系统代理已关闭"
```

# 更新软件仓库

```sh
sudo apt-get update
```
