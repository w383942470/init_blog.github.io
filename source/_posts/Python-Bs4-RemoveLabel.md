---
title: Python如何利用BeautifulSoup剔除不想要的标签
date: 2021-09-10 14:55:48
tags: [python]
categories: 日常问题
---
{% note info %}
在爬虫过程中遇到页面中有部分标签不是想要的，但是又无法取下一层标签进行精确定位时，可以用BeautifulSoup中的一下方法进行剔除标签，从而达到目的
{% endnote %}
``` python
from bs4 import BeautifulSoup
html = '
<h3>
<small>Sep 09, 2021, 08:00 ET</small>
Kawaii Islands raises $2.4M in private token sale for its upcoming anime metaverse
</h3>'
page_html = BeautifulSoup(html, 'lxml')
[s.extract() for s in page_html('small')]

print(page_html.text)
```
![添加微信](https://init-blog.init888.cn/post/common/WX_QR_code.png)
