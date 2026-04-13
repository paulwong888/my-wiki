---
title: 使用UV安装PYTHON环境
type: source
category: article
created: 2026-04-12
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2026/01/28/451733.html
author: paulwong
tags: ['blogjava']
---

# 使用UV安装PYTHON环境

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/01/28/451733.html  
**发布时间**: 2026-04-12

## 摘要

# 使用UV安装PYTHON环境

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/01/28/451733.html
**发布时间**: 2026-04-12

使用UV安装PYTHON环境


```bash
conda create -n my_ai_env python=3.10 -y
conda activate my_ai_env

#把 uv 请进来（代替普通的 pip）
conda install -c conda-forge uv -y

# 安装 vLLM 或其他重型库
uv pip install vllm --torch-backend auto
```

为什么系统装了 UV 对 CONDA 更有利？
缓存共享：你在 Conda 环境 A 里装过的包，如果环境 B 也要用，uv 会直接从全局缓存里链接过去，0 秒完成安装，且不占双倍硬盘空间。1
不污染环境：通过 uv pip 安装的包，Conda 依然能感知到（通过 conda list 可以看到它们，通常标注为 pypi 来源）。2
极致性能：在处理 vLLM 这...

## 原文内容

# 使用UV安装PYTHON环境

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/01/28/451733.html
**发布时间**: 2026-04-12

使用UV安装PYTHON环境


```bash
conda create -n my_ai_env python=3.10 -y
conda activate my_ai_env

#把 uv 请进来（代替普通的 pip）
conda install -c conda-forge uv -y

# 安装 vLLM 或其他重型库
uv pip install vllm --torch-backend auto
```

为什么系统装了 UV 对 CONDA 更有利？
缓存共享：你在 Conda 环境 A 里装过的包，如果环境 B 也要用，uv 会直接从全局缓存里链接过去，0 秒完成安装，且不占双倍硬盘空间。1
不污染环境：通过 uv pip 安装的包，Conda 依然能感知到（通过 conda list 可以看到它们，通常标注为 pypi 来源）。2
极致性能：在处理 vLLM 这种动辄几个 GB 的重型依赖时，全局 uv 的并行下载速度能直接跑满你的带宽。

uv 处理 PyTorch 与 CUDA 兼容性问题主要有两种方式：一种是全自动检测（推荐），另一种是手动指定索引（更稳定）。


1. 自动检测（最推荐：--torch-backend auto）
这是 uv 的杀手锏功能。当你使用以下命令时：
```bash
uv pip install torch --torch-backend auto
```
请谨慎使用此类代码。

原理：uv 会自动扫描你的本地环境（通过 nvidia-smi 或驱动版本），检测当前显卡支持的最高 CUDA 版本。

动作：它会自动从 PyTorch 的官方仓库（如 download.pytorch.org）匹配并下载对应的构建版本（如 +cu121 或 +cu124），无需你手动查表。


2. 手动指定官方索引（针对特定版本需求）
如果你需要安装特定版本的 CUDA（例如系统驱动较老），可以使用 --index-url：

```bash
# 安装适配 CUDA 12.1 的版本
uv pip install torch --index-url https://download.pytorch.org/whl/cu121
```
请谨慎使用此类代码。

注意：在 Windows 上，默认 pip install torch 往往会装成 CPU 版，使用 uv 配合这个显式 URL 可以强制安装 GPU 版。


3. 在配置文件中永久锁定（适合项目管理）
如果你在使用 pyproject.toml 管理项目，可以在文件中配置 tool.uv.index，确保团队所有成员装的都是同一个 CUDA 版本：
```
toml
[[tool.uv.index]]
name = \
```

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
