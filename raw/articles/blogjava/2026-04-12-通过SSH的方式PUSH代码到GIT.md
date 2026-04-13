---
title: 通过SSH的方式PUSH代码到GIT
date: 2026-04-12
source: http://www.blogjava.net/paulwong/archive/2024/07/24/451470.html
---

# 通过SSH的方式PUSH代码到GIT

**原文链接**: http://www.blogjava.net/paulwong/archive/2024/07/24/451470.html
**发布时间**: 2026-04-12

通过SSH的方式PUSH代码到GIT
这几天要PUSH代码到GITHUB，发现之前用的密码方式被取消了，需改成SSH KEY的方式。
1.生成SSH-KEY
ssh-keygen
#会产生 ~/.ssh/id_rsa 和 ~/.ssh/id_rsa_pub 文件
#如果是从别的地方拷贝过来的id_rsa，需chmod 400 ~/.ssh/id_rsa更改属性
2.在github上新建仓库
https://github.com/paulwong888/python-ai
3.导入公钥到github
打开你的SSH公钥文件，通常位于~/.ssh/id_rsa.pub。复制公钥内容，然后登录到你的GitHub账户，进入Settings > SSH and GPG keys，点击\