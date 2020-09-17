---
title: "Hugo博客搭建问题"
date: 2019-10-26T20:55:46+08:00
categories:
- 日常问题
tags:
- Hugo
keywords:
- tech
#thumbnailImage: //example.com/image.jpg
---

<!--more-->
总结一下初次尝试遇到的一些问题

***
## config.toml文件
拿我用的主题[hugo-tranquilpeak-theme](https://themes.gohugo.io/hugo-tranquilpeak-theme/)为例，首先很容易的将它git到本地，然后打开了该主题的[用户手册](https://github.com/kakawait/hugo-tranquilpeak-theme/blob/master/docs/user.md)并阅读，找到了用户自定义的方法(修改/exampleSite/config.toml)，通过修改该toml文件来配置自己
  主题功能。但在配置后发现了问题，主题样式并不会发生改变，在翻阅找到了解决方法。  
  
  <font color=#DC143C>将根目录的下的congfig.toml用exampleSite/config.toml文件替换即可。</font>  
  
***
## config.toml配置
主要配置:  

- baseURL
- author
- Menu Configuration
- coverImage
- favicon  

配置方案:  

1. baseURL配置为自己博客部署的url。 
2. author配置依照给的提示很简单，值得注意的是gravatarEmail覆盖用户picture，所以想要一个指定的头像的话还是在gravatarEmail前面加"#"注释掉吧。
3. Menu Configuration中的配置也可以给的提示配置，注意点是pre的值，也就是在边栏显示的图标，用的是font-awesome4,需要更换图标的可以去翻翻。
4. coverImage更换的是背景图，注意存放位置static\images\下。
5. favicon是网站图标，放于static\images\下，值得注意的在我翻阅github的时候发现了反馈的问题是图标只能在主页面显示，自己亲测确实如此，也得到了解决方法:在代码layouts/partials/head.html中的35行`{{ with .Site.Params.favicon }} <link rel="icon" href="{{ . | absURL }}"> {{ end }}`