---
title: Python-学习作图2
date: 2019-10-15 21:46:09
tags:
- Python
- Data
- Visualization
categories: 三十学艺
---

#### 几个原则

* 同样的数据可以有不同的图表展示方式
* 同样的图表可以通过不同层次的命令实现
* Python中的作图工具封装程度较高，后期调整需要在有限的属性中修改

#### Python中主要的绘图函数

* plot()
* matlibplot()
* seaborn.plot()

#### 图形类型

根据数据集，Python中提供不同的方法绘制图形，主要为以下几种数据类型提供绘图方法:

* 单变量（离散或分布）：hist，box，density，
* 双变量（离散或分布）：line，scatter
* 多变量（离散或分布）：correlation，k-cluster
* 地图

还可以简单地将图形分为：

* 基于categories的图形catplot()实现，如：box，scatter等
* 基于relationship的图形relplot()实现

#### jupyter notebook中的seaborn教程

<iframe width='100%' scolling=no height="800" frameborder="0" src='https://tewangchao213.github.io/seaborn_01.html'></iframe>>


