---
title: Python+Selenium 调起浏览器
date: 2021-08-13 13:56:37
tags: [python, selenium]
categories: 自动化测试
---
## 一、什么是Selenium？
<font color=red>Selenium</font>是一个用于Web应用程序测试的工具。Selenium测试直接运行在浏览器中，就像真正的用户在操作一样。支持的浏览器包括IE（7, 8, 9, 10, 11），Mozilla Firefox，Safari，Google Chrome，Opera，Edge等。这个工具的主要功能包括：测试与浏览器的兼容性——测试你的应用程序看是否能够很好得工作在不同浏览器和操作系统之上。测试系统功能——创建回归测试检验软件功能和用户需求。支持自动录制动作和自动生成 .Net、Java、Perl等不同语言的测试脚本。
## 二、安装Selenium
### 1. 下载python的selenium安装包
``` bash
pip install selenium
```
### 2. Windows下下载与浏览器版本相对应的webdriver
chrom浏览器的web driver
``` bash
http://npm.taobao.org/mirrors/chromedriver/
```
firefox（火狐浏览器）的web driver
``` bash
https://github.com/mozilla/geckodriver/releases
```
Safari的web driver
``` bash
https://webkit.org/blog/6900/webdriver-support-in-safari-10/
```
{% note primary %}
下载完成后，将解压出来的exe文件与py文件放置同一个目录下。
{% endnote %}
## 三、示例
### 1. 引入Selenium包，并调起浏览器
``` javascript
from selenium import webdriver
```