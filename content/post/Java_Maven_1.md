---
title: "Java_Maven_1"
date: 2020-09-17T09:06:22+08:00
categories:
- 日常问题
tags:
- Java
keywords:
- tech
#thumbnailImage: //example.com/image.jpg
---

<!--more-->

# Java
## <font color=#DC143C>Could not transfer artifact org.apache.maven:maven-profile:jar:*****from/to central (https://repo.maven.apache.org/maven2): GET request of: org/apache/maven/maven-profile/****/maven-profile-****.jar from central failed</font>

</br>

用IDEA添加依赖是出现的问题

</br>

解决办法:在setting中搜索Maven，找到自己Maven地址并打开。

![avatar](https://i.loli.net/2020/09/17/kP5QW8IyOhlDn4i.png)

</br>

打开后在该文件中搜索"lastUpdated"

![avatar](https://i.loli.net/2020/09/17/2AFLH8sQIkmgYDw.png)

</br>

然后将搜索到的"xxx.lastUpdated"文件<font color=#Dc143c>全部删掉</font>,刷新后就可以啦。