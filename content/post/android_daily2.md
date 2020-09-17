---
title: "Android_daily2"
date: 2019-11-20T00:08:40+08:00
categories:
- 日常问题
tags:
- Android
keywords:
- tech
#thumbnailImage: //example.com/image.jpg
---

<!--more-->
# Android daily 2
### <font color=#DC143C>is not an enclosing class</font>
继上回做音乐播放器UI时的有一个问题，这是在用Intent做页面跳转的时候遇到的，虽然问题是小问题，但是一开始是真的觉得很对的,QAQ，眼睛盯出问题了。
![android_daily03.png](https://images.cnblogs.com/cnblogs_com/MaGnet/1579760/o_191121063221android_daily03.png)

解决办法:是<font color=#DC143C>".class"</font>，看错了，误以为和前面的指定的界面一样用了".this"
![android_daily04.png](https://images.cnblogs.com/cnblogs_com/MaGnet/1579760/o_191121063226android_daily04.png)

敲代码的时候眼睛一定要看清了，别把自己敲蒙了。