---
title: 在LINUX系统直接重装windows系统（ventoy）
date: 2026-07-26
categories: [技术]
tags: [Windows, Linux]
---

使用ventoy安装windows 10

选择你刚才导入的WIN10ISO文件 回车。

进入安装页面，由于linux系统的硬盘格式问题，直接安装肯定是不成功的，所以要进入系统命令行

选择疑难解答

选择高级选项

选择命令提示符

窗口输入diskpart回车

进入DISKPART命令模式后，输入list disk回车，出现磁盘信息。

显示磁盘0，磁盘1直接信息是否联机，大小，可用状态。

若显示为磁盘0，select disk 0回车，接着输入clean，删除分区。

输入convert ntfs回车，磁盘转换为NTFS。

输入create partition primary size=102400。此部分是创建硬盘分区1024（100G）

若创建为102400，重装系统后可以到计算机管理-磁盘管理中创建剩余分区。

输入format fs=ntfs quick回车快速格式化

格式化完成后输入exit继续安装系统

文章出处：
https://zhuanlan.zhihu.com/p/366959499