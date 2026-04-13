---
title: STABLE DIFFUSION(1) - 提示词
type: source
category: article
created: 2024-06-29
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2024/06/29/451457.html
author: paulwong
tags: ['stable-diffusion']
---

# STABLE DIFFUSION(1) - 提示词

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/06/29/451457.html  
**发布时间**: 2024-06-29

## 摘要

# STABLE DIFFUSION(1) - 提示词

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/06/29/451457.html
**发布时间**: 2024-06-29

STABLE DIFFUSION(1) - 提示词
提示如果不被模型认识，则不会起效果。
如果提示词太多，则排在后面的提示词会被忽略。
越靠前的词，越会被注意。
同类型的提示词之间会被污染。
反向提示词写几个就足够，如nsfw,low quality, lowres，写多反而会被忽略
一层小括号里面的提示词会加权重成1.1倍，两层则是1.21倍。
一层中括号里面的提示词会加权重成0.9倍，两层则是0.81倍。
[super man|iron man]则生成的主题会融合两种特征。

posted on 2024-06-29 23:18 paulwong 阅读(96) 评论(0)  编辑  收藏 所属分类: AI-STABLE-DIFFUSION...

## 原文内容

# STABLE DIFFUSION(1) - 提示词

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/06/29/451457.html
**发布时间**: 2024-06-29

STABLE DIFFUSION(1) - 提示词
提示如果不被模型认识，则不会起效果。
如果提示词太多，则排在后面的提示词会被忽略。
越靠前的词，越会被注意。
同类型的提示词之间会被污染。
反向提示词写几个就足够，如nsfw,low quality, lowres，写多反而会被忽略
一层小括号里面的提示词会加权重成1.1倍，两层则是1.21倍。
一层中括号里面的提示词会加权重成0.9倍，两层则是0.81倍。
[super man|iron man]则生成的主题会融合两种特征。

posted on 2024-06-29 23:18 paulwong 阅读(96) 评论(0)  编辑  收藏 所属分类: AI-STABLE-DIFFUSION

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
