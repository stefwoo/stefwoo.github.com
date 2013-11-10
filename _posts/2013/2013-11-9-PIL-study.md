---
layout: post
title: PIL在Win7下不能show的解决办法
categories:
- Programming
tags:
- python
---

在Win7下使用python的PIL模块的时候，使用show（）方式的时候会出现如下问题：

![无法显示](http://wpimg-wpimg.stor.sinaapp.com/original/f202d8757a1062de27911fd9f12afaec.png "无法显示图片")

原因为PIL的show()方法生成一个bitmap的临时文件，然后调用图片浏览器观看，而Win7的图片浏览器不接受命令行形式的图片，所以不能显示。

解决办法为构建一个函数将图片先显式的保存为一个文件，然后调用webbrowser浏览这个图片就可以了，使用起来和原本的show()方法也差不多。但是需要注意的是，im需要先convert一下，免得其他格式的图片不能保存成为jpg。

    def show_img(im):
        im.save("tmp.jpg")
        import webbrowser
        webbrowser.open("tmp.jpg")
