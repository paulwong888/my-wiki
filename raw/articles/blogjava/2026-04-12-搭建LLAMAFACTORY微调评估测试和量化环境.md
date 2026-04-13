---
title: 搭建LLAMAFACTORY微调、评估、测试和量化环境
date: 2026-04-12
source: http://www.blogjava.net/paulwong/archive/2025/01/16/451558.html
---

# 搭建LLAMAFACTORY微调、评估、测试和量化环境

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/16/451558.html
**发布时间**: 2026-04-12

搭建LLAMAFACTORY微调、评估、测试和量化环境
0. 配置环境变量
HF_ENDPOINT=https://hf-mirror.com
HF_HOME=/root/autodl-tmp/paul/tools/huggingface


1. 本机安装python 3.10, 并设置软件源
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
pip config set global.index-url https://mirrors.huaweicloud.com/repository/pypi/simple


2. 安装miniconda
https://juejin.cn/post/7078965942968909854



3. 新建一个环境, 并激活
conda create -n quantization python=3.12


2. 本机安装pytorch2.5.1+cuda12.4
pip3 install torch torchvision torchaudio
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu124


3. clone llamafactory源码
git clone https://github.com/hiyouga/LLaMA-Factory


4. llamafactory本地安装依赖
pip install -e .
pip install -e .[\