---
title: Python爬虫遇到中文乱码怎么办
date: 2021-09-08 22:25:43
tags: [python]
categories: 日常问题
---

{% note info %}
在爬虫过程中遇到页面中文编码乱码的问题，直接给返回值更改编码即可解决
{% endnote %}
``` python
import requests

res = requests.get(url)

res.encoding = 'gb2312'

print(res.text)
```
![添加微信](https://init-blog.init888.cn/post/common/WX_QR_code.png)