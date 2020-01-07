---
title: 利用HEXO在GITHUB上部署个人网页的使用文档
subtitle: 阅读及编写使用文档
date: 2019-09-21 13:06:12
tags: hexo
categories: 三十学艺 
---

#### 主要过程
1. 备外部仓库（Github）；
2. 准备本地网页（HEXO）;
3. 利用HEXO生成本地网页；
4. 利用GIT工具将网页发布至Github。

#### 外部仓库的准备
1. 注册github账号
2. github账号下新建与用户名相同的仓库（repo）
3. 在repo下面的master分支下面创建博客页面
4. 经过设置页面下的博客生成，得到一个个人博客页面

#### 本地网页的准备
1. 需要安装node.js及Git windows2. 
2. 利用命令行安装hexo
```
npm install hexo-cli -g #安装hexo客户端
hexo init <文件夹名称>
cd <文件夹名称>
npm install #hexo客户端安装默认配置
hexo -v #确认hexo安装成功及版本
```
3. 进入我们需要发布的文件夹，右键“gitbash in this path”，常用的hexo命令及作用
```
 hexo -new # 生成新的文件位于source/posts下
 hexo -generate # 生成静态网页
 hexo -server # 生成本地网页
 hexo -deploy # 发布到目的repo
```
#### 链接github与hexo

1. 链接github与本地需要秘钥，生成密钥方法如下：
```
 git config --global user.name "github用户名"
 git config --global user.email "github注册邮箱"
 ssh-keygen -t rsa -C "github注册邮箱"
```
2. 在github网站中录入密钥信息，个人设置->ssh and GPG keys->录入isa.pub的密钥信息
3. 修改配置文件_config.yml中的deply信息
4. 安装deploy插件

 ```npm i hexo-deployer-git```

#### 完成



