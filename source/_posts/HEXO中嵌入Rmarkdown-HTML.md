---
title: HEXO中嵌入Rmarkdown-HTML
date: 2019-10-05 09:17:02
tags: 
- hexo
- R
- MarkDown
categories: 三十学艺
---
RMarkDown是R中的MarkDown语言，其文件可以在Rstudio中运行，可以直接输出html，PDF，Word，PPT等文件，是R语言学习的利器，如：编辑说明文档，完成R语言作业等。

HEXO+GItHub是极其方便有效的静态网页生成工具，但是非常难以使用Rmarkdown或Rmarkdown生成的文件。

利用`<iframe></iframe>`模块可以将html嵌入到正常md文件中，可以作为一种解决方案。

#### 问题描述

1. 目的是利用HEXO+GitHub发布Rmarkdown生成的文件；
2. Rmarkdown自带的Blogdown难以掌握，安装过程中出现了各种我无法解决的问题：如安装大量的包，硬盘格式不兼容；
3. Rmarkdown生成的html可以发布到GitHub上（~/\*html),但是这种方式生成的html文件没有tags和categories，难以归类和检索。

#### 解决方案

Rmarkdown->html->github->md文件中嵌入html网页

1. Rmarkdown生成html文件，修改该html文件，在文件起始加下以下：
```
---
layout: false
---
# 此语句防止hexo对该html文件的渲染
```
2. html文件放置于.source文件夹中，并通过`git deploy`发布到github上，此时该html位于github master-repo中的第一层，地址为"https://yourname.github.io/*.html"
3. 新建常规md文件，正常编辑，在需要嵌入html的位置加上如下语句：
```
<iframe width='100%' scolling=no height="800" frameborder="0" src='https://yourname.github.io/*.html'></iframe>>
```

#### 完成