---
title: LINUX学习（1）-Linux的文件管理
date: 2019-10-02 11:19:59
tags: Linux
categories: 三十学艺
---
入门Linux必须熟知Linux的文件管理方式，这是Linux及其他一些CLI软件的基础。

#### 1. Linux的文件管理方式
Linux脱胎于Unix，其核心思想：
1. 多用户多任务，Unix最早是相容分时系统演变而来。
2. 所有的程序或系统设备都是文件。
3. 不管建构编辑器还是附属文件，所写的程序只有一个目的，且要有效的完成目标。

Linux的文件树：
```
/: 为根目录，其下有/boot（启动），/bin（常用命令），/etc（配置文件），/home（用户），/root（管理员），/usr（应用程序），/lib（基本代码库），/sys（内核文件系统）
~：为用户目录，即/home/username
```
#### 2. Linux的文件类型
与windows文件不同，Linux的文件扩展名只起到标记作用。其文件属性可以用`ls -l`查看。
具体对应信息如下：

1|2-3-4|5-6-7|8-9-10
--|-----|-----|------
文件属性|root权限|用户权限|其他用户权限
d:目录 -: 文件|r-w-x|r-w-x|r-w-x
|读-写-执行|读-写-执行|读-写-执行

使用chmod命令可以更改文件属性。
```
$chmod +x filename 			#给文件添加可执行属性
$chmod -x filename          #给文件去除可执行属性
```
#### 3. Linux的文件编辑软件

Linux有非常好用的文件编辑软件vim，常用方法如下：
```
$vim filename               #新建，打开文件
键盘i                        #进入编辑模式
Esc                         #退出编辑模式
:wq                          #保存并退出
```
#### 4. Linux的可执行文件

Linux下，所有的文件都可以具备可执行属性，但是能否成功执行取决于文件内容。 有多种方式可以执行文件
1. 编辑可执行文件
```
#使用for循环批量创建10个文件 linux-1到linux-10
#!/bin/sh
[ ! -d $PWD/file ] && mkdir -p $PWD/file && exit 1
 
for count in `seq 10`
do
    touch $PWD/file/linux-$count
done
————————————————
版权声明：本文为CSDN博主「乌托邦2号」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/taiyang1987912/article/details/39934055
```
将以上文件保存为`create.sh`,并利用`chmod +x create.sh`将该文件增加可执行属性。直接运行`./create.sh`即可。

2. 上述文件还可以使用`sh create.sh`或`bash create.sh`运行。此时，文件开头的注释`#! /bin/sh`可以不写。该文件也可以不是可执行属性。

