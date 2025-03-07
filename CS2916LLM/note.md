![image-20250227180843950](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227180843950.png)

RNN 第一个“被淘汰”的架构

![image-20250227181028368](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227181028368.png)

不管句长，维度总是一定的

![image-20250227181015894](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227181015894.png)

序列 组合爆炸 

![image-20250227181052017](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227181052017.png)

![image-20250227181100402](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227181100402.png)

LSTM，GRU 都是RNN的一种

![image-20250227181125155](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227181125155.png)

vocab每一个列向量对应一个词，词表大小对应有多少列，多少行是指定的，查表使得把词语从离散的符号转换成连续的向量

![image-20250227181352398](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227181352398.png)

参数的权重是序列共享的（沿着时序），假设不同词语的语义共享，Hidden Vector是有一定的位置信息的，对于句子给一个向量；只用h4作为句子的表示，循环神经网络对于句子进行建模

![image-20250227181750381](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227181750381.png)

![image-20250227182005447](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227182005447.png)

![image-20250227182218147](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227182218147.png)

![image-20250227182345155](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227182345155.png)

激活函数的导数一般小于1

![image-20250227182435209](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227182435209.png)

![image-20250227182446625](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227182446625.png)

![image-20250227182545032](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227182545032.png)

![image-20250227182650919](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227182650919.png)

RNN，Xt H(t-1) --> H(t)

![image-20250227183038723](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227183038723.png)

![image-20250227183139607](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227183139607.png)

Feature -- Structure

![image-20250227183521929](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227183521929.png)

![image-20250227183814690](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227183814690.png)

![image-20250227184008480](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227184008480.png)

MLP,FeedForward,LCM的作者

World Model

LTSM（文本）-- CNN（卷积） -- Transformer

![image-20250227184441753](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227184441753.png)

![image-20250227185752997](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227185752997.png)

![image-20250227185824017](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227185824017.png)

没太多先验的是Transformer

![image-20250227185931006](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227185931006.png)

![image-20250227190045250](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227190045250.png)

CNN比RNN超参数多

![image-20250227190210459](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227190210459.png)

步数==2

![image-20250227190429779](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227190429779.png)

![image-20250227190509658](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227190509658.png)

![image-20250227190619787](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227190619787.png)

![image-20250227190639363](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227190639363.png)

解决变长问题

![image-20250227190715284](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227190715284.png)

![image-20250227190847339](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227190847339.png)

![image-20250227191135733](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227191135733.png)

![image-20250227191336158](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227191336158.png)

![image-20250227191705953](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227191705953.png)

Colonel

![image-20250227192159811](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227192159811.png)

![image-20250227192301962](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227192301962.png)

![image-20250227192344841](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227192344841.png)

Activation -- Weight

Hidden Vector -- Weight

Fast Weight  

参数和状态之间找到另一个状态

一个网络的权重是另一个网络的输出

![image-20250227192625999](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227192625999.png)

![image-20250227192649758](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227192649758.png)

![image-20250227192733735](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227192733735.png)

![image-20250227192818481](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227192818481.png)

Sequence -- Tree -- Graph

句法依存 -- Stanford

![image-20250227193213914](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227193213914.png)

![image-20250227193349228](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227193349228.png)

![image-20250227193402637](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227193402637.png)

![image-20250227193521318](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227193521318.png)

![image-20250227193634078](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227193634078.png)

![image-20250227193723636](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227193723636.png)

![image-20250227193758186](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227193758186.png)

![image-20250227193846202](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227193846202.png)

![image-20250227193932312](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227193932312.png)

![image-20250227193943119](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227193943119.png)

不可计算！

![image-20250227194010013](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227194010013.png)

![image-20250227194048711](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227194048711.png)

![image-20250227194100311](D:\SJTU\SJTU-Courses\typora-user-images\image-20250227194100311.png)

神经语言模型

Attention Transformer 袁仲翰老师

预训练







Week 3 2025.03.03

![image-20250303080146652](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303080146652.png)

![image-20250303080302068](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303080302068.png)

![image-20250303080441057](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303080441057.png)

![image-20250303080459749](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303080459749.png)

Seq2Seq 顺序输入 顺序输出 Encoder--Decoder

机器翻译之前 序列标注 文本分类



![image-20250303081122616](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303081122616.png)

LSTM 

Attention

![image-20250303081331123](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303081331123.png)

双向LSTM：（正反两个方向读取）句子所属类别的分类

局限：假设序列中间的某个词对于结果的影响，最中心的词语要走很多步，可能会有梯度爆炸和梯度消失；很难让分类效果优化，难以解决。

缓解：hidden-step做一个max-pooling

Attention：

![image-20250303082106471](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303082106471.png)

![image-20250303082227744](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303082227744.png)

![image-20250303082554481](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303082554481.png)

对Encoder的Hidden step加权求和得到单个Vector，给Decoder的Hidden step

Weight是model自己学的；Alignment要做好

![image-20250303083129910](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303083129910.png)

Context 是前面的线性加权求和，alpha通过Softmax计算，Softmax输入是s_i-1和y_i-1,

![image-20250303083332697](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303083332697.png)

第一版的2014的RNN

![image-20250303083532542](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303083532542.png)

![image-20250303083542270](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303083542270.png)

建立有效跳连

![image-20250303083647026](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303083647026.png)

在Encoder里面实现Self-Attention‘

![image-20250303083739863](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303083739863.png)

![image-20250303083823528](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303083823528.png)

![image-20250303083922956](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303083922956.png)

![image-20250303084023203](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303084023203.png)

![image-20250303084057250](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303084057250.png)

动态计算加权

RNN拿掉换成professional embedding 

-- Transformer

![image-20250303084227444](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303084227444.png)

![image-20250303084254543](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303084254543.png)

QKV 向量内积

3个Attention的作用不同；Decoder的顺序解码

![image-20250303085645221](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303085645221.png)

![image-20250303085815054](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303085815054.png)

![image-20250303085949899](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303085949899.png)

![image-20250303090620590](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303090620590.png)

![image-20250303090735146](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303090735146.png)



![image-20250303091046706](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303091046706.png)



![image-20250303091112413](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303091112413.png)

![image-20250303091135888](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303091135888.png)

![image-20250303091413335](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303091413335.png)

![image-20250303091548523](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303091548523.png)

![image-20250303091637139](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303091637139.png)

![image-20250303091916596](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303091916596.png)

![image-20250303092335795](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303092335795.png)

![image-20250303092625639](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303092625639.png)

![image-20250303092749942](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303092749942.png)

![image-20250303092821530](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303092821530.png)

![image-20250303093057421](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303093057421.png)

![image-20250303093432955](D:\SJTU\SJTU-Courses\typora-user-images\image-20250303093432955.png)