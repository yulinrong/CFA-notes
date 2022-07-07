---
marp: true
footer: 'Noted by 量化菜鸟'
---
# R3 概率学概念



---
## 学习目标

1.  定义随机变量、结果和事件
2.  识别概率的两个定义属性，包括相互排斥和详尽的事件，并比较和对比经验概率、主观概率和先验概率
3.  用支持和反对事件的几率来描述事件的概率
4.  计算和解释条件概率
5.  演示概率乘法和加法规则的应用
6.  比较和对比依赖和独立事件
---
7.  使用全概率规则计算和解释无条件概率
8.  计算和解释随机变量的期望值、方差和标准差
9.  解释在投资应用中使用条件期望
10.  解释概率树并展示其在投资问题中的应用
11.  计算和解释投资组合收益的期望值、方差、标准差、协方差和相关性
12.  使用联合概率函数计算和解释投资组合收益的协方差
13.  使用贝叶斯公式计算和解释更新的概率
14.  确定解决特定计数问题的最合适方法，并使用阶乘、组合和排列概念分析计数问题

---
## 条件概率和联合概率

+ unconditional probability 无条件概率
+ conditional probability 条件概率
+ joint probability 联合概率
+ $P(A|B) = \frac{P(AB)}{P(B)}$,$P(B) \neq 0$
+ Multiplication Rule for Probability $P(AB)=P(A|B)P(B)$
+ addition rule for probabilities $P(A or B) = P(A) + P(B) - P(AB)$
+ 事件A和B是independent独立的，当且仅当$P(A|B)=P(A)$或$P(B|A)=P(B)$
+ 事件是dependent依赖（相关）的：一个事件发生的概率与另一个事件的发生有关。
+ Multiplication Rule for Independent Events独立事件的乘法规则$P(AB)=P(A)P(B)$
+ total probability rule $P(A) = P(AS) + P(AS^C)$
---
## 期望值(平均值)、方差和期望值和方差的条件测量

+ 随机变量的期望值$E(X)$
+ 随机变量的方差$\sigma^{2}(X) = E\{[X-E(X)]^2\}$
+ standard deviation标准差是方差的正平方根
+ $\sigma^2(X) = \sum_{i=1}^{n}P(X_i)[X_i-E(X)]^2$
+ conditional expected values $E(X|S) = P(X_{1}|S)X_{1} + P(X_{2}|S)X_{2} + \cdots + P(X_{n}|S)X_{n}$
+ total probability rule for expected value:
	$E(X) = E(X|S)P(S) + E(X|S^C)P(S^C)$
	$E(X) = E(X|S_{1})P(S_{1})+E(X|S_{2})P(S_{2})+\cdots+E(X|S_{n})P(S_{n})$
+ probability tree diagram, node
+ conditional variances
---
## 期望值，方差，标准差，协方差和相关性

+ Calculation of Portfolio Expected Return 投资组合预期回报的计算
	 $E(R_{p}) = E(w_{1}R_{1} + w_{2}R_{2} + \cdots + w_{n}R_{n})$
	 $=w_{1}E(R_{1}) + w_{2}E(R_{2}) + \cdots + w_{n}E(R_{n})$
+ 两个随机变量$R_{i}$和$R_{j}$的协方差
	$Cov(R_i, R_j) = E[(R_{i} - ER_{i})(R_{j}-ER_{j})]$
	$Cov(R_{i},R_{j}) = \sum_{n=1}^{n} (R_{i,t}-\bar{R}_{i})(R_{j,t}-\bar{R}_{j})/(n-1)$
+ covariance matrix 协方差矩阵
+ 两个随机变量$R_{i}$和$R_{j}$之间的correlation相关性
	$\rho(R_{i},R_{j}) = Cov(R_{i},R_{j})/[\sigma(R_{i})\sigma(R_{j})]$
	$Cov(R_i,R_j) = \rho(R_i,R_j)\sigma(R_i)\sigma(R_j)$
---
## 给定联合概率分布的协方差

+ joint probability function联合概率函数计算协方差
+ $Cov(R_{A},R_{B}) = \sum_{i}\sum_{j} P(R_{A,i},R_{B,j})(R_{A,i}-ER_A)(R_{B,j}-ER_{B})$
+ 两个随机变量$X$和$Y$是独立当且仅当$P(X,Y)=P(X)P(Y)$
+ 不相关随机变量乘积期望值的乘法规则
		$E(XY) = E(X)E(Y)$
---
## 贝叶斯公式
+ Bayes' formula
给定一组感兴趣事件的先验概率，如果你收到新的信息，更新事件概率的规则是
$=\frac{Probability\ of\ the\ new\ information\ given\ event}{Unconditional\ probability\ of\ the\ new\ information} * Prior\ probability\ of\ event$
$P(Event|Information) = \frac{P(Information|Event)}{P(Information)}*P(Event)$
+ prior probability先验概率
+ likehoods观察的条件概率
+ posterior probability后验概率：反映或出现在新信息之后的更新概率。

## 计数原理
+ Multiplication Rule for Counting计数的乘法原理$(n_{1})(n_{2})\cdots(n_{k})$
+ Multinomial Formula (General Formula for Labeling Problems)多项式公式(标签问题的通用公式)
	$\frac{n!}{n_{1}!n_{2}!\cdots n_{k}!}$,  $n_1 +n_2 + \cdots + n_K = n$
+ combination组合是一个列表，其中列出的项目的顺序无关紧要。
+ Combination Formula (Binomial formula) 二项式公式
	$C_{n}^{r} = \frac{n!}{(n-r)!r!}$
+ permutation置换是一个有序列表。
+ permulation formula $P_{n}^{r} = \frac{n!}{(n-r)!}$