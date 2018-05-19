---
layout:     post
title:      "Anaconda skills"
subtitle:   "JupyterLab扩展汇总以及包"
date:       2018-05-19
author:     "Evan"
header-img: "img/post-bg-2015.jpg"
catalog:     true
tags:
    - skills
---

# About KERNEL

## install

``` bash
python -m ipykernel install --user --name myenv --display-name "Python (myenv)"
```

## uninstall 

```bash
jupyter kernelspec list
# list all kernels
jupyter kernelspec remove yourkernel
# remove kernel
```

# About VIRTUAL ENVIRONMENT

```bash
conda info -e
# list all your envs
conda create -n your_env_name python=X.X（such as 2.7、3.6）
# create envs
```
