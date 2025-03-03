Rational Model

![image-20250228140330411](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228140330411.png)

![image-20250228140418530](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228140418530.png)

![image-20250228140432839](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228140432839.png)

![image-20250228140504568](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228140504568.png)

![image-20250228140546647](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228140546647.png)

![image-20250228140554211](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228140554211.png)

![image-20250228140642212](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228140642212.png)













Week 2 //2025.02.28

![image-20250228140706845](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228140706845.png)

![image-20250228140732798](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228140732798.png)

input：表 -- output： 表

![image-20250228141025690](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228141025690.png)

![image-20250228141430801](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228141430801.png)

![image-20250228141745770](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228141745770.png)

哈希/排序（去重）

如果不去重，可以看到数据分布；

![image-20250228142245235](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228142245235.png)

![image-20250228142312216](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228142312216.png)

![image-20250228142514643](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228142514643.png)

![image-20250228142727758](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228142727758.png)

![image-20250228142930146](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228142930146.png)

DBMS 给上层的API是解耦，根据信息决定最好策略（抽象）

θ是连接条件 Theta Join是导出OP

![image-20250228143315798](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228143315798.png)

Natural Join是Theta Join + Projection

共同属性是空的时候，theta是true，所有连接的tuples都直接 Cartesian Procuct

![image-20250228144123390](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228144123390.png)

![image-20250228144217614](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228144217614.png)

R 和S 有相同的Schema，两者属性相同

![image-20250228144355452](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228144355452.png)

下面的内容介绍的是**关系代数（Relational Algebra）\**在关系数据库查询中的基本概念和常见操作。关系代数是一种\**基于关系模型**的查询语言，用来对关系数据库（表）进行检索与操作。每一个操作都以一个或多个关系（表）作为输入，并输出一个新的关系（表）。通过组合多个关系代数操作，可以形成更复杂的查询逻辑。

以下是图片中列出的几种常见关系代数运算及其含义：

------

## 1. Selection (选择) — 记作  σP(R)\sigma_{P}(R)

- **定义**：从关系 RR（一张表）中，挑选出满足谓词（条件）PP 的所有元组（行）。
- **谓词 PP**：通常是对属性的条件判断，例如 `age > 30`、`gender = 'M'` 等等。
- **输出**：仍然是一个关系（表），但只包含那些满足条件的行，列与原表相同。
- **作用**：过滤表中的行。

示例：

σage>30(R)\sigma_{\text{age} > 30}(R)

表示从关系 RR 中选取 `age` 大于 30 的所有行。

------

## 2. Projection (投影) — 记作  πA1,…,Ak(R)\pi_{A_1,\dots,A_k}(R)

- **定义**：从关系 RR 中选取若干属性列 {A1,…,Ak}\{A_1,\dots,A_k\}，只保留这些列，去掉其他列。
- **输出**：新的关系只包含指定的属性列，行数可能会由于去重等原因发生变化（在关系代数中，投影会去除重复的元组）。
- **作用**：只保留我们关心的列，类似于 SQL 中的 `SELECT 列名列表`。

示例：

πname,age(R)\pi_{\text{name,age}}(R)

表示只从关系 RR 中保留 `name` 和 `age` 两列，其他列被丢弃。

------

## 3. Cartesian Product (笛卡尔积 / 直积) — 记作  R×SR \times S

- **定义**：给定两个关系 RR 和 SS，产生所有可能的行组合，即 RR 中的每一行与 SS 中的每一行配对组合。
- **输出**：一个新的关系，其中列是 RR 和 SS 的所有列，行数是 RR 的行数乘以 SS 的行数。
- **作用**：为后续的连接操作（Join）提供基础，也可以与选择（Selection）一起用来实现等值连接等复杂查询。

示例：
 R×SR \times S 表示对 RR 和 SS 进行所有行的组合。

------

## 4. Union (并集) — 记作  R∪SR \cup S

- **定义**：将两个**结构相同**的关系 RR 和 SS（即相同的属性列）合并起来，去掉重复的行。
- **输出**：新的关系包含了在 RR 和 SS 中出现过的所有行（不重复）。
- **作用**：整合两个相同模式的表，获得它们的并集结果。

示例：
 R∪SR \cup S 表示把 RR 中的行和 SS 中的行合并成一个关系。

------

## 5. Difference (差集) — 记作  R−SR - S

- **定义**：得到在 RR 中出现但在 SS 中**没有**出现的行（同样需要 RR 和 SS 模式相同）。
- **输出**：只包含属于 RR 而不属于 SS 的元组。
- **作用**：从一个关系中去除另一个关系里也出现的行。

示例：
 R−SR - S 表示从 RR 中去除所有也在 SS 中出现的行。

------

## 6. Renaming (重命名) — 记作  ρS(A1,…,Ak)(R)\rho_{S(A_1,\dots,A_k)}(R)

- **定义**：将关系 RR 重命名为关系 SS，同时可以将其属性（列）改名为 {A1,…,Ak}\{A_1,\dots,A_k\}。
- **输出**：一个和 RR 结构相同的关系，但关系名和属性名被更新了。
- **作用**：在复杂查询或多个子查询组合时，方便区分不同的关系；也可在连接或笛卡尔积操作时避免属性名冲突。

示例：

ρT(x,y)(R)\rho_{T(x,y)}(R)

表示把关系 RR 的名字改成 TT，同时把它的两个属性改名为 xx 和 yy（假设原本 RR 只有两列）。

------

## 组合运算与查询构造

- 由于每个操作输入和输出的都是关系，可以将它们依次组合（流水线化）来构造更复杂的查询。例如，可以先对一个表做选择筛选，再做投影，然后再与另一个表做笛卡尔积或连接，最后再对结果进行投影等等。
- 关系代数是理论层面的抽象模型，SQL 等具体查询语言在本质上都可通过这些基本操作组合来实现。

------

## 总结

- **关系代数**是一种用**基本操作**（如选择、投影、并集、差集、笛卡尔积、重命名）来表达查询的形式化方法。
- 每个操作以一个或多个关系作为输入，输出也是关系，使得查询能像积木一样组合、构造。
- 关系代数在数据库原理课程中是核心内容，有助于理解 SQL 查询背后的理论基础以及数据库查询优化器的工作原理。

MiniOB 101

![image-20250228145647086](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228145647086.png)



有一个表，一个属性A，tuples内容为1，7，2，8，全是数字，写一个表达式输出一个表，内容是第一个表的最大值

在**标准的关系代数**里并没有直接的“MAX”函数，但我们可以用下面的思路找出某属性的最大值：

> **思路**：
>
> 1. 将关系 RR 自身进行笛卡尔积（做成两个拷贝，分别命名为 R1R_1 和 R2R_2）；
> 2. 在笛卡尔积结果中，选出那些 R1.A<R2.AR_1.A < R_2.A 的元组，并投影出 R1R_1 这一边的 A 值；
> 3. 这些投影得到的值都是“小于某些别的 A 值”的行，把它们从原关系 R1R_1 中减去（差集）之后，剩下的就是“从不小于任何别的 A 值”的行——也即最大值所在的行（如果有多个并列最大值都会保留）。

------

以下是一种**完整的关系代数表达式**示例：

1. **先给原关系重命名**

   ρR1(R),ρR2(R)\rho_{R_1}(R),\quad \rho_{R_2}(R)

   这样就能区分同一个表的两份拷贝，分别叫做 R1R_1 和 R2R_2。

2. **找出所有“前者 A < 后者 A”的组合**

   σR1.A<R2.A(R1×R2)\sigma_{R_1.A < R_2.A}\bigl(R_1 \times R_2\bigr)

3. **投影得到所有“比别的元组更小”的 A 值**

   πR1.A(σR1.A<R2.A(R1×R2))\pi_{R_1.A}\Bigl(\sigma_{R_1.A < R_2.A}\bigl(R_1 \times R_2\bigr)\Bigr)

4. **用差集运算，去掉那些“小于别的元组” 的 A 值**

   R1  ∖  πR1.A(σR1.A<R2.A(R1×R2))R_1 \;\setminus\; \pi_{R_1.A}\Bigl(\sigma_{R_1.A < R_2.A}\bigl(R_1 \times R_2\bigr)\Bigr)

这里 R1∖…R_1 \setminus \dots 表示：把那些“曾出现在小于别的 A 值的集合里”的行去除掉，剩下的就是**从来不小于任何其它行**的元组，即**最大值**的行。

------

### 例子说明

假设原关系 RR 里只有一个属性 AA，且包含行 {1,7,2,8}\{1,7,2,8\}。那么：

1. 自身笛卡尔积后，得到 

   R1×R2R_1 \times R_2

   ：

   ```
   R_1.A   R_2.A
    1       1
    1       7
    1       2
    1       8
    7       1
    7       7
    7       2
    7       8
    2       1
    2       7
    2       2
    2       8
    8       1
    8       7
    8       2
    8       8
   ```

2. 选择满足 R1.A<R2.AR_1.A < R_2.A 的元组，例如 `(1,7), (1,8), (2,7), (2,8), (7,8)` 等等。

3. 投影出 R1.AR_1.A 就是那些“小于别的”的 A 值：{1,2,7}\{1,2,7\}。

4. 用差集把这些 A 值从原表里去除：{1,7,2,8}−{1,2,7}={8}\{1,7,2,8\} - \{1,2,7\} = \{8\}。这样得到的就是最大值 `8`。

如果原关系有多列或有多行并列最大值，使用该方法也同样能保留下所有最大值的元组。

![image-20250228150934327](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228150934327.png)

![image-20250228151105289](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228151105289.png)

单调的指的是在集合意义上的单调（即包含）

![image-20250228152111842](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228152111842.png)

![image-20250228152245199](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228152245199.png)

语义上等价，开销第二个更小；实际上跟data有关系，如果老师很多，课很少，则第一种开销更小，这是用RA写，用SQL写的机制，等价变换成开销最小== 查询优化器

用户的API进行查询Query == 》 根据data的统计信息 == 》生成最优计划

![image-20250228152717360](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228152717360.png)

![image-20250228152950044](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228152950044.png)

没有递归：优化简单；但有些事情表达不出来。

![image-20250228153349674](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228153349674.png)

![image-20250228153527627](C:\Users\15508\AppData\Roaming\Typora\typora-user-images\image-20250228153527627.png)
