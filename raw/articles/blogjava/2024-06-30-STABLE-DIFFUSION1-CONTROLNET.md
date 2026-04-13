---
title: STABLE DIFFUSION(1) - CONTROLNET
date: 2024-06-30
source: http://www.blogjava.net/paulwong/archive/2024/06/30/451460.html
---

# STABLE DIFFUSION(1) - CONTROLNET

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/06/30/451460.html
**发布时间**: 2024-06-30

STABLE DIFFUSION(1) - CONTROLNET
CONTROLNET是STABLE DIFFUSION中的一个插件，允许用户指定某张图片上的特征，然后将这些特征应用到新生成的图片上。
特征可以是图片上某人物的姿势，景深等。
其中一些实用的CONTROL TYPE：
1，LINER
STABLE DIFFUSION实现过程，其实就是先生成样图的线稿图，然后再上色。
2，TITLE
STABLE DIFFUSION会根据提供图片的骨架，再生成新的内容
3，SCRIBBLE
通常用于产品工业设计，先画出线稿，STABLE DIFFUSION会根据线稿，再根据提示词内容生成图片

posted on 2024-06-30 00:38 paulwong 阅读(65) 评论(0)  编辑  收藏 所属分类: AI-STABLE-DIFFUSION