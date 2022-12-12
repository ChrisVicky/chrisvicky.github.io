---
title: Source Backup for Disk Update
toc: true
categories:
- Post
tags: 
- Linux
- 记录
---

## Background

* 作为大学生，只有一台 Thinkpad T14 Gen 1 的笔记本却安装了 Arch Linux，而由于课程需要仍保留了大部分 Windows 11 的系统，长期以来的使用，让 512 GB 的存储空间告急，于是打算更换一块 1T 的固态硬盘。在此对磁盘更换做一个记录。

## 准备

### 文件分类
* 第一大类：系统文件，
    * 如 Windows 等 Operating Systems 的文件
    * 不考虑保存，但需要先查清除如何对 Windows 11 下的 Office 全家桶进行恢复。

* 第二大类：工程文件；
    * 2-1. 项目、代码等
        * 存入 github 代码库，将不必要保存的 tmp 文件删除
        * 写好 README 文档
    * 2-2. 安装包、dependency
        * 丢弃，实际使用时再安装

* 第三大类：资源文件：
    * 3-1. 课程文件等
        * 打包按时间排序
        * 项目类文件保存两份
    * 3-2. 配置文件
        * 重要配置打包或上传 github 
    * 3-3. 字体
        * 不能打包，但需要确定安装和配置方案
    * 3-3. 其他资源
        * 写个 README

### 计划

1. 文件备份
    * 根据上述分类进行备份
    * 2022-12-12 23:38 DONE

2. 确定安装和磁盘分区
    * 安装 512 GB 的 Windows 11 系统 和 512 GB 的 Linux 系统 
    * Linux 安装 DWM + Xorg （需要先写好安装文档以便查看）

3. 购置固态硬盘
    * 选取三星 "980 Pro PCIe 4.0 NVMe M.2"
    * 2022-12-12 23:38 次日到貨 

4. 对需要安装的系统和软件、配置写教程

| 待安装（配置）的内容 | 教程                                                                               | 备注                             |
|----------------------|------------------------------------------------------------------------------------|----------------------------------|
| Arch Linux           | [viseator的博客](https://www.viseator.com/2017/05/17/arch_install/)                |                                  |
| dwm                  |                                                                                    | 拷贝文件即可, 应当包括 autostart |
| dmenu                |                                                                                    | 同上                             |
| vim / nvim           |                                                                                    | 同上                             |
| 中文输入法           | [中文輸入法等安裝](https://www.viseator.com/2017/07/02/arch_more/)                 |                                  |
| yay                  | [yay git repo](https://aur.archlinux.org/yay.git)                                  |                                  |
| clash                | [我的博客](https://chrisvicky.github.io/2022/12/09/Setup-Systemd-for-clash-Proxy/) |                                  |
| navicat              |                                                                                    | 有破解文件                       |
| apifox               |                                                                                    |                                  |
| vivado               |                                                                                    | 需要备份一下 PKGBUILD 文件       |
| libfreenect2         | !!                                                                                 | 十分重要                         |
| opencv               |                                                                                    | yay 将就用一下先                 |
| virtualbox           | OK                                                                                 |

---





