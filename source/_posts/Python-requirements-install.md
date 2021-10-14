---
title: Python中自动安装依赖(freeze)
date: 2021-10-05 16:35:20
tags: [python]
categories: 日常问题
---
## 前言
在学习python的过程中，经常会遇到需要在另外一台机器上去运行程序或者换电脑进行开发的情况出现，当遇到这些情况时最笨的办法就只能一遍一遍的敲运行命令看少哪个依赖包就去pip哪个依赖包，这样重复操作就非常的麻烦，那这时候我们就可以使用freeze命令来导出已安装模块文档
## 使用
在可运行项目的电脑中，进入项目根目录输入以下命令以导出已安装模块文档，完成以下命令后可在当前目录下生成一个相对应的文件，文件中包含了包名以及版本号
```bash
pip freeze > modules.txt
```
在另外一台电脑的项目根目录输入以下命令即可开始安装需要安装的依赖
```bash
pip install -r modules.txt
```
{% note success %}
接下来就只需要耐心等待安装完成，然后启动项目就好啦~
{% endnote %}
![添加微信](https://init-blog.init888.cn/post/common/WX_QR_code.png)