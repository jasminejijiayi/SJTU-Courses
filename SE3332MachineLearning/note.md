![image-20250225075737193](D:\SJTU\SJTU-Courses\typora-user-images\image-20250225075737193.png)

![image-20250225080918463](D:\SJTU\SJTU-Courses\typora-user-images\image-20250225080918463.png)

generalization 代表模型represent 通用的feature 右边的模型虽然学到了各种细节，但未能学习数据的规律，在泛化性方面：低次> 高次 simple >difficult 需要对模型的复杂度进行控制



underfitting VS overfitting （模型的复杂度/相对于数据而言）

避免过拟合措施

1. 增加训练数据
2. 正则化（L1 & L2）
3. 数据划分 & 交叉验证 
4. 早停
5. 先验知识



措施1：数据划分

原因：模型拟合的是总体数据的分布而不仅仅是训练集的分布

为了评估泛化误差，需要在训练的时候保留一部分未知数据

数据划分（Hold-Out）

**good loss function** to indicate the performance of the predictive model over the whole-data distribution instead of the training data

措施2：交叉验证（Cross Validation）

数据规模小时，K-折交叉验证

措施3：早停（Early Stop）

措施4：正则化（Regularization)

![image-20250225083427115](D:\SJTU\SJTU-Courses\typora-user-images\image-20250225083427115.png)

2范数 1范数





机器学习核心要素

1. 数据（Experience）
2. 模型（Hypothesis）
3. 损失函数（Objective）
4. 优化算法（Improve）

regression 预测，归因分析，控制





Loss Function：MSE

improve--- GD
![image-20250225090211823](D:\SJTU\SJTU-Courses\typora-user-images\image-20250225090211823.png)

![image-20250225090645577](D:\SJTU\SJTU-Courses\typora-user-images\image-20250225090645577.png)

![image-20250225091239435](D:\SJTU\SJTU-Courses\typora-user-images\image-20250225091239435.png)

![image-20250225091719107](D:\SJTU\SJTU-Courses\typora-user-images\image-20250225091719107.png)

![image-20250225092107238](D:\SJTU\SJTU-Courses\typora-user-images\image-20250225092107238.png)

解析方法中如果不可逆，则需要GD来求解 -- 正则化（对损失函数引入一个惩罚项）

![image-20250225092700246](D:\SJTU\SJTU-Courses\typora-user-images\image-20250225092700246.png)

正则化: 模型惩罚-- 数据增强

![image-20250225093223923](D:\SJTU\SJTU-Courses\typora-user-images\image-20250225093223923.png)





![image-20250228101300957](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228101300957.png)





数据分布是非线性问题的时候 -- 怎么解决？

![image-20250228102124889](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228102124889.png)

![image-20250228102302673](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228102302673.png)

![image-20250228102458035](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228102458035.png)

![image-20250228102634313](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228102634313.png)

![image-20250228103021945](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228103021945.png)

刻画纯度的指标：信息熵

![image-20250228103310614](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228103310614.png)

数据越纯 -- 信息熵越小

![image-20250228103553322](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228103553322.png)

子数据集的信息熵 -- 加权平均

![image-20250228103858499](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228103858499.png)

![image-20250228104325763](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228104325763.png)

![image-20250228104431219](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228104431219.png)

![image-20250228105739566](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228105739566.png)

![image-20250228105936728](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228105936728.png)

![image-20250228110109569](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228110109569.png)

![image-20250228110339455](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228110339455.png)

![image-20250228110622311](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228110622311.png)

解决过拟合的方法：随机森林

![image-20250228110753866](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228110753866.png)

![](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228111652505.png)

![image-20250228111822169](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228111822169.png)

![image-20250228111847347](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228111847347.png)

![image-20250228111902320](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228111902320.png)

![image-20250228112020154](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228112020154.png)

![image-20250228112310577](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228112310577.png)

![image-20250228112339421](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228112339421.png)

![image-20250228112348808](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228112348808.png)

![image-20250228112746401](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228112746401.png)

![image-20250228112903494](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228112903494.png)

![image-20250228113042677](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228113042677.png)

**贝叶斯**方法是一种生成模型，旨在通过学习**数据的联合概率分布**来进行预测和推断。 与判别模型（如支持向量机）不同，贝叶斯方法关注的是**数据生成**的过程，即如何从**潜在的概率分布**中生成观测数据。 这使得贝叶斯方法能够处理复杂的概率分布和变量之间的依赖关系，即使数据在特征空间中无法线性或递归地分离。 通过建模这些复杂的依赖关系，贝叶斯方法能够捕捉数据中的潜在模式，从而在分类、回归等任务中表现出色。

**参数是x,y的概率分布**

概率论的视角下：Loss Function 是概率最大化的问题

**常见的贝叶斯损失函数：**

1. **平方误差损失函数（Squared Error Loss）：**

   - 用于最小化预测值与真实值之间的平方差。
   - 贝叶斯估计中的后验均值（Posterior Mean）是最小化平方误差损失的估计量。
   - 该损失函数对异常值敏感，可能导致对离群点的过度拟合。

2. **绝对误差损失函数（Absolute Error Loss）：**

   - 用于最小化预测值与真实值之间的绝对差。
   - 贝叶斯估计中的后验中位数（Posterior Median）是最小化绝对误差损失的估计量。
   - 该损失函数对异常值的敏感性较低，适用于对离群点具有鲁棒性的情况。

3. **0-1损失函数（0-1 Loss）：**

   - 用于分类问题，衡量预测是否与真实类别一致。
   - 贝叶斯估计中的最大后验概率（MAP）估计量是最小化0-1损失的估计量。
   - 该损失函数在实际应用中可能导致优化困难，因为其不连续性和非凸性。

   ![image-20250228113723903](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228113723903.png)

朴素贝叶斯分类：

朴素贝叶斯分类器（Naive Bayes Classifier）是一种基于贝叶斯定理的概率分类方法，其核心思想是：在给定类别的条件下，特征之间相互独立。

**贝叶斯定理简介：**

贝叶斯定理描述了在已知某些条件下，事件发生的概率。其数学表达式为：

P(C∣X)=P(X∣C)⋅P(C)P(X)P(C|X) = \frac{P(X|C) \cdot P(C)}{P(X)}

其中，P(C∣X)P(C|X) 是在特征 XX 给定的条件下，类别 CC 发生的后验概率；P(X∣C)P(X|C) 是在类别 CC 给定的条件下，特征 XX 发生的似然概率；P(C)P(C) 是类别 CC 的先验概率；P(X)P(X) 是特征 XX 的边际概率。

**朴素贝叶斯分类器的工作原理：**

1. **训练阶段：**

   - **计算先验概率：** 统计训练数据中各类别的出现频率，计算每个类别的先验概率 P(C)P(C)。
   - **计算条件概率：** 在每个类别下，统计各特征的出现频率，计算每个特征在该类别下的条件概率 P(Xi∣C)P(X_i|C)。

2. **预测阶段：**

   - 对于待分类样本 X=(X1,X2,…,Xn)X = (X_1, X_2, \dots, X_n)，计算其在各类别下的后验概率：

     P(C∣X)∝P(C)⋅∏i=1nP(Xi∣C)P(C|X) \propto P(C) \cdot \prod_{i=1}^{n} P(X_i|C)

   - 选择具有最大后验概率的类别作为预测结果。

**朴素贝叶斯分类器的优点：**

- **简单高效：** 算法实现简单，计算效率高，适用于大规模数据集。
- **处理缺失数据：** 能够处理缺失数据，对于缺失的特征，模型会自动忽略其对分类结果的影响。
- **适用于高维数据：** 在特征维度较高的情况下，仍能保持良好的分类性能。

**朴素贝叶斯分类器的缺点：**

- **特征独立性假设：** 假设特征之间相互独立，这在实际应用中往往不成立，可能影响分类性能。
- **对零概率敏感：** 如果某个特征在训练集中未出现过，可能导致其条件概率为零，从而影响分类结果。为解决此问题，通常采用拉普拉斯平滑技术。

**应用场景：**

朴素贝叶斯分类器广泛应用于文本分类（如垃圾邮件过滤）、情感分析、医疗诊断等领域。

总之，朴素贝叶斯分类器是一种基于概率理论的简单而有效的分类方法，尽管其特征独立性假设在实际中可能不完全成立，但在许多实际应用中仍能取得令人满意的分类效果。

![image-20250228114041753](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228114041753.png)