基于环境的模型强化学习： 具身智能--多模态nero 基于sim的做planning

目标策动的层次化强化学习：（milestone）

模仿学习（现实环境，没有显式的奖励函数）：轨迹--模仿--泛化

太湖机器人（宁德时代）

多智能体强化学习（博弈）新的不确定性--环境非稳态

离线强化学习（offline 数据集）模拟与真实环境的交互效果，直接部署在真实测试环境中（工业环境中需要pretty fine的离线数据集）

large sequential model

![image-20250224160852354](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224160852354.png?raw=true)

![image-20250224160906587](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224160906587.png?raw=true)

有监督学习--预测接下来发生什么

解决样本复杂度的需求（基于模拟环境）

![image-20250224161035260](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224161035260.png?raw=true)

预测往后的encoder和decoder，循环

encoder离散化处理（聚类的token）RNN prediction更好 --> Sequence Model --> 未来Env -- > planning

DreamerV3

![image-20250224161338056](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224161338056.png?raw=true)

改变强化学习的范式 -- 目标 default goal ：maximum argument prediction reward function

具身智能 VRA model 写论文 LLMs -- prompt --Agent

![image-20250224161637003](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224161637003.png?raw=true)

achieve goal1 上层产生goal，下层产生action和新的goal

![image-20250224161740712](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224161740712.png?raw=true)

Imitation Learning： 调goal本身：人为驾驶车辆轨迹数据：policy 不如Experts

逆向学到reward function -- 正向强化学习-- tune --训练（RHLF）

![image-20250224161954946](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224161954946.png?raw=true)

London 做的极致 轨迹数据--逆向强化学习/模仿学习 -- 指导驾驶策略-- action

![image-20250224162127959](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224162127959.png?raw=true)

其他智能体正在学习 - non -stationary（环境也在变，对于每一个智能体而言都在变/博弈）/ dynamic（state tra）

![image-20250224162304826](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224162304826.png?raw=true)

![image-20250224162400151](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224162400151.png?raw=true)

![image-20250224162423951](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224162423951.png?raw=true)

优化过程不适合跨任务泛化/NLP 大sequence model基于范式做泛化

Alpha-go Deepseek

知识连通性 可能超越人（math code prediction/planning embodied）

application：交互环境生成：基于Mov推演 Generate a playable world set in a futuristic)

3D时间建模

application：环境游戏生成（引擎是NN给出的）diffusion google（前后都填空）

application： 聚变反应堆控制（AI4Sci）build a simulator 真实环境会浪费资源且有安全性问题

application：无人机体育竞技（灵活性）

application：控制机器狗跑酷（robot keeps re-trying）基于环境感知+运动控制

云深处--浙大老师/卷宇树（收集数据-模仿学习）

机器人进化速度太快了！

3A校友会博士论坛（动捕--强化学习）软件--全身协调控制

单脚跳--区别：没有任何reference motion，仅基于reward，角度/步态 take action

para 1MLP

VLA model （大脑控制）底层小脑控制

physical intelligence PI 家务

facebook

GPT-4 Technical Report

强化学习在大语言模型的落地 -pretraining loss

SFT/post training

![image-20250224170436108](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224170436108.png?raw=true)

DQN比MLA的创新弱多了

Deepseek 是掀桌子的技术（ML 学者）整个行业都变了

两层黑盒（环境的非稳态）

token（state 就叠一个token）

博士涉及强化学习 则被HR安排完了

探索未知环境产生新的数据和决策

Agent== LLM + interaction from fine-tuning + 交互环境（与调prompt无关）

探索与利用

强化学习的data来自于环境和智能体的交互/Agent 等级比较高/interaction产生新的知识 trade-off

![image-20250224171426347](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224171426347.png?raw=true)

舒适区（利用最大化但不容易以最高速率变强）

过于探索则不容易持续变强（policy没达到一定水平，策略的space是高维的）

T型人才：视野宽，某一领域精深

![image-20250224171803797](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224171803797.png?raw=true)

多臂老虎机（multi-armed bandit）问题的形式化描述

online learning

![image-20250224171931453](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224171931453.png?raw=true)

无state，只有认知（information state） 对于R（reward）的认知

背后有具体的二进制的（average reward是在很多次探索之后发现的）

which arm to take

![image-20250224172145211](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224172145211.png?raw=true)

![image-20250224172211267](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224172211267.png?raw=true)

![image-20250224172258883](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224172258883.png?raw=true)

懊悔值（相比于最优的收益的差）

![image-20250224172446204](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224172446204.png?raw=true)

trade-off sublinear regret 下界是log t

distribution很接近，则更难区分出来

![image-20250224172732253](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224172732253.png?raw=true)

ε -greedy

认知被贪心所限制 regret增长是linear的

ε -greedy policy to uniform / 积累了稳定的regret -- 衰减regret（exploration）

![image-20250224172936444](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224172936444.png?raw=true)

![image-20250224173140468](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224173140468.png?raw=true)

Naive method

New：早期

![image-20250224173208203](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224173208203.png?raw=true)

![image-20250224173313126](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224173313126.png?raw=true)

不确定性的测度

![image-20250224173406341](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224173406341.png?raw=true)

Standard Deviation

Sub-linear regret

![image-20250224173520555](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224173520555.png?raw=true)

![image-20250224173740349](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224173740349.png?raw=true)

![image-20250224173918153](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224173918153.png?raw=true)

采样范式一致

![image-20250224174009421](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224174009421.png?raw=true)

![image-20250224174140123](https://github.com/jasminejijiayi/SJTU-Courses/CS3316ReinforcementLearning/image/image-20250224174140123.png?raw=true)