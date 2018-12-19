---
layout: post
title: "[Deep Learning]Reading note on Linear Algebra "
subtitle: "Linear Algebra"
date: 2018-12-18
author: "Evan"
header-img: "img/post-bg-2015.jpg"
catalog: true
tags:
  - Machine Learning
  - Deep Learning
  - Linear Algebra
---

### 一 常见四种数学对象类型

1. 标量——小写斜体字表示
2. 向量——有序数组，小写粗体字表示

    用`集合`作为下标，表示向量中对应的元素组成的新向量。

    `集合前加负号`，表示向量中对应元素以外的元素组成的新向量。

3. 矩阵——二维数组，大写斜体字母表示

    `冒号`表示整行或列。

4. 张量——多维数组，用特殊字体表示



### 二 矩阵乘法和向量乘法

`转置`，是常用的矩阵操作。

`特别的`，深度学习中有一种操作，`矩阵加向量等于矩阵`。它意味着，矩阵的每一行都加上这个向量。

`元素积`，又称哈达玛积。

`点积`，又称内积。

### 三 单位矩阵和矩阵求逆

`单位矩阵`，主对角线上都是1，其余元素为0。

记作$I_{n}$。

`逆矩阵`，为$A^{-1}$。

逆矩阵满足$A^{-1}A=I_{n}$。

逆矩阵可用来求线性方程组，如果**系数矩阵可逆**的话。

### 四 线性相关和向量空间

线性方程组的系数矩阵A是可逆矩阵，才能通过矩阵求逆法求解。

### 五 范数

$$\lVert x \rVert _{p} = \sum _{i} \lvert x_i \rvert ^p \rgroup^{-\frac{1}{p}}$$

范数满足如下性质：
- x的范数为0，等价于x为0
- x与y的和的范数，小于等于x和y的范数和
- x的a倍的范数，等于x的范数的a的绝对值倍

常见的范数
- p=2，欧几里得范数，常用范数的平方数运算。
- p=1，用于区分0和极小非0数
- p=0，求解向量中非0元素的个数，常用L1范数代替。
- 最大范数，元素的最大绝对值
- 弗罗贝尼乌斯范数，矩阵所有元素的平方和开根号

范数形式下的点积公式：
$$x^Ty=\lVert x \rVert _2 \lVert y \rVert _2 cos \theta$$

### 六 特别的矩阵和向量

`对焦矩阵`，只有主对角线上的元素非0，记作$diag(v)$。

`对称矩阵`

`单位向量`，l2范数为1的向量

`正交矩阵`，$A^TA=AA^T=I$



### 七 特征分解

$$A=Vdiag(\lambda)V^{-1}$$

特征值对角矩阵约定具有递减顺序。

`正定矩阵`，矩阵的特征值都是正的。

`半正定矩阵`，矩阵的特征值是正数或者为0.

同理，还有负定矩阵，半负定矩阵。

### 八 奇异值分解

$$A=UDV^{T}$$

- U的列向量是左奇异向量，即$AA^T$的特征向量
- D是A的奇异值
- V的列向量是右奇异向量，即$A^TA$的特征向量
- 奇异值是$A^TA$的特征值

### 九 摩尔－彭若斯广义逆

解决奇异矩阵，或者非方阵的广义逆。

A的行比列更多时，用求伪逆方法求解。

`特别的`，用伪逆求解线性方程组的欧几里得范数最小值的解。

### 十 迹算子

矩阵主对角线上的和。

矩阵交换后的乘积的迹不变。

### 十一 行列式

det(A)



### 专业词汇 Specialized Vocabulary

| word           | meaning  |
| -------------- | -------- |
| linear algebra | 线性代数 |
scalar|标量
Cartesian product| 笛卡尔积
transpose| 转置
main diagonal|主对角线
shape|矩阵类型
matrix product| 矩阵积
element-wise product| 元素积
Hadamard product | 哈达玛积
dot product | 点积
associative|可组合性
distributive|可分配性
identity matrix | 单位矩阵
matrix inversion| 矩阵求逆
matrix inverse|逆矩阵
linear combination|线性组合
Linear Dependence|线性相关
span | 向量生成空间
singular | 奇异的,不可逆
norm |范数
Euclidean norm | 欧几里得范数
max norm| 最大范数
Frobenius norm|弗罗贝尼乌斯范数
symmetric matrix| 对称矩阵
unit vector|单位向量
orthogonal|正交
orthonormal|标准正交的
orthogonal matrix|正交矩阵
Eigendecomposition|特征分解
eigenvalues|特征值
eigenvectors|特征向量
positive definite|正定
singular value decomposition|奇异值分解
The Moore-Penrose Pseudoinverse|摩尔－彭若斯广义逆
pseudoinverse | 伪逆
Principal Components Analysis| 主成分分析



