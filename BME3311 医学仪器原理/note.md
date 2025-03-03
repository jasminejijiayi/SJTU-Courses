![image-20250224140258031](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224140258031.png)

![image-20250224140600064](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224140600064.png)

人体不是导体但是有良好的导电性；人是容积导体；

心脏电压在人体表不同位置电压不相等；

心房发生去极化，心室产生去极化，心脏电荷位置在变化，无法通过单一电荷模型进行模拟；我们一般通过偶极，则电场会产生电矢量；用这个矢量描述心脏产生的等效电场；体表找几个位置测量电压进而测量电矢量进行建模（不一定有意义，医生关心的是PQSR波和病症的对应）

Einthoven三角形 （三个单极导联和三个双级导联）

导联：心电图机的正负段（电压表）右腿接地

单极导联：右腿固定电位负端接地，右手正端输入

双级导联：右手正端，左手负端，一起接入心电图测量端

Ⅰ导联：右手 -> 左手（矢量描述） Ⅰ = V_l - V_r （单方向的分量）

Ⅱ导联：右手 -> 左腿

Ⅲ导联：左手 - >左腿

4个电极描述出6个不同分量 （测量是有噪声）= 》 偶极电场

在某一个导联里面的心电图（例如P波）清晰信息程度不同

单极导联：只接右手（测量的是右手相对于右腿的相对矢量分量）

临床多用12导联（右腿经常不接，3个电极，另外一个中心电端参考端，胸前6个电极）

![image-20250224142344909](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224142344909.png)

电线流过的时候有感应电荷会有电容，右腿整体点位会有抬升，在单极导联的时候会产生共模噪声。

Wilson中心电端（**3个肢体端电压的平均值**）作为参考端：未接平衡电阻时相对心脏电压不同

### 差值的忽略：（10+~100+欧姆）

在理论上，由于电阻的数值选择和电流分配的方式，电压差异非常小，因此通常认为它们对整体测量的影响可以忽略不计。通过**串联一个较大的电阻**，可以有效降低不匹配的影响，尤其是当电流通过电阻时，电压的变化在设计范围内是微小的。

### 原因：

- **电流路径的平均**：电阻的加入使得电流分配均匀，避免了某一电极的电压由于电阻过大或过小而过度衰减或放大的问题。
- **共模抑制**：因为每个电极与其他电极的电压比较接近，Wilson中心电端通过这种配置减少了干扰和噪声。

为什么信号源信号不能过大？

输出电阻和输入电阻一样大时，信号会损失很多，检测端电压会很小（5~300kΩ）

参考端电压会更加稳定（相对于右腿接地）

why Wilson中心电端（**3个肢体端电压的平均值**）

心电图机电阻无穷大，信号是有衰减的，V_m = 2/3 V_RA - 1/3(V_LA + V_LL)

所以我们采用加压导联，能使得信号幅值增加150%，提高50%信号利用率，Ⅰ Ⅱ Ⅲ导联是单极导联

右手 左手 左腿的**加压导联** 都是单极导联（参考端是另外两个电极的平均值）



**加压导联**（Augmented Leads）是心电图（ECG）系统中的一种特殊类型的导联，用于通过加大某些导联的电压幅度来增强心电图信号的可视性。加压导联是在传统的标准肢体导联（I、II、III）基础上引入的，通过使用特定的电压放大技术来增加信号幅度，从而更加清晰地显示心脏的电活动。

### 1. **加压导联的工作原理：**

加压导联使用单极导联的技术，并通过将特定的电极电压加以放大来产生更强的信号。具体来说，它通过改变电极接入方式和通过电流合成来获得更高的信号强度。

加压导联有三种主要类型，它们分别是：

- **aVR（增强右臂导联）**
- **aVL（增强左臂导联）**
- **aVF（增强左脚导联）**

### 2. **加压导联的公式：**

加压导联的电压是通过从单极电极（例如右臂、左臂、左脚）接收到的信号和其他两个肢体电极的组合来计算的。其公式如下：

#### aVR:

VaVR=VRA−(VLA+VLL)2V_{aVR} = \frac{V_{RA} - (V_{LA} + V_{LL})}{2}VaVR=2VRA−(VLA+VLL)

即：通过右臂电极的信号减去左臂和左脚电极的平均值来得到aVR信号。

#### aVL:

VaVL=VLA−(VRA+VLL)2V_{aVL} = \frac{V_{LA} - (V_{RA} + V_{LL})}{2}VaVL=2VLA−(VRA+VLL)

即：通过左臂电极的信号减去右臂和左脚电极的平均值来得到aVL信号。

#### aVF:

VaVF=VLL−(VRA+VLA)2V_{aVF} = \frac{V_{LL} - (V_{RA} + V_{LA})}{2}VaVF=2VLL−(VRA+VLA)

即：通过左脚电极的信号减去右臂和左臂电极的平均值来得到aVF信号。

### 3. **加压导联的优缺点：**

#### 优点：

1. **增强信号强度**：由于加压导联通过放大信号幅度，它们使得心电图中难以察觉的波形（如低幅度波形或细小的P波和T波）变得更加明显，从而有助于更清晰地检测和分析心脏的电活动。
2. **提高诊断精度**：增强信号能够让医生更容易发现心脏问题，如心律不齐、传导障碍等。加压导联能够提供更多的信息，尤其是在某些特定区域（如心房、心室电活动）上，能够对心电图的解读提供支持。
3. **简化检测过程**：加压导联可以有效增强电图中的微弱信号，使得在一些心脏疾病或异常的检测中更为简便。
4. **常规心电图检测中的标准配置**：在标准12导联心电图中，加压导联是常用的一部分，广泛应用于临床实践。

#### 缺点：

1. **信号失真**：加压导联通过放大信号来增强电压幅度，但这也可能导致信号的失真，尤其是在信号本身含有噪声的情况下，放大噪声可能会影响最终结果。
2. **对电极放置要求高**：加压导联需要对电极的准确放置有所要求。如果电极放置不当，可能会导致信号不清晰或产生误导性结果。
3. **可能对共模干扰敏感**：在某些情况下，加压导联对共模噪声（例如由外部电器设备引起的噪声）可能较为敏感，尤其是在环境噪声较大的临床环境中。
4. **对低电压信号的放大效果有限**：在某些情况下，放大低电压信号可能并不完全有效，尤其是在电极接触不良或信号较弱时。



除了双极肢体导联和加压导联之外，还有单极胸导联。

另外6个导联是胸导联（胸不是一个简单的球型），心室附近增加6个导联。

![image-20250224144515547](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224144515547.png)

12个不同方向的电矢量变化情况









如何测量：

![image-20250224144855983](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224144855983.png)

隔离与保护（有源仪器大部分为Ⅱ类以上）-- 光电转换

电 -- 光 （无接触传播）-- 电

信号检测： 前置放大 -- 高通滤波 / 快速恢复 -- 陷波器（电源干扰） -- 增益控制（量程匹配）

生物电放大器

心电图机设计：

（基本参数和特点）![image-20250224145611393](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224145611393.png)

1. 心电信号放大
2. 抑制干扰（高的共模抑制比）（噪声控制）
3. 避免可能对患者和仪器本身造成的损坏和伤害（安全性）



要点：

导联 -- 导电凝胶

生物电位放大器 

生物信号特征：低频微弱信号（提高到要求的强度和信噪比）

生物电位放大器：前置级--差分放大电路（要求：高输入阻抗，高增益，高共模抑制比）

滤波器

接地

隔离屏蔽

![image-20250224150308972](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224150308972.png)

人体阻抗 就是 信号源阻抗 （低频信号）

心电图机阻抗要远高于人体阻抗

高频信号一般阻抗都比较小（电容绝缘，但高频信号可通过）

![image-20250224150558333](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224150558333.png)

模电攻击...



![image-20250224151040412](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224151040412.png)

![image-20250224151202473](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224151202473.png)

差分放大器

![image-20250224151452501](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224151452501.png)

反向放大器 三运放达到需要的输入阻抗和增益，一个运放达到高共模抑制比

![image-20250224152414067](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224152414067.png)

阻抗不平衡会产生额外的差额输出

外部电磁场 -- 交流电场 -- 左右手电流一样，电阻不同 -- 左右手电压不同（共模抬升的数值不一样）--转化成差模输入（误差）【Wilson电阻匹配的意义 】



![image-20250224152822753](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224152822753.png)

对抗干扰

1. 50Hz的工频干扰（power frequency common mode interference） 位移电流-- 共模干扰 差模干扰--电压耦合（电阻抗的匹配） 磁场引起的差模干扰（电磁感应--磁通量变化--电压差） 作业

   ![image-20250224153247088](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250224153247088.png)

   作业1：










![image-20250227140121707](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227140121707.png)

![image-20250227140140850](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227140140850.png)

前置放大--微弱信号放大--提高共模抑制比（80db-- 共模是1，差模是10000）

加法器（让所有输入信号方法之后信号大于0）

输入：成人心电信号幅度 

调制：微弱信号+高频信号做载波

电压信号控制光电二极管，随电压，光强会变亮和变暗；

解调：把低频信号从高频信号中提取出来

减法器：得到前置放大以后的信号

低通滤波：把高频信号滤波掉

![image-20250227140743356](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227140743356.png)

前端电阻比较小的时候，信号源没有内阻，利用单运放差分放大器；

压力传感器--电桥电路--单运放

![image-20250227141403288](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227141403288.png)

好处：加了一个放大器的内阻（加了两个跟随器）

共模抑制比

共模增益是1，差模增益与阻值有关

![image-20250227141722860](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227141722860.png)

![image-20250227142010384](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227142010384.png)

![image-20250227142252118](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227142252118.png)

U2的作用是调频调制，另一端要有一个光电敏感传感器；

U3是光电隔离的装置

U4的作用是解调；减法器对应的是加法器的反向。

![image-20250227143153869](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227143153869.png)

共模噪声转换为差模噪声，Wilson中心电端--电阻值匹配

电极和皮肤接触的电阻可能引入差模的干扰。

金属屏蔽箱：电流不会在人体上感应电流

导线需要有屏蔽层，金属铜网+真正导线，感应电荷接入大地流走

50Hz的陷波器（Band-stop）强制去掉（明确特点：主要噪声频率）

滤波器设计和参数很重要：否则容易使得信号变形

![image-20250227144225466](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227144225466.png)



![image-20250227144235368](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227144235368.png)

容易受到其他仪器的干扰（如果不接入一样的地）

右腿驱动电路：

![image-20250227144602584](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227144602584.png)

直接右腿接地：共模信号会抬升人体电位，如果电阻不匹配会转化成差模信号，Wilson中心电位会解决转化成差模信号的问题；但也可以使用 右腿不直接接地，我们的目标是测量V3和V4的电压差，右腿驱动电路：在三运放的基础上增加一个辅助运算放大器。组成的负反馈电路。

![image-20250227145223392](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227145223392.png)

![image-20250227145937497](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227145937497.png)

![image-20250227145949522](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227145949522.png)

耐极化电压300mV

![image-20250227150319367](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227150319367.png)

![image-20250227150459974](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227150459974.png)

![image-20250227150831269](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227150831269.png)

想办法把母亲心率减掉

![image-20250227151411755](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227151411755.png)

![image-20250227151543915](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250227151543915.png)

无创脑电检测；幅度比心电更小，频率范围不一样







Week3 2025.03.03

![image-20250303140433404](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303140433404.png)

![image-20250303141415170](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303141415170.png)

![image-20250303141711695](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303141711695.png)

![image-20250303142324680](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303142324680.png)

单极导联对于共模抑制的作用不太好



![image-20250303143216579](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303143216579.png)

![image-20250303143507306](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303143507306.png)

![image-20250303143801221](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303143801221.png)

![image-20250303144022752](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303144022752.png)

![image-20250303145413453](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303145413453.png)

生物电信号 -- > 

![image-20250303145632791](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303145632791.png)

![image-20250303145935139](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303145935139.png)

![image-20250303150952344](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303150952344.png)

![image-20250303151324077](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303151324077.png)

![image-20250303151441420](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303151441420.png)

![image-20250303151758645](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303151758645.png)

![image-20250303152552501](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303152552501.png)

![image-20250303153132530](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250303153132530.png)