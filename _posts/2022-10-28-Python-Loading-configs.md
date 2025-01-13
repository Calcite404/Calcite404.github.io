---

layout: post
title: Python Cooknotes 01 - reading configs from a file
toc: true
date: 2022-10-28
tags: [python, config, yaml]
---


### Scenario

When python reading a common config file by `configparser`, for example, a `config` setting file for Scanpy:

``` config.txt

has_spatial = True

...

marker = Human-CD163,Human-CD3,Human-CD19,Human-CD4

marker_types = {Tcell: [Human-CD3, Human-CD4], Bcell: [Human-CD19], Macrophages: [Human-CD163], Other: []}

...

```

, since `configparser` always return `str` object, this may results in potential issues should be considered:

+ `bool(False)` return `True`

+ return elements in a list that contains blank, quotation mark, line break and other special characters

![config example](/assets/collections/20221028112920.png)

### Solution
#### 1. `configparser`
This is my personal not so "elegant" solution.

+ For `bool` dtype, using `.getboolean()` method
+ For `list` dtype, transformation using `.split()` and `.strip()`
+ For `dict` dtype, using internal `ast` library

``` python
def getConfig(filename, section, option, dtype=None):
    import ast

    conf = configparser.ConfigParser()
    conf.read(filename)
    if dtype == bool:
        config = conf[section].getboolean(option)
    elif dtype == list:
        config = conf[section][option]
        config = [c.strip() for c in config.split(',')]
    elif dtype == dict:
        config = conf[section][option]
        config = ast.literal_eval(config)
    else:
        config = conf[section][option]
        config = config.strip('"\n\t ') #eval()
    return config
```

##### Reference
+ [https://favtutor.com/blogs/string-to-dict-python](https://favtutor.com/blogs/string-to-dict-python)
+ [configparser --- 配置文件解析器 — Python 3.10.8 文档](https://docs.python.org/zh-cn/3.10/library/configparser.html)
+ [python - Lists in ConfigParser - Stack Overflow](https://stackoverflow.com/questions/335695/lists-in-configparser)

#### 2. `yaml`

Here list an example from `pyyaml` document to show its organization way.
A block mapping may be nested in a block sequence:

```
# YAML
- name: PyYAML
  status: 4
  license: MIT
  language: Python
- name: PySyck
  status: 5
  license: BSD
  language: Python
```

+ read-in by python
```
# Python
[{'status': 4, 'language': 'Python', 'name': 'PyYAML', 'license': 'MIT'},
{'status': 5, 'license': 'BSD', 'name': 'PySyck', 'language': 'Python'}]
```

+ code-usage
``` python
import yaml
with open("./config/config.yaml", 'r') as stream: 
    config = yaml.safe_load(stream) 
```

##### Reference
+ [https://pyyaml.org/wiki/PyYAMLDocumentation](https://pyyaml.org/wiki/PyYAMLDocumentation)
+ [https://www.jianshu.com/p/eaa1bf01b3a6](https://www.jianshu.com/p/eaa1bf01b3a6)
+ [https://dreamhomes.top/posts/202104251804/](https://dreamhomes.top/posts/202104251804/)