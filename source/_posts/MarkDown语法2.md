---
title: MarkDown语法（2）
date: 2019-10-01 20:07:24
tags: MarkDown
categories: 三十学艺
---
MarkDown作为一种极为优秀的编辑格式，为程序员所喜爱。一个重要的原因是MarkDown提供非常方便的代码引用功能。

#### 单行代码引用
```
单行代码引用，使用"`"作为起点和终点
`这是一行代码`
```
效果如下

`这是一行代码`

#### 代码块引用
```
代码块以“```”起始一行，以“```”结束一行
（```）
这是一个代码块
（```）
```
效果如下
```
这是一个代码块
printf("Hello,world!")
```

#### 其他引用
```
使用“>”引用他人的词句
> 飞流直下三千尺，
>
> 疑是银河落九天。

引用还可以嵌套，使用多个“>>”达到效果
> 飞流直下三千尺，
>> 疑是银河落九天。
```
效果如下
> 飞流直下三千尺，
>
> 疑是银河落九天。

> 飞流直下三千尺，
>> 疑是银河落九天。

#### 流程图
```
高级用法，流程图有自己的语法，尚在研究之中。
```flow
st=start:Start
i=inputoutput:输入年份n
cond1=condition:n能否被4整除？
cond2=condition:n能否被100整除？
cond3=condition:n能否被400整除？
o1=inputoutput:输出非闰年
o2=inputoutput:输出非闰年
o3=inputoutput:输出闰年
o4=inputoutput:输出闰年
e=end

st-i-cond1
cond1(no)-o1-e
cond1(yes)-cond2
cond2(no)-o3-e
cond2(yes)-cond3
cond3(yes)-o2-e
cond3(no)-o4-e
```
```

```
