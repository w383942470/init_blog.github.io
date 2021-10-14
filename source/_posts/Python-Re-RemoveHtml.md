---
title: Python中使用正则去除html标签
date: 2021-09-10 18:00:37
tags: [python]
categories: 日常问题
---
{% note info %}
在爬虫过程中渠道的text中包含html标签，或者想剔除某一块标签，使用正则即可将html标签完全剔除
{% endnote %}
``` python
import re

html = '<font color=red>区块链</font>技术应用场景落地，重庆智能学生证助力大数据精准教学'

pattern = re.compile(r'<[^>]+>', re.S)
title = pattern.sub('', html)

print(title)
```
![添加微信](https://init-blog.init888.cn/post/common/WX_QR_code.png)
