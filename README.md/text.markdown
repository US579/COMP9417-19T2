# comp9417


## Week1 **liner regression**

### regression task 

- 类别

	- Supervised learning

		- output class is  given 有label

	- Unsupervised learning 

		- output class is  given 无label

- representation

	- symbolic representations

		- 在假说的空间搜索

	- numeric representations

		- 在函数的空间搜索(找到最适合这个数据的function)

- regression equation

	- weight 和 value 加和的表达形式

		- 
![](assets/F4B9787B-445D-4D5D-B917-915791CDB1F9.png)

		- 
![](assets/98CDAC22-20CF-4122-BEE7-43720D140CAB.png)

	- 误差平方和

		- 
![](assets/3985B27A-34D9-481A-96F6-AC02F943074E.png)

			- 真实值减去预测值的平方在求和(来确定b的组合是否与数据集吻合) 找到b的值能使左边这个等式最小

- 估计estimator

	- mean

	- variance

		- 
![](assets/F4B75510-BC60-4504-A80F-21291FED278A.png)

		- 
![](assets/F3DF3367-4B4B-4014-8271-B9B4777112D7.png)

			- 无根号的话就是标准差

	- covariance

		- 
![](assets/530312C4-AA6C-4BF4-8AE4-DABEF8DC232C.png)

			- 表示x,y的变化是否一致

	- correlation

		- 
![](assets/62FC41C9-9B0B-443D-8423-8F6018A64F9C.png)

			- 表示x , y 是否相关 [-1 ,1]

			- -1 表示完全不相关,1 表示完全先关

			- 
![](assets/31B6F767-30B9-4489-9730-34D55E4D9007.png)

### how liner regression to solve problem

- least sequare error criterion(最小二乘法)

- parameter estimation (回归的参数估计)

	- 参数估计

		- 
![](assets/683DC71F-9198-4880-832F-76E6CD34B5A5.png)

		- 最小化其least sequare function
![](assets/2B3A19F6-98B2-4A17-8054-2AEDE235E0EF.png)

			- 计算参数b

				- 
![](assets/371F98C2-EC5B-4CA9-96E9-A7D40113F869.png)

					- 
![](assets/20D50361-D972-42AC-9AE5-973032C4F02E.png)

			- 计算参数a

				- 
![](assets/5E2DC435-C44E-4BEE-8D84-A56F05D59E63.png)

			- 高维的形式w的表达式

				- least-square function
![](assets/0417B7CF-EC52-4B86-808B-B9DBD421850C.png)

				- 
![](assets/CAE5A3F0-CDEC-498A-9A99-65E831C9A40C.png)

		- 残差和

			- 
![](assets/601F7C36-3C6D-4508-81BD-B05EAAAC40DB.png)

				- n倍的y的均值 -n倍的x的均值 - na
![](assets/4E7E1D63-DC9F-4A57-B3E8-8F9989EA262C.png)

	- regularisation正则化  (找到模型的准确度和模型的复杂度之间的关系) 

		- 
![](assets/FE5D94D2-E63D-43FE-BC3D-2690D6BA056A.png)

			- MSE function

		- 
![](assets/716D73DA-3D41-44B5-8180-0CB10F634743.png)

			- 加入一个参数的惩罚项 用lambda来调整准确度和复杂的之间的关系

		- 高维的regularisation表达式

			- 
![](assets/9459F901-7E14-472F-A180-7DBD2265400C.png)

## Week2  classification

### framework

- 
![](assets/05F4DFB8-92C3-4DFE-A1FF-25A6A27E094C.png)

### Induction and deduction

- Induction指从一系列具体的事实概括中一个一般的结论，即归纳法。

	- 只要从样本中抽取足够多,那么最后的model和target function可以近似一样,就是从部分数据预测整体数据结果
![](assets/1536F3A3-5C76-4519-9A68-539650680D07.png)

		- batch learning 

			- 一次性的把所有数据都放进去然后通过计算在更新

		- online learning

			- 不断有新data进来,在线不断学习,不断更新

		- parametric

			- non-parametric

				- 没有fixed的参数,参数随着模型复杂度的增大而增大

			- parametric

				- 有fixed的参数

- Deduction 从一般结论推测具体事实

### 线性分类

- liner classification

	- 
![](assets/D2E87F7F-E66E-489D-9DA4-E838E11F56F0.png)

		- 
![](assets/952A00E9-FFAB-4AFA-ADC0-9A5DAB510461.png)

		- 
![](assets/125A84C7-CFEF-44A2-9588-AC40AED05DA6.png)

	- 在正值点去一个中心点,在负值点去一个中心点,两个点连线的中垂线,就可以最为liner classfier
![](assets/2CFF80E6-DCDF-4F5F-8A3F-25B130E4C7FE.png)

- evaluation

	- cross-validation(数据集比较小的情况)

		- 分成三份用两份进行训练,一份进行验证,分别调整validate的位置来进行测试
![](assets/64C88E1A-6143-460A-996B-4EA1E7CF8A34.png)

		- 最后取均值

	- 
![](assets/452E0EDF-2DBD-4A88-8B1D-9E62425609A8.png)

		- 计算准确率
![](assets/037894B7-89BC-491C-9FE4-5D9474164B40.png)

### distance measure 

- 
![](assets/CE4FA8A0-F929-478C-B231-DC52C1F97E2A.png)

	- 计算公式
![](assets/9757D62E-1EBE-4154-BFCE-88A4CF6D4FEC.png)

		- 
![](assets/0398FD00-E164-40D7-840A-52338B43AB5E.png)

- 满足成为distance的条件

	- 
![](assets/15B74B86-641F-4302-B568-3BD8405C518C.png)

### KNN

- NN算法

	- 
![](assets/ED140596-7EBD-4A0C-982C-13AA3EAAB815.png)

		- 
![](assets/4E257740-5EA9-40CC-8CEC-1C41233F69E2.png)

	- 
![](assets/09E9DB45-BAC6-4684-8531-FC80BC34C5FE.png)

- nearest neighbour 思想(regression)

	- 
![](assets/59AF407F-77DC-4D37-B49D-F59544BEC5DF.png)

		- 回归的做法
![](assets/19D92D30-30CC-401E-B08F-5D5C0143A66D.png)

- KNN(classification)

	- 根据major vote的确定xq的分类

	- 问题有

		- attribute 的scale不同

			- 身高和体重差值0.2 和 2   
![](assets/B653516B-5264-47A9-BD88-378A521B47B7.png)

		- 解决方法

			- normalize

				- Min-max算法把数值压缩到0-1之间
![](assets/878543B2-BF5B-463B-A72A-B07493F4D288.png)

	- advantage

		- 1速度快

		- 2结果精确

		- 3可以学习复杂function

		- 4不会损失信息

	- disadvantage

		- 1slow query time

		- 2curse of dimensionality

			- 
![](assets/D71AA0FD-E3F4-4E86-B5CB-B3A63B2AB8D6.png)

	- inductive bias

		- 问题????为啥bias减小
![](assets/D6053EE6-AC7B-4C68-ABA1-D430DBBAD106.png)

		- 
![](assets/B3CC0A8A-B00C-444D-81E3-A8E77BC342A6.png)

		- Knn可以输出概率分布   当k>1
![](assets/2A8A0735-0BDF-4A75-B73F-F262BB5595E9.png)

	- 对其每一个k加权重

		- 
![](assets/6390191C-B5E8-4D4A-B2EE-EDFFD73AB309.png)

		- Wi为距离倒数的平方,距离越大,权重越小,距离越小权重越大
![](assets/A28FB1CF-4E39-4C1E-908C-04AEA471936D.png)

	- lazy learner

		- 1不进行学习

		- 2等待query来进行查找

	- evaluate

		- 问题

			- 
![](assets/FD073F25-783C-4E3E-ABAF-631DE52E3A24.png)

				- 1 很慢

				- 2 noise

				- 3 weight 相同

			- 
![](assets/DC2DC27F-616B-4603-9A86-3F4A93A0F1C1.png)

		- loocv
![](assets/7F09833A-EC08-4B87-B06B-8639824DE469.png)

			- 
![](assets/AEF9BA38-367E-49FF-8511-8EAD52193F17.png)

			- 取出一个数据点,用剩余的n-1个数据点进行训练,在用这个一个数据点进行验证,对每个数据重复该过程,求出平均的预测error

## Week 3 classification2

### inductive bias

- 
![](assets/0D1E5C23-A62F-4615-856C-5AAFAF90F22E.png)

- 我们在训练模型的时候需要作出一些假设,但这些假设不一定是对的(会偏离target)        我们称为inductive bias

	- 使用MSE来评测model的好坏(这个不一定)

### bayes theorem

- 
![](assets/0BBA9331-041E-4A4F-8103-19DEB6031E0C.png)

	- 后验概率
![](assets/8D43741D-6C05-4885-932F-40BE50B90D25.png)

	- 似然概率
![](assets/FB7839F6-8200-4F1A-AF03-5CAE4FB7EC40.png)

	- 先验概率
![](assets/5633DA50-15DB-4B83-906C-083283A23C3C.png)

### MAP ML

- ML 最大似然

	- 
![](assets/8FAE089A-AB99-4D5F-AA1B-15F74C144734.png)

- **MAP 最大后验概率**

	- 
![](assets/7CEAB845-1FA6-45B9-B1D3-CDCC23125430.png)

### 规范概念学习任务
![](assets/D3C868C6-689C-4E22-8246-D730FECD4C8B.png)

- 
![](assets/73A91B09-67CF-4455-A64D-B8654CAB8296.png)

	- 1 . h用vshd表示

	- 2. h属于H(假设空间)

	- 3 . h能够对每一个D中的数据预测准确

### 用贝叶斯理论解释regression的问题

- di中的ei就是人为增加的噪音
![](assets/BE4E79C9-00EC-432A-AC4B-17023782184F.png)

	- Ei服从正态分布

		- 
![](assets/AA34219F-8A0C-42C4-B834-2F35FCEC69AF.png)

- 只是把原来的function变成了h(xi)(假设)
![](assets/C8500555-1189-4C75-A5C1-6C2E6DD59CFA.png)

	- P(D|h) 可以写成连乘的形式,     连乘服从正态分布
![](assets/800B5891-229D-4F01-B001-0099A4C4C2E8.png)

		- 通过化简可以得到

			- 其实和liner regression 一样这里取最大就是取最小的least sequare 
![](assets/D12FC23F-C0D1-41A7-A5BB-78890DD67808.png)

### bayes optimal classification rule

- 表示在givenD的条件下hi的概率乘上givenhi的条件下vj的概率
![](assets/007677FF-A13F-445E-9B92-CE2A81DA5E16.png)

	- Vj表示h(x)的class

	- 
![](assets/0D8B2D94-D4AB-4E6D-925D-84B8F9F7AB5F.png)

	- 转换成
![](assets/28578392-909E-436A-8983-6C5C0A0260A7.png)

		- 得到结论0.6大,class 为-
![](assets/E96000A1-4F7F-4A35-81E6-83221DC5A93B.png)

### Naive bayes classification algorithm

- 
![](assets/4879E978-4FEF-4360-8EA6-B43548A08580.png)

	- 朴素贝叶斯就是假设我们有多个attribute,并且假设相互独立的条件下来应用MAP 和 ML算法来解决问题的classifier

- 
![](assets/974C97DF-5193-4A1F-9827-DE262D813AB0.png)

- *************重要*********
![](assets/3D27064B-80DF-442F-AB67-DF2CEAFE9E4C.png)

	- 算法
![](assets/C64822E3-31B1-4369-91E6-8E4747524F2B.png)

### 在text 分类上运用naive bayes

- 伯努利形式

	- Smoothing的时候分母+类别数 分子+1

- 多项式形式

	- smoothing的时候分母+总共的单词数 分子+ 1

### logistic classification(逻辑回归)

- 在原来liner regression上面加了一个激活函数 sigmoid函数

## Week4 tree learning

### 决策树表达形式

- 当instance由多种attributes来构成
![](assets/A550BCBB-BE3C-4ED4-998C-8F1CBE445623.png)

- 到了leaf节点对class进行判别

### basic top-down algorithm

- 
![](assets/6B50FDC2-3DB6-4678-9F98-F6C1FE92B122.png)

- 使用entropy来判别是否可分

	- 
![](assets/FBF56AA6-E1F8-4539-86D7-12983AA5B2A1.png)

	- 当dataset里面都是a或者b的时候,熵的值为0,当ab各一半的时候熵达到最大值
![](assets/39E224ED-6114-4BE9-A2E7-82876138C20B.png)

	- 熵增公式(分裂条件根据gain大的分)
![](assets/40E98209-3B19-406F-BDBB-1D1466996871.png)

### 如何减小overfitting

- overfitting的定义                         假设h 和h’   
  如果在h在训练集上的错误要小于h’在训练集上的错误  
  但h在整个训练集上的错误要大于h’在整个训练集上的错误
![](assets/935F5EA3-D517-4081-A1C0-D29989177A08.png)

- pre-pruning

	- 在构建树的时候,先算出不split的熵,在算出split后的熵,然后依据两个熵来判断是否split

		- 缺点

			- 过早停止underfitting

		- 优点

			- 速度快

- post-pruning

	- 在树构建完成之后,对每一个subtree进行熵的分析和上面一样

		- 缺点

			- 速度慢

	- reduce-error pruning

		- 优缺点

			- 用小的dataset产生能够预测准确的树
![](assets/38BA3A6E-553D-4878-8B49-CA1F3F23582A.png)

			- 减小了dataset大小的有效性因为减小了size
![](assets/31E3995A-A882-49C4-8B42-CD79AE365257.png)

		- 方法:把data划分成trainning 和 validate两个数据集(就是西瓜书上的方法)

			- 用training data训练,用validate测试分开和不分的准确率,如果低于则不分,反之亦然

	- error-based pruning

		- 悲观估计
![](assets/D6A8F4C9-B1B9-4C37-ADCA-95766B44F90E.png)

			- 目的是要在原来的f上增加一个惩罚,                                        ****主要惩罚那些example数量很少但是错误率却很高的node*******(N是子树上面所有node的数量,如有多个child node 其悲观错误率为加权和)

				- 
![](assets/A725C533-52C8-49A2-A4E7-98AC68DCDEED.png)

			- tree learning的错误率不会超过0.5

			- 从node leaf的子树不断往上剪枝直到root为止(分之后的悲观错误率小于分之前的就分)

		- f 是真实错误率 N是node的个数 Zc是一个常数  

- 两个问题

	- many-value 问题

		- 因为如果有很多的attribute的话,他的information gain肯定很大

		- 解决方法

			- 使用gainratio来计算
![](assets/1BB17E14-8FF1-4576-ADCB-F78473BBABAB.png)

			- 
![](assets/F6AE230B-38EE-43B0-A952-B21F9067653D.png)

	- cost 问题

		- Atest花费1000刀 bloodtest花费100刀只有当A的information gain远远高于bloodtest 我们才选A来split
![](assets/F42E1A56-A812-4C6B-860B-32DA9C24B855.png)

		- 
![](assets/26E08390-2842-4652-BC1B-175D2D6B41AD.png)

### 树结构的扩展

- 把树转换成这样的形式
![](assets/EB99F5EF-5DAE-4A05-9B42-4B019A510E89.png)

- regression tree

	- 输出numeric value

		- 用variance来取代information gain
![](assets/8A72AE30-D4AD-4A1C-9C52-9B20CAB821BD.png)

			- 计算variance,想在同一个node他们尽可能接近,使得其variacne越小越好

			- 最初可能variance 很大,但是split后variance 就会变小

- model tree

	- 每个node都有一个liner regression
![](assets/7C56AD89-2C3C-422D-8003-816181E9EEFC.png)

	- 如何smooth

		- 
![](assets/A080B5B1-B54A-4006-BA7D-503505ADB0F5.png)

	- 如何build

		- 使用标准差的reduction类似于information gain
![](assets/6D9DEDC3-DEE8-4B35-9159-461783314FEA.png)

	- 如何pruning

		- 使用找个计算公式来决定是否prune
![](assets/F7030D67-1BF1-445C-A825-34E5593DD5B2.png)

## Week 5 neural network

### perceptron

- Sum Wi*Xi
![](assets/3FD80A06-25E2-4576-B421-34DE6D36E356.png)

- 激活函数
![](assets/1E38FC5A-EA34-4F2C-88D3-27BF638C3F40.png)

- 不断的修正w
![](assets/06F5DDC8-29EA-434F-BDEF-DDDB65DA59E8.png)

	- Wi的表示形式 第一个决定步长 第二个决定符号 第三个决定方向
![](assets/A1A3F7BD-B26E-4403-9A77-6CC32D16FCBE.png)

### multilayer perceptron             遇见non-linearly separate data

- 概念

	- multilayer perceptron

	- Input 是高维度的

	- 存在噪音数据

	- 人类的可理解性是不重要的

	- 如果满足以上条件就适合使用多层感知机来生成model

- 梯度

	-  梯度下降

		- 使用梯度下降来计算delta w

			- 
![](assets/DDB77912-3774-4356-9075-5F5451576780.png)

			- loss function
![](assets/18934B2C-4A34-4C59-8AC6-31816826ED0D.png)

			- 计算过程
![](assets/A726DA8B-5E03-42AD-907C-C5B5B87B0097.png)

			- 算法:对每一个wi进行更新
![](assets/19134A1E-D1BA-40A3-B8B9-8EEE40C33704.png)

	- 使用激活函数函数的                        梯度下降

		- sigmoid 激活函数
![](assets/8D919780-E015-48D8-A059-347E9C1631DB.png)

			- 1 具有好的求导性质

				- 
![](assets/3336F933-BEBA-4247-BCBE-2FE8595A2603.png)

			- 2 能够将数据映射到0-1

		- 将线性转换成非线性

		- 
![](assets/52CE5352-623D-47E8-BC8B-DE9B5F1ACA2F.png)

			- Od就是sigmoid的函数

			- Netd就是之前sigmoid函数的输入
![](assets/4F87F3D1-38FD-4CD4-86DB-81BC933EE313.png)

			- 可以得到
![](assets/3920E352-691B-4EB2-9015-6BC876991DB6.png)

				- 
![](assets/73D301E4-5B00-4C89-A8EE-C02A1A202E6A.png)

		- different mode

			- batch mode

				- 所有的数据训练完,最后更新w

					- 
![](assets/6C8EF8BE-6887-4834-AF48-892FF7ACECA3.png)

				- 
![](assets/F0C7067B-5AFE-45F5-A267-861E1DED0D16.png)

			- incremental mode

				- 训练完每一个example完进行更新

					- 
![](assets/C354F0EE-1C8B-4726-A342-760255A65D0E.png)

				- 
![](assets/0F946DE7-29B1-478C-92FD-5BB0B8746B2B.png)

- 反向传播算法

	- 产生问题

		- 局部最优

			- 

	- 解决方法

		- mini batch

			- 每次放进去100个进行更新避免其陷入局部最优

	- 
![](assets/EEFD953A-4170-45D3-B210-BE2A3722C846.png)

- 神经网络overfitting解决方法

	- dropout

		- 不是训练所有的数据,而是设置一个抹除率,随机的将一部分节点给去除后进行训练

	- 类似于线性回归的正则化给其加一个惩罚项和一个lambda项来平衡其error和overfitting的问题

		- 
![](assets/2284C065-ADA4-42A3-B40B-F679113FF7A6.png)

- 神经网络 作为classification

	- 使用交叉熵作为loss function
![](assets/4B142072-C237-412C-B676-155462B00FFC.png)

- 补充知识

	- sigmoid 

		- 1 存在梯度消失问题

		- 2 不是0 centeral的

	- reLu

		- 
![](assets/DAA929E6-43B9-4CCD-9972-BC2CD4FBD1FB.png)

	- tanh

		- 0 center 函数

		- 在[-1 +1]

## Week 6  kernel methods

### 前置知识

- liner classifier in dual form 问题

### SVM

- 概念

	- 落在边界上的点就叫做support vector

	- 找到一条线有最大的margin

- 计算

	- 做大化2/||w|| 就是最小化1/2||w||**2 并给其一个约束
![](assets/EF3DE483-6A95-4F14-B3FF-7BBD2D2D7D2A.png)

		- Alfa1,2,3...,n为拉格朗日乘子
![](assets/FDBC2DF2-8A56-49D0-AF33-EC1B4B97496E.png)

			- 得到拉格朗日的对偶形式
![](assets/F0FEB8D2-45CA-4C64-A61F-B744457E6870.png)

			- 看tutorial题,注意参数带入过程

### soft margin SVM

- allowing margin errors

	- 
![](assets/C22EA85D-3B77-4176-833F-B08D58E4D7C5.png)

- 
![](assets/4B3FD0E0-17B7-46C3-833B-0D7B0800634D.png)

	- 能够分析不同的ai,点所在的位置
![](assets/53F6A19D-D7B8-401B-8526-9B01250CB523.png)

		- 用这两个公式分析
![](assets/3913FA73-1CA3-4E3E-BDB5-AE4014D14104.png)

			- 当ai为0的时候1-E = 0,并没有放宽条件

			- 当0<ai<c的时候E = 0,点全部在线上

			- 当ai=c的时候,inside margin

		- A
![](assets/7CD2F8DE-B335-44A6-AEAF-BF9C5A653E5F.png)

		- B
![](assets/53F51E3E-DF14-4AD8-A419-0E6428235CCE.png)

		- 
![](assets/C6B9DEC9-E5B6-4342-8954-5E3E2C80BBD0.png)

### kernel method

- kernal trick

	- 公式记住
![](assets/8FFB3B16-64D0-4231-989F-0C43B44A02E1.png)

## Week 7 ensemble learning

### bias-variance decomposition(必考)

- bias  模型和真实值之间的mismatch

- Variance  用不同数据所得到的不一样的模型

### 问题

- bias is too high 

	- 使用复杂的模型

		- 会导致variance

			- 使用大量的数据

### stability

- 用两个dataset(从同一个distrubution产生的)如果产生的model 一样,称为stability

	- stable: KNN

	- unstable : 决策树

- 稳定的模型通常比较简单,高bias 低variance

- 1NN

	- 能够完美分开训练数据,所以low bias ,high variance

- Knn

	- K是可以变得,当k变的很大就是stable的

### bagging

- 问题: 在不增加数据量的前提下减小bias and variance

- Define :  随机sample T次数据(有放回的抽取),然后用相同的算法训练,然后返回T个模型

	- 缺点

		- 1 变复杂

### random forest bagging 

- 和bagging一样,但在选取feature的时候,随机选取feature(不全部选取),增加了第二个随机量

### boosting

- weak leaner的定义
![](assets/78411EA8-F40C-4F23-B616-6C90321C1635.png)

- 

	- 训练weak leaner

		- Chain式的训练,不断增加weak leaner 后一个leaner只训练前一个leaner预测错的数据

		- 

	- 算法一

		- h1是一个weak leaner

		- H2是从h1中做错的数据集中训练来的

			- 
![](assets/163AB84F-DABF-45DF-BC55-495A1051F3E2.png)

			- 将h1 h2结合在一起,他两一直的结果就作为最终结果不一致的话就交给h3进行预测

### stacking 

- 概念: 组合不同的模型来合成一个模型进行预测

	- meta learner (level  1 )

	- base learner (level  2 )

	- meta leaner 通过权重结合base learner 的输出来进行输出

### 需要记住

- low-bias model tend to have high bias and vice versa

- bagging 用来减小variance

- boosting 用来减小 bias

## Week 8 unsupervised leaning

### 概念

- supervise learning : 有label

- unsupervised learning : 无label

### PCA

- 
![](assets/0A151714-83E0-4E3E-B2AB-235607A9607F.png)

### cluster

- hierarchical methods

	- Hierarchical clustering

		- single link

			- 找minimum

				- 
![](assets/83611C64-E9DF-4D80-A8BA-FA921CE5F25D.png)

		- complete link

			- 找maximum

		- average link

			- 找平均值

- partitioning methods

	- K-means

		- 重复取中心点在分类

		- 是class内间距最近

### EM

- 有k个数据服从正态分布,但其mean不同

	- 假设一个初始化均值

	- 计算输入值是哪一个高斯分布的可能性大,然后在重新计算mean 和variacne,在进行分类
![](assets/084EC557-BB5D-4E11-81D4-D9573F309C37.png)

	- 
![](assets/49BF0D2F-1C4E-4D1E-8469-FC5F33CD5634.png)

### evaluate 衡量cluster的好坏

- silhouette plot(轮廓) width [-1, 1]

- 组内距离和组间距离来衡量

- b(i)就是数据点i和组间其点的距离的均值
![](assets/6F2835FD-FAD6-4591-8EE0-0A7A8955B848.png)

- a(i)就是数据点i和组内其他点的距离的均值
![](assets/DFEED23F-F19E-4CD9-8198-09875D9B6E0E.png)

- 找到一个最小的平均组间距离应用下式
![](assets/23BB697D-CD12-4CD3-A67D-940842991B0C.png)

- 得到的值越大越好
![](assets/8A6D0990-450D-4738-BDE1-F358D2AEB1D5.png)

## Week 9 learning theroy

### 

- 解决问题

	- sample complexity

		- 有多少sample 需要leaner 去学习才能到达收敛

	- computational complexity 

		- 需要多少的计算复杂度才能使学习到达收敛

	- hypothesis complexity

		- 怎么测量假说空间复杂度

		- 需要多大的假说空间

	- mistake bound

		- 需要多少错分才能使得learner成功能够收敛

- PAC 模型

	- more_general_than_equal_to(偏序关系)

		- h2 is more general than equal to h1

		- ❓代表all
![](assets/7913497B-87FF-424F-A0FE-5CFEA516E7AF.png)

	- 转换到假说空间还要加上all属性所以3+1 = 4 ,all代表不管attribute是啥都为真
![](assets/E4A20F44-93A2-4C25-A2E5-69BF90DC2FC6.png)

	- consistent

		- 我们的假说在dataset上预测全都是对的

	- 分析

		- 
![](assets/9291323E-492A-4931-86C3-90EEA5BF135A.png)

			- 所有小h的true error都是小于E的,我就认为他叫做E-exhausted
![](assets/EE4872FD-4646-4122-9AEA-8A126B261731.png)

			- 有m个数据的dataset里面我们的vshd 里面有一个或者多个错误率比E大的概率是小于

				- 
![](assets/15D22426-1B6E-4929-805B-23177E1E7F6D.png)

		- 公式记住 
![](assets/87783235-1E15-4192-832A-95AF526FF9BE.png)

		- 
![](assets/25833ECB-E491-4327-BBF4-719A14BCC010.png)

		- 我要有m个training example 才能训练处合适和模型
![](assets/A1AEBA1C-D77E-4471-A1DA-297F2B9E7622.png)

	- PAC-learnable

		- 在此条件下模型能学到东西

		- 条件限制

			- 
![](assets/B2ED23E7-A387-4324-8825-EC909E144155.png)

		- vc dimension

			- shatter

				- 能不能shatter取决于
![](assets/9FD0999D-7443-4108-9C0B-0D25C5A87472.png)

				- 不论怎么分配三个点,都能分配白色和黑色点都能把三个点分配到两边

			- vc dimension用来减少我们假设空间

				- 在此模型下,我们能够shatter最多点的个数称为Vc dimension 如果在d维的平面上,用liner classifier ,那么它的vc dimension 为d+1

				- d个连接在一起的布尔function他的vc dimension 为d

- 算法

	- find-s

		- 
![](assets/FFBB17FA-3BC2-40A6-9E81-6C539F7FF64E.png)

			- 在第h1处的话,每一个空集包含两种情况(terms),匹配和不匹配

			- 第二轮就会较小一半的terms

			- 在最坏的情况

				- 每一轮有一个错误加上h1出的错误为n+1
![](assets/2B38E72E-39E1-4C9C-9BDA-CC6EC3993018.png)

		- 1 . 设置为空集的形式,什么都不行

			- 
![](assets/A27CD5A1-1360-43B4-A9E4-50CF64006285.png)

		- 2. 与下面的假说对比,冲突的变成?,不冲突的保留,-号的跳过

		- 3 .直到h4

	- halving algorithm

		- 使用major vote 的形式删除不正确的

		- mistake-bound

			- 为log2|H|
![](assets/5E59A935-D670-4728-8FD8-BA0E86B6B94E.png)

			- 
![](assets/39A629C0-C49C-4A13-9AC7-405BA838AE25.png)

	- winnow2

		- 类似于有权重的liner classifier的算法

		- 改变的instance weight

			- 对于每一个instance如果预测错误,更改其weight

			- 
![](assets/3F191C41-175D-4770-840F-A4D240899113.png)

	-  no free lunch

		- 统一的平均所有的目标函数,对于其off-train-set error 所有的算法都是一样的

		- 假设有set D 能够完全正确的被所有算法学习到,平均所有目标函数,没有任何学习算法所产生的  
		  
		  off-training-error 大于任何一种算法(都是一样的)

