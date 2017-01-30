## Students t-distribution
If the population variance is unknown we know and $$X$$ follows a normal distribution then provided $$n$$ was large:
$$
\frac{(\bar{X} - \mu)}{\frac{S}{\sqrt{n}}} \approx N(0, 1^2)
$$

However if $$n$$ is small we can use t-distribution to get a better estimate.
$$
\frac{(\bar{X} - \mu)}{\frac{S}{\sqrt{n}}} \approx t_{n-1}\text{-distribution}
$$

### Confidence intervals
Let $$n = 26$$, $$\bar{x} = 122$$ and $$s^2 = 225$$. Calculate a 95% confidence interval.

$$
\begin{align}
122 \pm t_{26-1}(0.025) \times \frac{\sqrt{225}}{\sqrt{26}} &=\\
122 \pm 2.060 \times 3.132&= (115.941, 128.059)\\
\end{align}
$$

### Hypothesis test for mean of normal distribution with unknown varience
Let $$n = 20$$, $$\sum{x} = 21.7$$, $$\sum{x^2} = 28.4$$, $$H_0: \mu = 1.00$$, $$H_1: \mu > 1.00$$. Test the hypothesis at a 10% significance level

Sample mean and estimator of variance
$$
\bar{x} = \frac{21.7}{20} = 1.085\\
s = \sqrt{\frac{1}{20 - 1} \times (28.4 - \frac{21.7^2}{20})} = 0.5055
$$

Test statistic
$$
\frac{1.085 - 1}{\frac{0.5055}{\sqrt{20}}} = 0.752
$$

Critical value
$$
t = t_{19}(0.90) = 1.3278
$$

$$0.752 < 1.3278$$ so accept $$H_0$$ and reject $$H_1$$.