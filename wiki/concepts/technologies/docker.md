---
title: Docker
type: concept
category: technology
created: 2026-04-12
updated: 2026-04-12
tags:
  - container
  - devops
  - virtualization
  - linux
related:
  - "[[concepts/technologies/docker]]"
  - "[[sources/articles/blogjava-2025-06-21-最全-DOCKER-神器集结让你的服务器瞬间起飞]]"
---

# Docker

## 定义

Docker 是一个**容器化平台**，允许开发者将应用程序及其依赖打包成标准化的容器，实现跨环境的一致部署。

## 核心概念

### 1. 镜像 (Image)
- 只读的模板
- 包含应用程序和运行环境
- 分层存储结构

### 2. 容器 (Container)
- 镜像的运行实例
- 独立的进程空间
- 轻量级虚拟化

### 3. Dockerfile
- 定义镜像构建过程
- 指令：FROM、RUN、COPY、CMD 等

### 4. Docker Compose
- 多容器应用编排
- YAML 配置文件
- 一键启动服务栈

## 常用命令

```bash
# 镜像管理
docker pull <image>
docker build -t <name> .
docker images

# 容器管理
docker run -d -p 80:80 <image>
docker ps
docker stop <container>
docker rm <container>

# 数据卷
docker volume create <name>
docker run -v <volume>:/data <image>
```

## AI 相关应用

- **Ollama**：本地大模型运行
- **Open WebUI**：Web 界面管理
- **vLLM**：高性能推理服务
- **NVIDIA Container Toolkit**：GPU 支持

## 相关资源

- [[sources/articles/blogjava-2024-06-19-部署docker版的nginx]]
- [[sources/articles/blogjava-2026-04-12-部署docker版的人工智能OPEN-WEBUIOLLAMA-NGINX]]
- [[sources/articles/blogjava-2025-06-21-最全Docker神器集结]]
