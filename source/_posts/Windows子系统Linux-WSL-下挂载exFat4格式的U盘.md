---
title: Windows子系统Linux(WSL)下挂载exFat4格式的U盘
date: 2019-10-03 09:36:12
tags: Linux
categories: 三十学艺
---
#### 问题描述
在Surface GO上装了exFat4格式的U盘，但是在WSL中无法在/mnt目录下找到。

#### 解决方法
需要安装Linux下exFat的支持。
```
sudo apt-get install exfat-fuse exfat-utils   # 安装exFat格式支持
sudo mkdir /mnt/d                             # 准备挂载目录
sudo mount -t drvfs d: /mnt/d                 # 挂载盘符
sudo umount /mnt/d                            # 退出linux前卸载U盘，否则下次会出错
```


