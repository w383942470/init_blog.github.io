---
title: Python如何随机打乱list列表
date: 2021-09-05 09:39:45
tags: [python]
categories: 日常问题
---
## 条件
{% note info %}
假设已有一个list为['dog', 'pig', 'cat', 'mouse']，需求是将该列表随机打乱
{% endnote %}
## 解决方法
{% note info %}
使用python随机函数random，调用random中的shuffle方法，将需要打乱的列表作为参数传递
{% endnote %}
```python
import random

demo_list = ['dog', 'pig', 'cat', 'mouse']

print(demo_list)
print('------------------------------')

# 循环打印十次看随机后的列表
for i in range(0, 10):
    random.shuffle(demo_list)
    print(demo_list)
```
![结果展示](Python-Change-List/show_result.jpg)
![添加微信](Python-Change-List/WX_QR_code.png)