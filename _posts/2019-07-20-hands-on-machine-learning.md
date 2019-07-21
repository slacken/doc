---
layout: post
title:  "Hands-On Machine Learning with Scikit-Learn & Tensorflow"
date:   2019-07-20 14:32:04 +0800
categories: "Machine Learning"
---

## 相关链接

* [code examples as Jupyter notebooks](https://github.com/ageron/handson-ml)
* [scikit-learn](http://scikit-learn.org/)
* [tensorflow](http://tensorflow.org/)


补充材料
* [Kaggle past solutions](https://github.com/EliotAndres/kaggle-past-solutions)

## 笔记

### pipenv install 太慢

优化1：切换依赖源，比如阿里云：https://mirrors.aliyun.com/pypi/simple

优化2：主要是locking过程很慢，可以先跳过lock过程，即 pipenv install --skip-lock，最后再 pipenv lock

总体上pipenv还是很好用的。

### RuntimeError: Python is not installed as a framework

The Mac OS X backend will not be able to function correctly if Python is not installed as a framework. See the Python documentation for more information on installing Python as a framework on Mac OS X.

解决办法：指定MacOS支持的二维图片渲染引擎

Create a file ~/.matplotlib/matplotlibrc there and add the following code:

```backend: TkAgg```

或者在代码里
```python
import matplotlib
matplotlib.use('TkAgg')
```