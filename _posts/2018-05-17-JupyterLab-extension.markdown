---
layout:     post
title:      "JupyterLab extension && useful python package"
subtitle:   "JupyterLab扩展汇总以及包"
date:       2018-05-17 
author:     "Evan"
header-img: "img/post-bg-2015.jpg"
catalog:     true
tags:
    - 工具
---

# Visualization for the data

## plotly

pip install plotly 
jupyter labextension install @jupyterlab/plotly-extension

## matplotlib

使用%matplotlib inline进行激活

## bokeh

### init
 
``` python
from bokeh.io import push_notebook,show, output_notebook
from bokeh.layouts import row
from bokeh.plotting import figure
output_notebook()
```

# Visualization for the image

scipy

scikit-image

[demo](http://www.scipy-lectures.org/packages/scikit-image/index.html)

# LaTex

pip install jupyterlab_latex
jupyter labextension install @jupyterlab/latex

# magic

[the cell magics in ipython](http://nbviewer.jupyter.org/github/ipython/ipython/blob/1.x/examples/notebooks/Cell%20Magics.ipynb#The-cell-magics-in-IPython)