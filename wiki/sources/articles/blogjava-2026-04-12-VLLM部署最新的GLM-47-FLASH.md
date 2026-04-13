---
title: VLLM部署最新的GLM-4.7-FLASH
type: source
category: article
created: 2026-04-12
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2026/02/02/451735.html
author: paulwong
tags: ['blogjava']
---

# VLLM部署最新的GLM-4.7-FLASH

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/02/02/451735.html  
**发布时间**: 2026-04-12

## 摘要

# VLLM部署最新的GLM-4.7-FLASH

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/02/02/451735.html
**发布时间**: 2026-04-12

VLLM部署最新的GLM-4.7-FLASH
目前要部署成功，主要是各种组件的版本要最新
torch: 2.9.1+cu130
vllm: nightly
transformers: 5.0.0rc3


安装命令
```bash
conda create -n vllm-glm47 python=3.12 -y
conda activate vllm-glm47
pip install torch==2.9.1+cu130 --index-url https://download.pytorch.org/whl/cu130
pip list
pip install -U vllm --pre --extra-index-url https://wheels.vllm.ai/nightly/cu130
pip list
pip install -U transf...
```

## 原文内容

# VLLM部署最新的GLM-4.7-FLASH

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/02/02/451735.html
**发布时间**: 2026-04-12

VLLM部署最新的GLM-4.7-FLASH
目前要部署成功，主要是各种组件的版本要最新
torch: 2.9.1+cu130
vllm: nightly
transformers: 5.0.0rc3


安装命令
```bash
conda create -n vllm-glm47 python=3.12 -y
conda activate vllm-glm47
pip install torch==2.9.1+cu130 --index-url https://download.pytorch.org/whl/cu130
pip list
pip install -U vllm --pre --extra-index-url https://wheels.vllm.ai/nightly/cu130
pip list
pip install -U transformers==5.0.0rc3
```


启动命令_start-vllm.sh
```bash
BIN_PATH=$(cd `dirname $0`; pwd)
cd $BIN_PATH

#source /home/dgx/ai/miniconda3/bin/activate
#conda activate vllm-nightly

#uv pip install -U vllm --extra-index-url https://wheels.vllm.ai/nightly/cu130 --extra-index-url https://download.pytorch.org/whl/cu130

export CUDA_HOME=/usr/local/cuda
export TRITON_PTXAS_PATH=\
```

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
