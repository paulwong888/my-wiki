---
title: 微调LLAMA3大模型(2) - 使用OLLAMA搭建CHATBOT
type: source
category: article
created: 2026-04-12
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2024/07/08/451464.html
author: paulwong
tags: ['ai']
---

# 微调LLAMA3大模型(2) - 使用OLLAMA搭建CHATBOT

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/07/08/451464.html  
**发布时间**: 2026-04-12

## 摘要

# 微调LLAMA3大模型(2) - 使用OLLAMA搭建CHATBOT

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/07/08/451464.html
**发布时间**: 2026-04-12

微调LLAMA3大模型(2) - 使用OLLAMA搭建CHATBOT
上篇已经合并出了训练好的大模型，现在要搭建起一套CHATBOT，使得这套大模型能有一个WEBUI用起来。
1.设置环境变量，ollama的模型保存路径，/etc/profile
export OLLAMA_MODELS=/root/autodl-tmp/models/ollama
2.克隆ollama代码
curl -fsSL https://ollama.com/install.sh | sh
3.启动ollama
ollama serve
4.建立ollama镜像的配置文件，Modelfile
# set the base model
FROM /root/.ollama/llamafactory-export/saves/llama3-8b/lor...

## 原文内容

# 微调LLAMA3大模型(2) - 使用OLLAMA搭建CHATBOT

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/07/08/451464.html
**发布时间**: 2026-04-12

微调LLAMA3大模型(2) - 使用OLLAMA搭建CHATBOT
上篇已经合并出了训练好的大模型，现在要搭建起一套CHATBOT，使得这套大模型能有一个WEBUI用起来。
1.设置环境变量，ollama的模型保存路径，/etc/profile
export OLLAMA_MODELS=/root/autodl-tmp/models/ollama
2.克隆ollama代码
curl -fsSL https://ollama.com/install.sh | sh
3.启动ollama
ollama serve
4.建立ollama镜像的配置文件，Modelfile
# set the base model
FROM /root/.ollama/llamafactory-export/saves/llama3-8b/lora/docker-commnad-nlp/export

# set custom parameter values
PARAMETER temperature 1
PARAMETER num_keep 24
PARAMETER stop <|start_header_id|>
PARAMETER stop <|end_header_id|>
PARAMETER stop <|eot_id|>
PARAMETER stop <|reserved_special_token

# set the model template
TEMPLATE \

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
