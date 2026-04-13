---
title: WINDOWS中添加端口转发规则
type: source
category: article
created: 2025-01-13
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2025/01/13/451549.html
author: paulwong
tags: ['blogjava']
---

# WINDOWS中添加端口转发规则

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/13/451549.html  
**发布时间**: 2025-01-13

## 摘要

# WINDOWS中添加端口转发规则

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/13/451549.html
**发布时间**: 2025-01-13

WINDOWS中添加端口转发规则
设置端口转发
在 Windows 上，以管理员身份打开 PowerShell，
netsh interface portproxy add v4tov4 listenport=7860 listenaddress=0.0.0.0 connectport=7860 connectaddress=123.45.67.89


在 PowerShell 中使用 netsh interface portproxy 命令设置的端口转发规则是持久性的。这些规则会在系统重启后继续生效，因为它们被存储在 Windows 的注册表中。


删除端口转发规则
如果想删除之前设置的端口转发规则，可以使用以下命令：
netsh interface portproxy delete v4tov4 listenport=7860 listenaddre...

## 原文内容

# WINDOWS中添加端口转发规则

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/13/451549.html
**发布时间**: 2025-01-13

WINDOWS中添加端口转发规则
设置端口转发
在 Windows 上，以管理员身份打开 PowerShell，
netsh interface portproxy add v4tov4 listenport=7860 listenaddress=0.0.0.0 connectport=7860 connectaddress=123.45.67.89


在 PowerShell 中使用 netsh interface portproxy 命令设置的端口转发规则是持久性的。这些规则会在系统重启后继续生效，因为它们被存储在 Windows 的注册表中。


删除端口转发规则
如果想删除之前设置的端口转发规则，可以使用以下命令：
netsh interface portproxy delete v4tov4 listenport=7860 listenaddress=0.0.0.0



这里的 listenport 和 listenaddress 应与之前设置时的值一致。


查看当前的端口转发规则
要查看当前系统中所有的端口转发规则，可以运行：
netsh interface portproxy show all






posted on 2025-01-13 09:34 paulwong 阅读(177) 评论(0)  编辑  收藏 所属分类: WSL

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
