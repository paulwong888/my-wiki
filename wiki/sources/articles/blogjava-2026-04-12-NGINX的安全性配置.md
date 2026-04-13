---
title: NGINX的安全性配置
type: source
category: article
created: 2026-04-12
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2024/06/19/451448.html
author: paulwong
tags: ['blogjava']
---

# NGINX的安全性配置

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/06/19/451448.html  
**发布时间**: 2026-04-12

## 摘要

# NGINX的安全性配置

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/06/19/451448.html
**发布时间**: 2026-04-12

NGINX的安全性配置
最近将一台HTTP服务器暴露于仅见，随即引来大量黑客的光顾，其实也就是发各种HTTP请求，以获取一个输入，输出界面，在输入界面输入SHELL命令，在输出界面观看结果，也就是说不用去到电脑前，用登录用户名和密码这种方法来登录，再跑各种命令。
日志显示有下面这些操作：
185.191.127.212 - - [19/Jun/2024:21:10:22 +0800] \...

## 原文内容

# NGINX的安全性配置

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/06/19/451448.html
**发布时间**: 2026-04-12

NGINX的安全性配置
最近将一台HTTP服务器暴露于仅见，随即引来大量黑客的光顾，其实也就是发各种HTTP请求，以获取一个输入，输出界面，在输入界面输入SHELL命令，在输出界面观看结果，也就是说不用去到电脑前，用登录用户名和密码这种方法来登录，再跑各种命令。
日志显示有下面这些操作：
185.191.127.212 - - [19/Jun/2024:21:10:22 +0800] \

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
