---
layout:     post
title:      "Anaconda skills"
subtitle:   "some useful cmd"
date:       2018-05-19
author:     "Evan"
header-img: "img/post-bg-2015.jpg"
catalog:     true
tags:
    - skills
---

## About KERNEL

##### install

``` bash
python -m ipykernel install --user --name myenv --display-name "Python (myenv)"
```

##### uninstall 

```bash
jupyter kernelspec list
# list all kernels
jupyter kernelspec remove yourkernel
# remove kernel
```

## About VIRTUAL ENVIRONMENT

```bash
conda info -e
# list all your envs
conda create -n your_env_name python=X.X（such as 2.7、3.6）
# create envs
conda create -n your_env_name package --clone existing_env_name
# create a env from an existing env
```

## Export/Import packages-dependency

```bash
# export
source activate <environment-name>
conda env export >  <environment-name>.yml
# import
conda env create -f <environment-name>.yml
# Directly conda install, but this will result in failure of install
conda install --yes --file requirements.txt
# This will partly fix the problem above.
conda install --yes $requirement; done < requirements.txt



```
