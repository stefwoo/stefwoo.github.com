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

## *args, **kwargs

* *args表示任何多个无名参数，它是一个tuple； 
* *kwargs表示关键字参数，它是一个 dict。

同时使用args和kwargs时，必须args参数列要在kwargs前，否则报语法错误。

## @property 

@property装饰可以将python定义的函数“当做”属性访问，从而提供更加友好访问方式。

## eval()

eval语句用来计算存储在字符串中的有效Python表达式。下面是一个简单的例子

## exec

exec语句用来执行储存在字符串或文件中的Python语句

## enumerate(）函数

enumerate(）函数相当于给一个序列增加一个序号，很好用
    >>> seasons = ['Spring', 'Summer', 'Fall', 'Winter']
    >>> list(enumerate(seasons))
    [(0, 'Spring'), (1, 'Summer'), (2, 'Fall'), (3, 'Winter')]
    >>> list(enumerate(seasons, start=1))
    [(1, 'Spring'), (2, 'Summer'), (3, 'Fall'), (4, 'Winter')]

## dict.popitem()

字典的popitem()返回一个元组，然后删除字典中的item，如字典为空则报错。
和列表的pop类似。
列表的pop和append方法同时使用，很方便。
dict.get(key[, default])
Return the value for key if key is in the dictionary, else default. If default is not given, it defaults to None, so that this method never raises a KeyError.
如果存在key对应的值则返回值，如果不存在则返回设置的值。方便啊！


