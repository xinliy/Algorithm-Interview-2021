# Algorithm-Interview-2021
Collection of algorithm interview questions

This is a repo for me to collect and answer questions of algorithm job 2021

1. 生成模型和判别模型基本形式，有哪些?

- 给定 带标记的样本的联合分布P(X,Y), 模型直接学习一个函数令 Y=f(X) 是判别模型 （decision boundary）；
- 若通过已知数据（训练集）来算出P(Y'|X')以此估算联合分布P(X,Y)是生成模型。

2. 核函数的种类和应用场景？
- 线性核（样本多或特征多）
- 多项式核-
- 高斯核（特征少）

3. 说一下 Xgboost 原理，为什么好？
- 使用了boosting原理，串联决策树，每一颗新的树都对原模型表现最差的样本着重优化
- 梯度下降时同时考虑了泰勒展开的一阶和二阶导数。
- 目标函数是预测距离+正则化树的复杂度
- 设置阈值防止过拟合(树的深度，分裂需要的最小样本数等）

ex: Xgboost的组件CART
- 用二分法切割特征空间
- 回归树使用最小二乘法，分类树选择基尼指数最小的特征(feature impurity) -> Gini=1-sum(P_class**2)

4. 什么是过拟合？
- 由于样本空间和实际变量分布的错位**数据不完备是原因**，模型只能够学习到样本空间的分布
- 模型过度记忆了样本数据的特征
- 当过拟合时，模型最小化训练误差（预测到样本的距离），但是方差变大（样本变动导致模型的变动），泛化能力变差

ex: 过拟合解决方案
- 增加训练集
- 正则化(Normalization,Dropout)
- 用交叉验证找到合适的停止训练点，或者平均模型

