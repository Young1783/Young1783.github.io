---
layout:     post
title:      "LaTeX Usage"
subtitle:   "An efficient method of writting an Academic Paper"
date:       2018-05-08
author:     "Evan"
header-img: "img/post-bg-2015.jpg"
catalog:    true
tags:
    - 技术使用
---


# LaTeX的介绍


> Wikipedia:
> 
> LaTeX (a shortening of Lamport TeX) is a document preparation system. When writing, the writer uses plain text as opposed to the formatted text found in WYSIWYG ("what you see is what you get") word processors like Microsoft Word, LibreOffice Writer and Apple Pages. The writer uses markup tagging conventions to define the general structure of a document (such as article, book, and letter), to stylise text throughout a document (such as bold and italics), and to add citations and cross-references. A TeX distribution such as TeX Live or MikTeX is used to produce an output file (such as PDF or DVI) suitable for printing or digital distribution. Within the typesetting system, its name is stylised as LATEX.
> 


> 维基百科：
> 
> LaTex(Lamport Tex的简写)是一个文档准备系统。当写作时，作者使用纯文本而不是所见即所得的格式化文本文字处理器，就像微软的word，LibreOffice的Writer和苹果的Pages。作者使用标记标签约定以定义文本的基本结构（诸如文章，图书，信件），和通过文档风格化文本（就像加粗，倾斜），和添加引文交叉引用。诸如Tex Live或者MikTex这样的TeX的发行版本被用来导出文件（pdf或者DVI格式）适合用来打印或者数字发行的。在这个类型预定义的体系里，它的名字被风格化为LATEX
> 

# 学习LaTeX的目的

只需要关注学术论文的内容，而减少大量的花费在排版上的时间成本。

# 系统环境

> 操作系统：Windows
> 
> 编辑器：Visual Studio Code
> 
> 扩展/插件：LaTeX Workshop
> 
> LaTex编译器:
>  > 前提：perl/MikTeX
> 
> XeLaTex
>
> pdf阅读器：福晰阅读器

# LaTeX的使用

Google it 

# VS code's Settings
```
    "latex-workshop.view.pdf.viewer": "external",
    "latex-workshop.latex.clean.enabled": true,
    "latex-workshop.latex.clean.fileTypes": 
    [
        "*.aux",
        "*.bbl",
        "*.blg",
        "*.idx",
        "*.ind",
        "*.lof",
        "*.lot",
        "*.out",
        "*.toc",
        "*.acn",
        "*.acr",
        "*.alg",
        "*.glg",
        "*.glo",
        "*.gls",
        "*.ist",
        "*.fls",
        "*.log",
        "*.fdb_latexmk",
        "*.synctex.gz"
    ],
    "latex-workshop.view.pdf.external.command": {
        "command": "FoxitPhantomPDF.exe",
        "args": [
            "%PDF%"
        ]
    },
    "latex-workshop.latex.tools": [
        {
            "name": "latexmk",
            "command": "latexmk",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-pdf",
                "%DOC%"
            ]
        },
        {
            "name": "pdflatex",
            "command": "pdflatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOC%"
            ]
        },
        {
            "name": "bibtex",
            "command": "bibtex",
            "args": [
                "%DOCFILE%"
            ]
        },
        {
            "name": "xelatex",
            "command": "xelatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOC%"
            ]
        }
    ],
    "latex-workshop.latex.recipes": [
        {
            "name": "xelatex",
            "tools": [
                "xelatex"
            ]
        },
    ],
```  