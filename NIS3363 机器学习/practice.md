Logistic Regression 逻辑回归

二分类问题

线性回归在有些时候可以处理二分类问题 make sense

二分类问题需要得到的是【0，1】的概率

把线性回归的值映射为概率（Sigmoid），即把实数空间的输出映射到概率【0，1】

逻辑回归的logit函数是怎么来的？

probability

odds：p/(1-p) [0,∞]

伯努利分布：p,1-p

对于odds取自然对数Ln -- Logit(p) = Ln[p/(1-p)] = z

p = 1/(1+exp^(-z))  == Sigmoid

目标函数：Target 极大似然估计

概率密度函数 -- 正态分布 -- 

概率：已知概率分布参数，预测观测的结果

似然：已知观测出的结果，估计观测结果所属于的概率分布



机器学习最常见的构建目标函数的方法：最大似然估计



ln的累乘转换为ln外的累加

Cross Entropy 交叉熵损失函数 -- 两个伯努利的分散程度，希望熵越小越好

Distribution （真实和拟合）Target 和 Model预测之间

GD：



假如用SE作为Logistic Regression的loss function

GD过程中：梯度在二分类中走不动



Sigmoid

逻辑回归是线性分类器

决策边界（Decision Boundary） 在决策边界上两种类别概率相同。



softmax是神经网络最后层用到的。 避免负数和零的情况，拉大数据差距。

numpy在维度上有broadcasting机制