---
title: GITHUB无法访问的办法
type: source
category: article
created: 2025-01-05
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2025/01/05/451538.html
author: paulwong
tags: ['blogjava']
---

# GITHUB无法访问的办法

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/05/451538.html  
**发布时间**: 2025-01-05

## 摘要

# GITHUB无法访问的办法

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/05/451538.html
**发布时间**: 2025-01-05

GITHUB无法访问的办法
浏览器打开https://www.ipaddress.com/website/www.github.com/, 输入www.github.com, 得到相应的ip, 本地clone以ip的方式, 但如果要访问页面, 需改本地的hosts文件:


# /etc/hosts
140.82.112.4    www.github.com









posted on 2025-01-05 12:08 paulwong 阅读(100) 评论(0)  编辑  收藏 所属分类: GIT...

## 原文内容

# GITHUB无法访问的办法

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/05/451538.html
**发布时间**: 2025-01-05

GITHUB无法访问的办法
浏览器打开https://www.ipaddress.com/website/www.github.com/, 输入www.github.com, 得到相应的ip, 本地clone以ip的方式, 但如果要访问页面, 需改本地的hosts文件:


# /etc/hosts
140.82.112.4    www.github.com









posted on 2025-01-05 12:08 paulwong 阅读(100) 评论(0)  编辑  收藏 所属分类: GIT

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
