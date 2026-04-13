---
title: MAC使用VSCODE远程连接WIN11下的WSL2的方法
date: 2025-01-11
source: http://www.blogjava.net/paulwong/archive/2025/01/11/451544.html
---

# MAC使用VSCODE远程连接WIN11下的WSL2的方法

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/11/451544.html
**发布时间**: 2025-01-11

MAC使用VSCODE远程连接WIN11下的WSL2的方法
1.首先给win11的ssh开一个新端口.(修改C:\\ProgramData\\ssh\\sshd_config即可)

2.win11设置防火墙,开放1中添加的端口.

3.win11进入wsl2,输入ifconfig,查看ip地址(输出信息第二行 inet后面那一串数字).

4.在win11的cmd中输入以下命令:

netsh interface portproxy add v4tov4 listenaddress=127.0.0.1 listenport=<步骤1中开放的端口> connectaddress=<步骤3中得到的ip地址> connectport=22


5. ssh连接步骤1中开放的端口就可以连接上wsl2(注意事项:(1)连接时,win11上需要有一个wsl窗口,不然连不上,(2)ssh连接时的用户名写wsl2中的用户名,密码写wsl2中的密码,ip地址写win11的ip地址)

https://www.zhihu.com/question/618935377

posted on 2025-01-11 09:59 paulwong 阅读(106) 评论(0)  编辑  收藏 所属分类: WSL