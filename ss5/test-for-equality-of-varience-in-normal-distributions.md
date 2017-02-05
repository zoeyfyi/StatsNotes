## Difference between distributions
Sometimes we are interested in the difference between two independent populations.

To test two distributions we can use the rules for combining distributions to derive this test statistic for two normal distributions $$X$$ and $$Y$$:
$$
Z = \frac{\bar{X} - \bar{Y} - (\mu_x - \mu_y)}
{\sqrt{\frac{\sigma_x^2}{n_x}+\frac{\sigma_y^2}{n_y}}}
$$

If $$n_x$$ and $$n_y$$ are larger enough, this statistic can be used for distributions where $$X$$ and $$Y$$ are not normal.

#### Example
A study weighs children in area $$A$$ and area $$B$$. The results are as follows:

| | $$n$$ | $$\bar{x}$$ | $$s$$ |
| --- | --- | --- | --- |
| $$A$$ | 220 | 37.8 | 3.6 |
| $$B$$ | 180 | 38.6 | 4.1 |

Test at a 5% level of significance the difference in the mean weight of two children.	

###### Hypothesis
$$
H_0: \mu_A = \mu_B\\
H_1: \mu_A \neq \mu_B\\
$$

###### Test statistic
$$
\begin{align}
z &= \frac{\bar{x}_A - \bar{x}_B - (\mu_A - \mu_B)}{\sqrt{\frac{\sigma_A^2}{n_A}+\frac{\sigma_B^2}{n_B}}}\\
  &= \frac{37.6 - 38.6}{\sqrt{\frac{3.6^2}{220}+\frac{4.1^2}{180}}}\\
  &= -2.56243...\\
  &= -2.56\\
\end{align}
$$

###### Critical value
$$z = \pm1.96$$


###### Conclusion
Since $$-2.56 < -1.96$$, the result is significant so reject $$H_0$$, their is evidence that the mean weight is different in the two areas.

### Confidence interval for the difference between two means from independent normal distributions with equal but unknown variances.
We already know that if the sample size is large
$$
N(0, 1^2) \approx \frac{\bar{X} - \bar{Y} - (\mu_x - \mu_y)}
{\sqrt{\frac{\sigma_x^2}{n_x}+\frac{\sigma_y^2}{n_y}}}
$$

but if its small then we must make 3 assumptions:

- The population is normal
- Samples are independent
- Variance is equal

Since the variances must be equal we can use the pooled estimator for variances and substitute $S_p$ for $\sigma_x$ and $\sigma_y$ to end up with:
$$
\frac{\bar{X} - \bar{Y} - (\mu_x - \mu_y)}{\sqrt{S_p^2(\frac{1}{n_x}+\frac{1}{n_y}})} \sim t_(n_x + n_y - 2)
$$

Therefor the limits are given by:
$$
\begin{align}
P(-t_{\text{crit}} < t_{(n_x + n_y-2)} < t_{\text{crit}}) &= 0.95\\
P(-t_{\text{crit}} < \frac{\bar{X} - \bar{Y} - (\mu_x - \mu_y)}{\sqrt{S_p^2(\frac{1}{n_x}+\frac{1}{n_y}})} < t_{\text{crit}}) &= 0.95\\
P(-t_{\text{crit}}\sqrt{S_p^2(\frac{1}{n_x}+\frac{1}{n_y}}) < \bar{X} - \bar{Y} - (\mu_x - \mu_y) < t_{\text{crit}}\sqrt{S_p^2(\frac{1}{n_x}+\frac{1}{n_y}})) &= 0.95\\
\end{align}
$$

Therefore the confidence limits for $(\mu_x - \mu_y)$ are therefore given by:
$$
(\bar{x} - \bar{y}) \pm t_{\text{crit}}\sqrt{S_p^2(\frac{1}{n_x}+\frac{1}{n_y}})
$$


#### Example
Samples of the pertol consumption of 2 and 1.6 liter cars has been collected:
**2 liter**: 34.4, 32.1 30.1, 32.8, 31.5, 35.8, 28.2, 26.6, 28.8, 28.5, 33.6, 28.8
**1.6 liter**: 35.3, 34.0, 36.7, 40.9, 34.4, 39.8, 33.6, 36.7, 34.0, 39.2, 39.8, 38.7, 40.8, 35.0, 36.7

Find a 95% confidence interval: 

 Varibles 
 $$
 n_y = 12\\
 \bar{y} = 30.933\\
 s_y^2 = 8.7177
 $$
$$
 n_x = 15\\
 \bar{x} = 37.04\\
 s_x^2 = 6.894
 $$
$$
s_p^2 = \frac{6.894 \times (15 - 1) + 8.7177 \times (12 - 1)}{12 + 15 -2} = 7.459
$$
$$
t_{\text{crit}} = t_{12 + 15 -2}(0.975) = 2.060
$$

So confidence interval is:
$$
(37.04 - 30.933) \pm 2.060 \times \sqrt{7.459 \times (\frac{1}{15} + \frac{1}{12})}\\
(3.928, 8.286)
$$

### Two sample t-test
We can use the same method to test if two random variables (where t applies) have different means. 

#### Example
Group X: 40, 37, 45, 34, 30, 41, 42, 43, 36
Group Y: 38, 43, 36, 45, 35, 44, 41

##### State any assumptions that need to be made in order to conduct a difference of means test on this data.
- Normaly distributed
- Independent
- Populations have the same variance

##### Conduct the test at a 10% significance level.
Hypothesis
$$
H_0: \mu_x = \mu_y \\
H_1: \mu_x \ne \mu_y
$$

Varibles
$$
n_x = 9\\
\bar{x} = 38.667\\
s_x^2 = 23 
$$
$$
n_y = 7\\
\bar{y} = 40.286\\
s_y^2 = 15.905 
$$

Statistic
$$
s_p^2 = \frac{(9 - 1) \times 23 + (7 - 1) \times 15.905}{9 + 7 - 2} = 19.959\\
$$
$$
t = \frac{38.667 - 40.286}{\sqrt{19.959 \times (\frac{1}{9} + \frac{1}{7})}} = -0.719\\
$$

Critical value
$$
t_{9 + 7 - 2}(0.95) = t_{14}(0.95) = 1.761
$$

$-1.761 < -0.719 < 1.761$ so accept $H_0$, evidence suggests their is no difference in the means of the two groups.