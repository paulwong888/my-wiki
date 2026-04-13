---
title: 微调LLAMA3大模型(1) - 使用LLAMA FACTORY微调LLAMA3大模型
date: 2026-04-12
source: http://www.blogjava.net/paulwong/archive/2024/07/08/451463.html
---

# 微调LLAMA3大模型(1) - 使用LLAMA FACTORY微调LLAMA3大模型

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/07/08/451463.html
**发布时间**: 2026-04-12

微调LLAMA3大模型(1) - 使用LLAMA FACTORY微调LLAMA3大模型
对于象META的开源大模型，如llama3，由于都是用通用数据进行预训练，对想使用其模型的公司来说，可能会不适用，因为这大模型对公司的数据不熟悉，因此引入微调(Fine-Tunning)。
通过喂给大模型大量数据，1万条起步，使得大模型也能对公司的数据熟悉，进而用于各种对话场景。
1.克隆并安装LLAMA FACTORY库，install-llamafactory.sh
BIN_PATH=$(cd `dirname $0`; pwd)
cd $BIN_PATH/../
pwd
git clone --depth 1 https://github.com/hiyouga/LLaMA-Factory.git
cd LLaMA-Factory
pip install -e \