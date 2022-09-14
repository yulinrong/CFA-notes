

Noted by 量化菜鸟

# 线性回归

## 简单线性回归

+ Regression analysis 回归分析：一种检验一个变量对解释另一个变量是否有用的工具。
+ sum of squares total (SST)总平方和：variation of $Y=\sum_{i=1}^{n}(Y_i - \bar{Y})^2$
+ 将正在解释其变化的变量称为**因变量**，或**被解释变量**；用Y表示。
+ 将其变化用于解释因变量变化的变量称为**自变量**或**解释变量**；用X表示。
+ 只有一个自变量，称为Simple Linear Regression简单线性回归（SLR）；有多个自变量，称为多元回归。



## 估计简单线性回归的参数

+ 线性回归假设因变量和自变量之间存在线性关系。
+ 线性回归通常被称为ordinary least squares (OLS)普通最小二乘 (OLS) 回归
+ $Y_{i} = b_{0} + b_{1}X_{1} + \epsilon_{i}, i=1, \cdots, n$, intercept截距$b_0$, slope coefficient 斜率系数$b_1$, error term 误差项$\epsilon$。
+ regression coefficients 回归系数：截距$b_0$和斜率系数$b_1$
+ 第$i$个观测的residual残差$e_i$，是$Y_i$的观测值与$\hat{Y}_i$的差异有多大，使用回归线估计:$e_i = Y_i − \hat{Y}_i$。
+ 残差平方和: sum of squares error (SSE) (1)因变量值与(2)根据估计的回归线得出的因变量值的方差平方和。



+ sum of squares error = $\sum_{i=1}^{n} (Y_i - \hat{Y}_i)^2 = \sum_{i=1}^{n} e_{i}^2$
+ $\hat{b}_1 = \frac{Covariance\ of\ Y\ and\ X}{Variance\ of\ X} = \frac{\sum_{i=1}^{n}(Y_i-\bar{Y})(X_i-\bar{X})}{\sum_{i=1}^{n}(X_i-\bar{X}^2)}$
+ $\hat{b}_0 = \bar{Y} - \hat{b}_1\bar{X}$
+ 横截面回归涉及同一时间段内对X和Y的许多观察。
+ 时间序列数据使用来自同一公司、资产类别、投资基金、国家或其他实体的不同时间段的许多观察结果，具体取决于回归模型。




## 简单线性回归模型的假设

+ Linearity线性:因变量$Y$和自变量$X$之间的关系是线性的。
+ Homoskedasticity同方差:回归残差的方差对于所有的观测值都是相同的。
+ Independence独立性:观察到的$Ys$和$Xs$是相互独立的。
+ Normality正态性:回归残差为正态分布。



## 方差分析

+ sum of squares regression (SSR) 回归平方和
+ sun of squares total (SST) 总平方和
+ sum of squares error (SSE) 误差平方和
+ $SST = SSR + SSE$
+ measures of goodness of Fit 拟合优度度量
+ 1. 确定系数coefficient of determination——由自变量解释的因变量的变化部分——是描述性的，它不是统计检验。
  $coefficient\ of\ determination=\frac{Sum\ of\ squares\ regression}{Sum\ of\ squares\ total} = \frac{\sum_{i=1}^{n}(\hat{Y}_i-\bar{Y})^2}{\sum_{i=1}^{n}(Y_i-\bar{Y})^2}$



+ 2. 均方回归mean square regression (MSR)
    $MSR = \frac{Sum\ of\ squares\ regression}{k} = \frac{\sum_{i=1}^{n}(\hat{Y}_i-\bar{Y})^2}{1}$
    
+ 3. 均方误差mean square error (MSE)
   $MSE = \frac{\sum_{i=1}^{n}(Y_i - \hat{Y}_i)^2}{n-2}$
+ 4. F分布（MSR/MSE）
+ 简单线性回归中估计的方差分析和标准误差analysis of variance (ANOVA),standard error of the estimate $s_e$
+ $s_e = \sqrt{MSE} = \sqrt{\frac{\sum_{i=1}^{n}(Y_i-\hat{Y}_i)^2}{n-2}}$



## 线性回归系数的假设检验

+ 斜率系数slope coefficient $\hat{b}_1$
+ 斜率系数的标准误差standard error of the slope coefficient 
    $s_{\hat{b}_1} = \frac{s_e}{\sqrt{\sum_{i=1}^{n}(X_i - \bar{X})^2}}$
+ 截距的假设检验
    $s_{\hat{b}_0} = \sqrt{\frac{1}{n}+\frac{\bar{X}^2}{\sum_{i=1}^{2}(X_i - \bar{X})^2}}$
+ indicator variable 指示变量：根据条件只接受0或1两个值中的一个的变量。



## 使用简单线性回归和预测区间进行预测

+ 预测的标准误差standard error of the forecast $s_f = s_e \sqrt{1+\frac{1}{n} + \frac{(X_f-\bar{X})^2}{\sum_{i=1}^{n}(X_i-\bar{X})^2}}$
+ 估计的标准误差$s_e$,观察次数$n$,自变量的预测值$X_f$



![围绕预测因变量创建预测区间](https://s3.amazonaws.com/wmx-api-production/courses/36811/images/CFA2207-R-EXH31.png)
  


## 简单线性回归的函数形式

三种常用的函数形式，每一种都涉及对数转换：
1. log-lin 模型，其中因变量是对数的，但自变量是线性的$ln Y_{i} = b_{0} + b_{1}X_{i}$
2. lin-log 模型，其中因变量是线性的，但自变量是对数的$ln Y_{i} = b_{0} + b_{1}ln X_{i}$
3. log-log 模型，其中因变量和自变量都是对数形式$ln Y_i = b_{0} + b_{1}ln X_{i}$



## 学习目标

1. 描述一个简单的线性回归模型以及模型中因变量和自变量的作用
2. 描述最小二乘准则，如何使用它来估计回归系数，以及它们的解释
3. 解释简单线性回归模型的假设，并描述残差和残差图如何指示这些假设是否可能被违反
4. 在简单的线性回归中计算和解释决定系数和F统计量
5. 描述回归分析中方差分析 (ANOVA) 的使用，解释方差分析结果，计算和解释简单线性回归中估计的标准误差
6. 制定关于回归系数的总体值的原假设和备择假设，并确定原假设是否在给定的显着性水平上被拒绝
7. 给定估计的线性回归模型和自变量的值，计算和解释因变量的预测值及其预测区间
8. 描述简单线性回归的不同函数形式

