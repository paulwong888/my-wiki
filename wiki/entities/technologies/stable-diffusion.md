---
title: Stable Diffusion
type: entity
entity_type: technology
created: 2026-04-12
updated: 2026-04-12
tags:
  - ai
  - image-generation
  - open-source
related:
  - "[[entities/technologies/stable-diffusion]]"
  - "[[sources/articles/blogjava-2024-06-29-STABLE-DIFFUSION1-提示词]]"
---

# Stable Diffusion

## 定义

Stable Diffusion 是一个开源的**文本到图像生成模型**，由 Stability AI 开发。它能够根据文本描述生成高质量的图像，是目前最流行的开源 AI 图像生成工具之一。

## 核心技术

### 1. 扩散模型 (Diffusion Model)
- 通过逐步去噪的过程从随机噪声生成图像
- 训练过程：向图像添加噪声，模型学习如何逆转这个过程

### 2. ControlNet
- 允许用户控制生成图像的特定特征
- 支持的 Control Types：
  - **LineArt**：线稿控制
  - **Depth**：景深控制
  - **OpenPose**：人物姿态控制
  - **Canny**：边缘检测控制
  - **Scribble**：涂鸦控制

### 3. 采样方法 (Sampling Methods)
- Euler、Euler a
- DPM++ 2M、DPM++ 2M Karras
- DDIM、PLMS 等

### 4. 面部修复和高清修复
- 自动修复生成图像中的面部细节
- 通过放大和重绘提高图像分辨率

## 应用场景

- **艺术创作**：插画、概念设计
- **产品设计**：工业设计草图
- **游戏开发**：角色和场景设计
- **建筑可视化**：建筑外观和室内设计

## 相关资源

- [[sources/articles/blogjava-2024-06-29-STABLE-DIFFUSION1-提示词]]
- [[sources/articles/blogjava-2024-06-29-STABLE-DIFFUSION2-采样方法]]
- [[sources/articles/blogjava-2024-06-30-STABLE-DIFFUSION1-CONTROLNET]]
- [[sources/articles/blogjava-2024-06-30-STABLE-DIFFUSION3-面部修复和高清修复]]
