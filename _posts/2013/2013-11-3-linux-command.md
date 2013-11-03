---
layout: post
title: 用到的linux命令
categories:
- Linux
tags:
- linux
---
## 常用压缩和解压缩命令

    壓　縮：tar -jcv -f filename.tar.bz2 要被壓縮的檔案或目錄名稱
    查　詢：tar -jtv -f filename.tar.bz2
    解壓縮：tar -jxv -f filename.tar.bz2 -C 欲解壓縮的目錄

## 查看磁盘剩余空间和文件夹大小

    df -hl 查看磁盘剩余空间
    du -h 文件夹
    更多功能查看：
    df --help
    du --help

## FTP

    登录
    ftp ip
    输入用户名，密码即可

    查看FTP 命令
    ftp> ?

    上传文件
    Put命令：格式：put local-file [remote-file] 将一个文件上传到ftp
    Mput命令：格式：mput local-files 将本地主机中一批文件传送至远端主机.
                  注意：mput命令只能将当前本地目录下的文件上传到FTP上的当前目录。比如，在 /root/dave下运行的ftp命令，则只有在/root/dave下的文件linux才会上传到服务器上的当前目录下。

    ftp> pwd    -- 显示FTP上当前路径
    ftp> ls   -- 显示当前目录下的文件
    ftp> mkdir Dave    -- 创建文件夹Dave
    ftp> cd Dave      -- 进入文件夹Dave
    ftp> lcd     -- 显示当前本地的路径，我们可以将这个路径下的这个文件上传到FTP服务器的相关位置

    下载文件
    同样也有2个命令： get 和 mget。 Mget 用户批量下载。
    get [remote-file] [local-file]
    mget [remote-files]
    同样，mget 是将文件下载到本地的当前目录下。

ftp> bye  --断开FTP 连接