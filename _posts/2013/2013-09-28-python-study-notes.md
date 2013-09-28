---
layout: post
title: 学习python的一些记录
categories:
- Programming
tags:
- python
---

## json

json.loads()参数中的object_hook作为一个参数用来处理输入的数据。在输入数据流中, 对于解码获得的每个字典都会调用object_hook, 将这个字典转换成其他类型的对象,object_hook函数返回的是调用程序所需要的对象, 而不是字典。

## urllib2

urllib2.urlopen()的参数timeout需设置，避免未知故障引起的超时，从而造成程序假死。

据朋友[small.fz](http://bluemask.net)说urllib2库的口碑不太好，推荐我用[Requests库](http://cn.python-requests.org/en/latest/),目前正在看文档。
