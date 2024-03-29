---
layout: post
title:  "Chi2 Squared Test"
date:  2023-11-11
blurb: "卡方检验"
---

卡方检验是一种用于检验总体的分布和我们预想的分布之间是否一致的假设检验方法。卡方检验使用$\chi^{2}$分布进行检验，是一种非参数假设检验方法。

设待检验的总体的分布函数为$F(X)$，$F_0(X)$为已知分布函数，则卡方检验的零假设和备择假设分别为

$$
\begin{aligned}
    H_0 &: F(X)=F_0(X) \\
    H_1 &: F(X)\not=F_0(X)
\end{aligned}
$$

卡方检验最适用于离散变量的检验，对于连续型随机变量，可以将数轴划分为多段来进行检验。我们首先需要计算$\chi^2$统计量（其中$n_i$为第i类的值被称为**实际频数**，$E(n_i)$为理论上的期望值也称**理论频数**）

$$
\chi^{2}=\sum_{i=1}^{k}\frac{(n_i-E(n_i))^2}{E(n_i)}
$$

计算得到$\chi^{2}$统计量后，第二步是计算对应卡方分布自由度，第三步则是根据拒绝域和自由度来**查表**并与上面得到的卡方统计量进行比较，并根据比赛的结果来判断是否拒绝原假设。

卡方检验的基本上来讲有两种用法：

+ 拟合优度检验：看实际数据的分布与理论分布的区别
+ 独立性检验：看A与B两个变量之间是否独立

对于这两种情况，我们都需要将原数据分为不相交的K类。尤其是对于第二类用法，我们实际上常将其用于检测变量和输出是否独立。

第一种情况是容易说明和理解的，我们计算$\chi^2$统计量时，如果两个分布是接近的，那么实际频数和理论频数就会很接近，那么这个统计量值就会较小。第一种情况下，卡方分布自由度为K-1且由于此时我们有一个假设的理论分布（如假设原分布为泊松分布），$E(n_i)$是不难计算的。

第二种情况则需要我们建立一个列联表，假设A有R种取值，B有C种取值，总共有N个样本。那么我们可以用一个如下的2x2列联表来举例：

<div style="margin: 0 auto; display: table;">
  <table>
        <tr>
            <td></td>
            <td>$c_1$</td>
            <td>$c_2$</td>
            <td>$R_{all}$</td>
        </tr>
        <tr>
            <td>$r_1$</td>
            <td>$O_{1,1}$</td>
            <td>$O_{1,2}$</td>
            <td>$O_{1,}$</td>
        </tr>
        <tr>
            <td>$r_2$</td>
            <td>$O_{2,1}$</td>
            <td>$O_{2,2}$</td>
            <td>$O_{2,}$</td>
        </tr>
        <tr>
            <td>$C_{all}$</td>
            <td>$O_{,1}$</td>
            <td>$O_{,2}$</td>
            <td>N</td>
        </tr>
    </table>
</div>

此时的卡方统计量公式为：

$$
\chi^2=\sum^{R}_{r=1}\sum^{C}_{c=1}\frac{(O_{r,c}-E(O_{r,c}))^2}{E(O_{r,c})}
$$

其中

$$
E(O_{r,c})=N*E(O_{,c})*E(O_{r,})=\frac{ O_{,c}*O_{r,} }{N}
$$

这里可以直接利用期望的性质展开，是由于我们是进行独立性假设的检验，所以我们的理论频数是直接按照独立来计算的。此时，我们的卡方分布的自由度为$(R-1)*(C-1)$。

若要计算多个变量与B是否独立，则需要建立多个列联表来进行分别计算。

