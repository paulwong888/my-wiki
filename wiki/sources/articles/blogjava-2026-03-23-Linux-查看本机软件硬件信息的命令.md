---
title: Linux 查看本机软件硬件信息的命令
type: source
category: article
created: 2026-03-23
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2026/03/23/451765.html
author: paulwong
tags: ['linux']
---

# Linux 查看本机软件硬件信息的命令

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/03/23/451765.html  
**发布时间**: 2026-03-23

## 摘要

# Linux 查看本机软件硬件信息的命令

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/03/23/451765.html
**发布时间**: 2026-03-23

🖥️ 硬件信息

    CPU 信息

        lscpu → 显示 CPU 架构、核心数、线程数
        cat /proc/cpuinfo → 查看详细 CPU 型号、频率

    内存信息

        free -h → 显示内存使用情况
        cat /proc/meminfo → 查看详细内存参数

    硬盘信息

        lsblk → 查看磁盘分区和挂载
        df -h → 查看磁盘使用情况
        fdisk -l → 查看磁盘分区表

    PCI/USB 设备

        lspci → 列出所有 PCI 设备
        lsusb → 列出所有 USB 设备

    主板/BIOS

        dmidecode → 显示 BIOS、主板、内...

## 原文内容

# Linux 查看本机软件硬件信息的命令

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/03/23/451765.html
**发布时间**: 2026-03-23

🖥️ 硬件信息

    CPU 信息

        lscpu → 显示 CPU 架构、核心数、线程数
        cat /proc/cpuinfo → 查看详细 CPU 型号、频率

    内存信息

        free -h → 显示内存使用情况
        cat /proc/meminfo → 查看详细内存参数

    硬盘信息

        lsblk → 查看磁盘分区和挂载
        df -h → 查看磁盘使用情况
        fdisk -l → 查看磁盘分区表

    PCI/USB 设备

        lspci → 列出所有 PCI 设备
        lsusb → 列出所有 USB 设备

    主板/BIOS

        dmidecode → 显示 BIOS、主板、内存插槽等信息

  📦 软件信息

    操作系统版本

        cat /etc/os-release → 查看发行版信息
        uname -a → 查看内核版本和架构

    已安装软件

        Debian/Ubuntu: dpkg -l 或 apt list --installed
        RHEL/CentOS/AlmaLinux: rpm -qa 或 dnf list installed

    服务与进程

        systemctl list-units --type=service → 查看正在运行的服务
        ps aux → 查看当前进程

    网络信息

        ip addr → 查看网卡和 IP 地址
        ss -tuln → 查看端口监听情况

  🔍 综合工具

    inxi -Fx → 一次性显示完整的硬件和系统信息
    neofetch → 美观地显示系统信息
  paulwong 2026-03-23 11:45 发表评论

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
