---
title: AI微调框架AXOLOTL安装
date: 2025-01-12
source: http://www.blogjava.net/paulwong/archive/2025/01/12/451548.html
---

# AI微调框架AXOLOTL安装

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/12/451548.html
**发布时间**: 2025-01-12

AI微调框架AXOLOTL安装
1. N卡驱动和toolkit安装
https://developer.nvidia.com/cuda-downloads?target_os=Linux&target_arch=x86_64&Distribution=WSL-Ubuntu&target_version=2.0&target_type=runfile_local
 
2. python和mini-conda安装
基本是要下载安装包安装,
python下载地址：https://repo.huaweicloud.com/python/3.12.8/
mini-conda下载地址：https://mirrors.tuna.tsinghua.edu.cn/anaconda/miniconda/
conda清华资源：https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/




3. 新建一个conda环境
conda create -n axolotl python=3.12


4. cuda版本的pytorch安装
https://download.pytorch.org/whl/cu124/torch-2.5.0%2Bcu124-cp311-cp311-linux_x86_64.whl#sha256=5e3f4a7ba812517c2c1659857b5195f287a288fbd050a5abf9311e03dbe1a28b

如想安装其他版本, 可从以下网址查找:
https://download.pytorch.org/whl/torch



5. git clone https://github.com/axolotl-ai-cloud/axolotl, cd到根目录, 运行
pip3 install --no-build-isolation axolotl[flash-attn,deepspeed]











posted on 2025-01-12 16:37 paulwong 阅读(99) 评论(0)  编辑  收藏 所属分类: AI-FINE-TUNNING