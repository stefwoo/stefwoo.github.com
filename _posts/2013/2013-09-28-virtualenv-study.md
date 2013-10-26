---
layout: post
title: 一个virtualenv例子
categories:
- Programming
tags:
- python
---
#virtualenv 用来创建隔离的Python环境

    mkdir myproject1
    cd myproject1
    virtualenv env --no-site-packages #创建干净的环境，如果不带此参数则将原安装的所有包安装过来
    source env/bin/active
    (env) pip install django
    (env) pip install mysql-python
    (env) deactive
