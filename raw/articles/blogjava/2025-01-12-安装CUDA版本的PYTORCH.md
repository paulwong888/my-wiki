---
title: 安装CUDA版本的PYTORCH
date: 2025-01-12
source: http://www.blogjava.net/paulwong/archive/2025/01/12/451546.html
---

# 安装CUDA版本的PYTORCH

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/12/451546.html
**发布时间**: 2025-01-12

安装CUDA版本的PYTORCH
先下载cuda版本的pytorch的整个打包文件:
https://download.pytorch.org/whl/cu124/torch-2.5.1%2Bcu124-cp312-cp312-linux_x86_64.whl#sha256=bf6484bfe5bc4f92a4a1a1bf553041505e19a911f717065330eb061afe0e14d7

https://mirrors.huaweicloud.com/artifactory/pypi-public/simple/torch/





pip install torch-2.5.1+cu124-cp312-cp312-linux_x86_64.whl


验证:
#python
import torch
torch.__version__

posted on 2025-01-12 11:05 paulwong 阅读(98) 评论(0)  编辑  收藏 所属分类: AI-PYTHON