## Difference between distributions
Sometimes we are interested in the difference between two independent populations.

To test two distributions we can use the rules for combining distributions to derive this test statistic for two normal distributions $X$ and $Y$:
$$
Z = \frac{\bar{X} - \bar{Y} - (\mu_x - \mu_y)}
{\sqrt{\frac{\sigma_x^2}{n_x}+\frac{\sigma_y^2}{n_y}}}
$$

If $n_x$ and $n_y$ are larger enough, this statistic can be used for distributions where $X$ and $Y$ are not normal

#### Example
A study weighs children in area $A$ and area $B$. The results are as follows:
| | $n$ | $\bar{x}$ | $s$ |
| --- | --- | --- | --- |
| $A$ | 220 | 37.8 | 3.6 |
| $B$ | 180 | 38.6 | 4.1 |

#####a. Test at a 5% level of significance the difference in the mean weight of two children.	
Hypothesis:
$$
H_0: \mu_A = \mu_B\\
H_1: \mu_A \neq \mu_B\\
$$

Test statistic:
$$
\begin{align}
z &= \frac{\bar{x}_A - \bar{x}_B - (\mu_A - \mu_B)}{\sqrt{\frac{\sigma_A^2}{n_A}+\frac{\sigma_B^2}{n_B}}}\\
  &= \frac{37.6 - 38.6}{\sqrt{\frac{3.6^2}{220}+\frac{4.1^2}{180}}}\\
  &= -2.56243...\\
  &= -2.56\\
\end{align}
$$

Test is two tails at 5%, so critical values are $z = \pm1.96$

Since $-2.56 < -1.96$, the result is significant so reject $H_0$, their is evidence that the mean weight is different in the two areas.

#####b. State any assumptions made
The test required $\sigma$ so it was assumed $s^2 = \sigma^2$ for the samples. We also assumed that both distributions were normally distributed because of their large sample size. 