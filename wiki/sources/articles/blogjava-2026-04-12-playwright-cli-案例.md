---
title: playwright-cli 案例
type: source
category: article
created: 2026-04-12
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2026/04/12/451769.html
author: paulwong
tags: ['blogjava']
---

# playwright-cli 案例

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/04/12/451769.html  
**发布时间**: 2026-04-12

## 摘要

# playwright-cli 案例

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/04/12/451769.html
**发布时间**: 2026-04-12

环境

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->hiclaw docker
```bash
cat /etc/os-release 
```bash
PRETTY_NAME="Ubuntu 22.04.5 LTS"
```bash
NAME="Ubuntu"
```bash
VERSION_ID="22.04"
```bash
VERSION="22.04.5 LTS (Jammy Jellyfish)"
```bash
VERSION_CODENAME=jammy
```bash
ID=ubuntu
```bash
ID_LIKE=debian
```bash
HOME_URL="https://www.ubuntu.com/"
```bash
SUPPORT_URL="https://help.ubuntu.com/"
```bash
BUG_REPORT_URL=...
```

## 原文内容

# playwright-cli 案例

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/04/12/451769.html
**发布时间**: 2026-04-12

环境

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->hiclaw docker
```bash
cat /etc/os-release 
```bash
PRETTY_NAME="Ubuntu 22.04.5 LTS"
```bash
NAME="Ubuntu"
```bash
VERSION_ID="22.04"
```bash
VERSION="22.04.5 LTS (Jammy Jellyfish)"
```bash
VERSION_CODENAME=jammy
```bash
ID=ubuntu
```bash
ID_LIKE=debian
```bash
HOME_URL="https://www.ubuntu.com/"
```bash
SUPPORT_URL="https://help.ubuntu.com/"
```bash
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
```bash
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
```bash
UBUNTU_CODENAME=jammy
```

安装

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->npm install -g @playwright/cli@latest

安装chrome

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->npx playwright install chrome

操作

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->playwright-cli open www.cnn.com 
### Browser `default` opened with pid 159651.
### Ran Playwright code
```js
await page.goto('https://www.cnn.com');
```
### Page
- Page URL: https://edition.cnn.com/
### Snapshot
- [Snapshot](.playwright-cli/page-2026-04-12T02-21-31-067Z.yml)

安装skill

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->playwright-cli install --skills

默认会在当前目录下生成 .claude/skills/playwright-cli
得将playwright-cli搬到不同agent的skills目录下

案例1:打开页面，输入内容

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->用paywight-cLi参数--headed --persistent，打开grok，问问今天青岛天气怎么样?

案例2:打开页面，需点击加载数据

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->用playwrightcli 带参数 --headed --persistent 查看https://detail.tmall.com/item.htm?&xxc=taobaoSearchabbucket=4&id=612098145454&mi_id=0000AWGjgiGB7oSCDLfegRXMs0rDPkp34S50rNrByn86yAY&ns=1&skuId=5872701131539&spm-a21n57.1.hoverItem.2utparam-%7B%22aplus_abtest%22%3A%2240acb849856085978c81b6cdec803550%22%70D
前100条评论保存到一个csV文件里面。

让ai保存成一个skill

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->创建一个save_mall_comments skill把刚才打开网站，查看评论，并且保存评论的全过程，遇到的坑都提炼出来保存到skill里面

直接保存成一个不依赖ai的可执行脚本

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->你把刚才所有的playWwright CLI命令汇总成成一个脚本，执行脚本就能获取商品前100条评论，并且保存到一个CSV文件里面。注意每一步都有合理的延时与等待，确保任务成功。脚本写完你先测试一轮。

下次直接执行

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->./save_mall_comments.sh "https://detail.tmall.com/item.htm?id=612098145454&skuId=5872701131539" 100 --output tmall_reviews_612098145454_top100.csv --close-browser

案例3:web自动化测试

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->阅读代码，把从注册开始的主体流程写一个中文的测试文档，只测试主流程即可。然后用playwright-cli open --headed --persistent 打开网页，根据你的测试用例，完成进行测试，

还可以借助openclaw，进行定时自动化测试

案例4:在x上发推

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->playwright-cli https://x.com/compose/articles  --headed --persistent  打开网站，创建写一个新的文章，把 为什么巨头都在做CLI.local.html 的内容粘贴进去。

然后找到所有的"1f4f7.svg"小icon的位置，按Backspace键删除，然后复制images文件夹里面的图片，按Ctrl+V粘贴进去。"1f4f7.svg"小icon数量跟图片数量是相等的，你要按顺序替换。复制操作你应使用操作系统的CLI命令，粘贴操作在浏览器里按Ctrl+V就行了。

整理成skill

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->好，非常好，你把从把文章里的图片下载到本地，开始的全流程，整理成一个skills，放到项目目录。以后我只要给你一个文章，你就能自动发布

如何使用这个skill

Code highlighting produced by Actipro CodeHighlighter (freeware)
http://www.CodeHighlighter.com/

-->给http://xxx.xxx.xxx/xxx.html 文章路径，用 x-article-auto-publisher自动发布

paulwong 2026-04-12 10:24 发表评论

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
