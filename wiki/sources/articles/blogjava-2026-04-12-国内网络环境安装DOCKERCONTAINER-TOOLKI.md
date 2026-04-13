---
title: 国内网络环境安装DOCKER＋CONTAINER TOOLKIT
type: source
category: article
created: 2026-04-12
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2024/08/15/451479.html
author: paulwong
tags: ['ai', 'docker']
---

# 国内网络环境安装DOCKER＋CONTAINER TOOLKIT

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/08/15/451479.html  
**发布时间**: 2026-04-12

## 摘要

# 国内网络环境安装DOCKER＋CONTAINER TOOLKIT

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/08/15/451479.html
**发布时间**: 2026-04-12

国内网络环境安装DOCKER＋CONTAINER TOOLKIT
操作系统为centos 9.
先安装驱动程序
在https://www.nvidia.cn/drivers/lookup/ 中查找对应的驱动程序下载到本地，再运行
#切换成文字界面
sudo systemctl set-default multi-user.target
sudo reboot

sh NVIDIA-Linux-x86_64-550.107.02.run

#切换成图形界面
sudo systemctl set-default graphical.target
sudo reboot
安装docker:
yum remove docker \\
                  docker-client \\
                ...

## 原文内容

# 国内网络环境安装DOCKER＋CONTAINER TOOLKIT

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/08/15/451479.html
**发布时间**: 2026-04-12

国内网络环境安装DOCKER＋CONTAINER TOOLKIT
操作系统为centos 9.
先安装驱动程序
在https://www.nvidia.cn/drivers/lookup/ 中查找对应的驱动程序下载到本地，再运行
#切换成文字界面
sudo systemctl set-default multi-user.target
sudo reboot

sh NVIDIA-Linux-x86_64-550.107.02.run

#切换成图形界面
sudo systemctl set-default graphical.target
sudo reboot
安装docker:
yum remove docker \\
                  docker-client \\
                  docker-client-latest \\
                  docker-common \\
                  docker-latest \\
                  docker-latest-logrotate \\
                  docker-logrotate \\
                  docker-engine

yum install -y yum-utils
yum-config-manager --add-repo https://mirrors.tuna.tsinghua.edu.cn/docker-ce/linux/centos/docker-ce.repo
sed -i 's+https://download.docker.com+https://mirrors.tuna.tsinghua.edu.cn/docker-ce+' /etc/yum.repos.d/docker-ce.repo

yum install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

sudo nvidia-ctk runtime configure --runtime=docker
改镜像地址：
[paul@paul-pc ~]$ cat /etc/docker/daemon.json
{  
    \

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
