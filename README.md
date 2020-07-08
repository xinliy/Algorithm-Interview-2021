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

* Xgboost的组件CART
- 用二分法切割特征空间
- 回归树最小化误差，分类树选择基尼指数最小的特征(feature impurity) Gini=1-sum(P_class**2)
