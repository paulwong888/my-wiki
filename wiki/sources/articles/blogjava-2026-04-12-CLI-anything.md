---
title: CLI anything
type: source
category: article
created: 2026-04-12
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2026/04/12/451770.html
author: paulwong
tags: ['blogjava']
---

# CLI anything

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/04/12/451770.html  
**发布时间**: 2026-04-12

## 摘要

# CLI anything

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/04/12/451770.html
**发布时间**: 2026-04-12

现在我们要操作一个网站，通常要打开浏览器，点不同的按钮进行操作，不同的按钮代表了不同的功能。
cli将网站的这些功能，在命令行中完成，cli-boss search 就能返回职位的数据，当然是json或其他文本格式，对于人类是阅读不方便的，但对于ai是非常友好。
也就是搜索网站的职位，在cli中对应cli-boss search。

cli安装

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->#添加CLI-Anything插件市场
/plugin marketplace add HKUDS/CLI-Anything

#从市场安装 cli-anything插件
/plugin install cli-anythi...

## 原文内容

# CLI anything

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/04/12/451770.html
**发布时间**: 2026-04-12

现在我们要操作一个网站，通常要打开浏览器，点不同的按钮进行操作，不同的按钮代表了不同的功能。
cli将网站的这些功能，在命令行中完成，cli-boss search 就能返回职位的数据，当然是json或其他文本格式，对于人类是阅读不方便的，但对于ai是非常友好。
也就是搜索网站的职位，在cli中对应cli-boss search。

cli安装

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->#添加CLI-Anything插件市场
/plugin marketplace add HKUDS/CLI-Anything

#从市场安装 cli-anything插件
/plugin install cli-anything

制作专属cli流程
生成专属cli所需的代码，如python

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->克隆 https://github.com/jgraph/drawio
/cli-anything:cli-anything ./drawio

执行后，会生成一个cli_anything文件夹，里面有各种说明文件和源代码，包括了用户输入命令行后，背后需做的动作

编译源码，生成命令

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->#根据readme.md来操作
cd cli_anything
```bash
pip install -e .
```

使用专属cli

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

--># Create a new diagram 
filecii-anything-drawio project new mydiagram.drawio

# Open an existing 
diagramcli-anything-drawio project open mydiagram.drawio

# Add a shape
cli-anything-drawio edit add --value "Hello" --x 100 --y 100

# List all elements
cli-anything-drawio edit list

#其他各种见cli_anything/readme.md

借助agent使用专属cli

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->你借助 cli-anything-drawio里面的CLI命令画一个快速排序算法的流程图

paulwong 2026-04-12 15:11 发表评论

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
