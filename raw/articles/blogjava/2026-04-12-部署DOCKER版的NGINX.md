---
title: 部署DOCKER版的NGINX
date: 2026-04-12
source: http://www.blogjava.net/paulwong/archive/2024/06/19/451449.html
---

# 部署DOCKER版的NGINX

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/06/19/451449.html
**发布时间**: 2026-04-12

部署DOCKER版的NGINX
使用docker compose搞配置方便，配置放在配置文件中，比放在启动命令直观。
docker-compose.yaml


version: '3.8'
services:

  nginx-web: #这里注意名称随便起，但要保证在docker环境中维一，否则docker compose down时，会被全局down掉
    volumes:
      - /opt/tool/nginx/data/html:/usr/share/nginx/html:ro #配置html文件在宿主机上
      - /opt/tool/nginx/data/conf/nginx.conf:/etc/nginx/nginx.conf:ro #配置配置文件在宿主机上
      - /opt/tool/nginx/data/conf/conf.d/default-web.conf:/etc/nginx/conf.d/default.conf:ro #配置配置文件在宿主机上
      - /opt/tool/nginx/data/conf/.htpasswd:/etc/nginx/.htpasswd:ro #配置登录NGINX时要用到的用户名和密码文件
      - /etc/localtime:/etc/localtime:ro #配置NGINX上的时钟与宿主机相同
      - /opt/tool/nginx/data/log/access.log:/var/log/nginx/access.log #配置ACCESS文件在宿主机上
      - /opt/tool/nginx/data/log/error.log:/var/log/nginx/error.log #配置ERROR文件在宿主机上
    container_name: nginx-web #容器名称，全局维一
    ports:
      - \