---
title: 安装CUDA版本的PYTORCH
type: source
category: article
created: 2025-01-12
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2025/01/12/451546.html
author: paulwong
tags: ['blogjava']
---

# 安装CUDA版本的PYTORCH

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/12/451546.html  
**发布时间**: 2025-01-12

## 摘要

安装CUDA版本的PYTORCH

先下载cuda版本的pytorch的整个打包文件:
- https://download.pytorch.org/whl/cu124/torch-2.5.1%2Bcu124-cp312-cp312-linux_x86_64.whl
- https://mirrors.huaweicloud.com/artifactory/pypi-public/simple/torch/

安装命令:

```bash
pip install torch-2.5.1+cu124-cp312-cp312-linux_x86_64.whl
```

验证:

```python
import torch
torch.__version__
```

## 原文内容

安装CUDA版本的PYTORCH

先下载cuda版本的pytorch的整个打包文件:
- https://download.pytorch.org/whl/cu124/torch-2.5.1%2Bcu124-cp312-cp312-linux_x86_64.whl
- https://mirrors.huaweicloud.com/artifactory/pypi-public/simple/torch/

安装命令:

```bash
pip install torch-2.5.1+cu124-cp312-cp312-linux_x86_64.whl
```

验证:

```python
import torch
torch.__version__
```

posted on 2025-01-12 11:05 paulwong 阅读(98) 评论(0)  编辑  收藏 所属分类: AI-PYTHON

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
