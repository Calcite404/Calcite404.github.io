---
layout: post
title: 20221021-使用nbconvert提升jupyter生产力
toc:  true
date: 2022-10-21 15:46 +0800
tags: [jupyter, nbconvert, notebook]
---

一直在寻求提升`jupyter notebook`扩展性的方法，发现了`nbconvert`这个简单好用的pkg.


#### Installation
+ 安装nbconvert
``` shell
conda install nbconvert
```
+ 安装Pandoc（Optional）
+ 安装Tex（Optional）

#### Run
```
jupyter nbconvert --to <Format> <notebook.ipynb>
# 同时转换多个
jupyter nbconvert --to <Format> <notebook1.ipynb> <notebook2.ipynb>
```
-   为需要转换成的格式，可选的有`html`, `latex`, `pdf`, `slides`, `markdown`, `rst`, `script`, `notebook`

### Reference: How to improve jupyter notebook expansibility
+ [This blog post was written in a Jupyter Notebook | Scott Condron’s Blog](https://www.scottcondron.com/jupyter/blogging/visualisation/2020/01/20/this-blog-post-was-written-in-a-jupyter-notebooks.html)
+ [Quarto - Tutorial: Hello, Quarto](https://quarto.org/docs/get-started/hello/jupyter.html)
+ [Site Unreachable](https://nbdev.fast.ai/tutorials/tutorial.html)
+ [pandoc · PyPI](https://pypi.org/project/pandoc/)
+ [GitHub - jupyter/nbconvert: Jupyter Notebook Conversion](https://github.com/jupyter/nbconvert)
+ [Jupyter文件转换-nbconvert命令行工具简介_madao10086+的博客-CSDN博客_jupyter-nbconvert](https://blog.csdn.net/qq_36178962/article/details/115870759)
+ [GitHub - jupyter/nbconvert: Jupyter Notebook Conversion](https://github.com/jupyter/nbconvert)
+ [Installation — nbconvert 7.2.0.dev0 documentation](https://nbconvert.readthedocs.io/en/latest/install.html#installing-nbconvert)