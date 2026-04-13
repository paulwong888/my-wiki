---
title: 部署DOCKER版的人工智能OPEN-WEBUI+OLLAMA+NGINX
date: 2026-04-12
source: http://www.blogjava.net/paulwong/archive/2024/06/19/451450.html
---

# 部署DOCKER版的人工智能OPEN-WEBUI+OLLAMA+NGINX

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/06/19/451450.html
**发布时间**: 2026-04-12

部署DOCKER版的人工智能OPEN-WEBUI+OLLAMA+NGINX
一键部署人工智能中的OPEN-WEBUI,OLLAMA, NGINX，也就对类似OPEN-AI的对话机器人
docker-compose.yaml
services:

  # ollama:
  #   deploy:
  #     resources:
  #       reservations:
  #         devices:
  #           - driver: nvidia
  #             count: all
  #             capabilities:
  #               - gpu  #使用GPU加速
  #   volumes:
  #     - ollama-volume:/root/.ollama #配置OLLAMA的配置数据文件在宿主机
  #     - /etc/localtime:/etc/localtime:ro
  #   container_name: ollama
  #   image: ollama/ollama
  #   restart: unless-stopped
  #   networks:
  #     - isolated #使用DOCKER的隔离网络
  #     - internet

  vllm:
    container_name: vllm
    image: vllm/vllm-openai:latest
    # ipc: host
    volumes:
      - ${HUGGINGFACE_MODELS_DIR}:/models
      - /etc/localtime:/etc/localtime:ro
    command: >
      --model /models/models--unsloth--llama-3-8b-Instruct-lawdata
      --served-model-name llama-3-8b-Instruct-lawdata
      --gpu-memory-utilization 0.90
      --max_model_len 1072
      --quantization bitsandbytes
      --load_format bitsandbytes
    ports:
      - \