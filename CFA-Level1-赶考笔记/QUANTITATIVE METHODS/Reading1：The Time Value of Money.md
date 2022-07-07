---
marp: true
---

# Reading 1-货币的时间价值

```
金钱具有时间价值，因为个人越早收到一定数量的金钱，它的价值就越高。
```

Noted by：量化菜鸟

---
## 学习目标

a. 将利率解释为**所需的回报率、贴现率或机会成本**
b. 将利率解释为**实际无风险利率**和**补偿投资者承担不同类型风险的溢价的总和**
c. 给定规定的年利率和复利频率，计算和解释**有效年利率**
d. 计算**不同复利频率的货币时间价值**问题的解
e. 计算和解释**单笔资金、普通年金、到期年金、永续年金（仅限 PV）和一系列不等现金流的未来价值 (FV) 和现值 (PV)**
f. 演示在建模和解决货币时间价值问题中使用**时间线**

---
## 利率

+ Interest rate利率，表示为$r$, 是反映不同日期现金流量之间关系的回报率。
+ “interest rate”=“discount rate”
+ opportunity cost机会成本是投资者通过选择特定的行动方案而放弃的价值。
+ _r_ = Real risk-free interest rate + Inflation premium + Default risk premium + Liquidity premium + Maturity premium

---
+ real risk-free interest rate**实际无风险利率是指在**没有通胀预期的情况下完全无风险证券的单期利率。
+ Inflation premium**通胀溢价**补偿投资者的预期通胀，并反映债务到期时预期的平均通胀率。实际无风险利率和通货膨胀溢价之和就是**名义无风险利率**nominal risk-free interest rate。
+ default risk premium**违约风险溢价**补偿投资者因借款人未能在约定的时间和约定的金额上做出承诺的付款的可能性。
+ Liquidity premium如果投资需要快速转换为现金，**流动性溢价**补偿投资者相对于投资公允价值的损失风险。
+ **到期溢价**补偿了投资者随着到期日的延长而增加的债务市场价值对市场利率变化的敏感性。
---

## 单一现金流的终值（一次性）Future Value of a Single Cash Flow (Lump Sum)

+ $PV$ = present value of the investment
+ $FV_N$= future value of the investment _N_ periods from today
+ $r$ = rate of interest per period
+ For $N$ = 1, the expression for the future value of amount PV is
	$FV_{1}= PV(1 +r)$

---

+ simple interest单利
+ Principal本金
+ compounding复利
初始投资的现值$FV$与其$N$个周期后的未来值$PV_N$联系起来
	$FV_{N}=PV(1+r)^{N}$
+ $r$ is the stated interest rate per period
+ $N$ is the number of compounding periods
+ 规定的利率$r$和复利期数$N$时间单位必须兼容

---

## 非年度复利（终值）Non-Annual Compounding (Future Value)

+ stated annual interest rate or quoted interest rate $r_s$
+ 一年多于一个复利期，终值公式可以表示为:

	$FV_N=PV(1+r_{s}/m)^{mN}$
+ $r_s$是规定的年利率，$m$是每年的复利期数，$N$现在代表年数。请注意此处使用的利率$r_s/m$和复利期数$mN$之间的兼容性。

---

## 连续复利、规定和有效利率Continuous Compounding, Stated and Effective Rates

+ 每年的复利期数变为无限，则称利息连续复利
+ N年连续复利的未来价值为
	$FV_N=PVe^{r_{s}N}$
 + stated annual interest rate规定的年利率和有效年利率the effective annual rate (EAR)之间的关系：[离散的复利和连续的复利]
	 $EAR=(1+Periodic\ interest\ rate)^{m}−1=e^{r_s}−1$

---

## 一系列现金流的终值，年金的终值Future Value of a Series of Cash Flows, Future Value Annuities


+ **年金annuity**是一组有限的水平顺序现金流
+ **普通年金ordinary annuity**具有从现在开始的一个时期发生的第一笔现金流（索引为t=1）
+ **到期的年金annuity due**具有立即发生的第一笔现金流（索引为t=0）
+ **永续年金perpetuity**，或一组永无止境的连续现金流，第一笔现金流发生在从现在开始的一个时
+ 等额现金流Equal cash flows--ordinary annuity
+ 不均的现金流Unequal cash flows
---
## 非年度复利的现值Non-Annual Compounding (Present Value)

+ 如果一年中有多个复利期，**现值**公式：$PV=FV_{N}(1+r_{s}/m)^{−mN}$
+ _m_ = 每年的复利期数
+ $r_s$ = 报价年利率
+ $N$ = 年数
---
## 一系列等额现金流(年金)、不等额现金流的现值Present Value of a Series of Equal Cash Flows (Annuities) and Unequal Cash Flows

1. 一系列等额现金流(年金)的现值
	$PV=A[\frac{1−\frac{1}{(1+r)^{N}}}{r}]$
	+ $A$ = 年金金额
	+ $r$ = 对应于年金支付频率的每期利率（例如，每年、每季度或每月）
	+ $N$ = 年金支付次数
2. 一些列不等额现金流的现值
	+ 求和
---
## 永续年金的现值和在T=0以外时刻的现值Present Value of a Perpetuity and Present Values Indexed at times othen than T=0

+ 永续年金的现值
	$PV=A/r$
+ 在T=0以外时刻的现值
	$PV = FV_{N}(1+r)^{-N}$
---
## 求解利率、增长率和期数Solving for Interest Rates, Growth Rates, and Number of Periods

+ $PV = FV_{N}(1+r)^{-N}$
+ 增长率$g=(FV_{N}/PV)^{1/N}−1$
+ $(1+r)^{N}=FV_{N}/PV$  推导出期数$N$
---
## 求年金的支付规模(结合终值和现值年金)Solving for Size of Annuity Payments (Combining Future Value and Present Value Aunuities
+ 抵押贷款、汽车贷款和退休储蓄计划是应用年金公式的经典例子
+ $PV=A[\frac{1−\frac{1}{(1+r)^{N}}}{r}]$
+ 退休计划--现金流相加原理
+ $FV=A[\frac{(1+r)^{N}−1}{r}]$
---
## 现值和未来值等价，可加性原理Present Value and Future Value Equivalence, Additivity Principle

+ **等价性**：一笔总付可以被视为等同于年金，而年金可以被视为等同于其未来价值。因此，现值、未来值和一系列现金流都可以被认为是等价的，只要它们在同一时间点被索引即可。
+ **现金流可加性原理**——即在同一时间点索引的货币数量是可加的——是货币时间价值数学中最重要的概念之一。