---
layout: post
title: Start painting with NovelAI
toc:  true
date: 2022-10-23 19:08 +0800
tags: [novelai, ai绘画]
---


#### Installation

+ git clone
```
git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git novelai
```

+ [GitHub - AUTOMATIC1111/stable-diffusion-webui: Stable Diffusion web UI](https://github.com/AUTOMATIC1111/stable-diffusion-webui)
> Automatic Installation on Windows
	1.  Install [Python 3.10.6](https://www.python.org/downloads/windows/), checking "Add Python to PATH"
	2.  Install [git](https://git-scm.com/download/win).
	3.  Download the stable-diffusion-webui repository, for example by running `git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git`.
	4.  Place `model.ckpt` in the `models` directory (see [dependencies](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Dependencies) for where to get it).
	5.  __(Optional)__ Place `GFPGANv1.4.pth` in the base directory, alongside `webui.py` (see [dependencies](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Dependencies) for where to get it).
	6.  Run `webui-user.bat` from Windows Explorer as normal, non-administrator, user.

+ pytorch:
[Start Locally | PyTorch](https://pytorch.org/get-started/locally/)
```
conda install pytorch torchvision torchaudio cudatoolkit=11.6 -c pytorch -c conda-forge
```

+ dependency
`cd` to the project root path
```
python -m pip install -r requirements.txt
```

#### Tag generator
[NovelAI tag在线生成器](https://wolfchen.top/tag/?from=zhihu)

[NovelAI tag在线生成器 - 知乎](https://zhuanlan.zhihu.com/p/573340345#:~:text=NovelAI%E4%B8%AD%EF%BC%8C%20%7B%7D%E5%8F%AF%E4%BB%A5%E7%94%A8%E6%9D%A5%E5%A2%9E%E5%8A%A0%E6%9D%83%E9%87%8D%EF%BC%8C%E5%B0%B1%E6%98%AF%E4%BC%9A%E4%BC%98%E5%85%88%E7%94%9F%E6%88%90%E6%9C%89%E5%A4%A7%E6%8B%AC%E5%8F%B7%E7%9B%B8%E5%85%B3%E7%9A%84%E5%86%85%E5%AE%B9%E3%80%82%20%E6%AF%8F%E4%B8%AA%E5%A4%A7%E6%8B%AC%E5%8F%B7%E6%9D%83%E9%87%8D%E6%98%AF1.05%EF%BC%8C%E6%99%AE%E9%80%9A%E7%9A%84%E6%98%AF1%EF%BC%8C%E5%8F%AF%E4%BB%A5%E5%B5%8C%E5%A5%97%EF%BC%8C%E4%BE%8B%E5%A6%82%20%7B%20%7Bbondage%7D%7D,Stable-diffusion%E4%B8%AD%EF%BC%8C%E5%A2%9E%E5%8A%A0%E6%9D%83%E9%87%8D%E7%9A%84%E6%98%AF%E6%99%AE%E9%80%9A%E7%9A%84%20%E8%8B%B1%E6%96%87%20%E6%8B%AC%E5%8F%B7%20%28%29%EF%BC%8C%E4%B9%9F%E5%8F%AF%E4%BB%A5%E5%B5%8C%E5%A5%97%EF%BC%8C%E4%BE%8B%E5%A6%82%20%28%28bondage%29%29)

#### Parameters tuning

+ [如何评价AI绘画网站NovelAI？ - 知乎](https://www.zhihu.com/question/558019952/answers/updated)

+ [【NovelAI|Stable Diffusion】AI绘画调参搞出帅哥技巧【铜仁女狂喜】 - 知乎](https://zhuanlan.zhihu.com/p/572865961)


#### Resources
+ [NovelAI - The GPT-powered AI Storyteller](https://novelai.net/)
+ [Image Generation has arrived, NovelAI Diffusion is here! | Medium](https://blog.novelai.net/image-generation-announcement-807b3cf0afec)
+ NovelAI documentation
+ [Image Generation - NovelAI Documentation](https://docs.novelai.net/)
+ [Paint New Image - Edit Image - Canvas - NovelAI Documentation](https://docs.novelai.net/image/editimagecanvas.html#canvas--paint-new-image--edit-image)
+ [Novel AI搭建教程 - 哔哩哔哩](https://www.bilibili.com/read/cv19122535)
+ [【AI绘画】再次进化！novelai真官网版本解压即用 无需下载！这次1分钟内不用学也能会用_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1EV4y1L7dX/?vd_source=24df2e6861e218f2143199245603cf0c)
+ [AI 杀疯了，NovelAI开源教程_Jack-Cui的博客-CSDN博客_csnd](https://blog.csdn.net/c406495762/article/details/127419474)