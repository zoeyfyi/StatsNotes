## Hypothesis test for mean of normal distribution with unknown variance
If the variance is unknown and we assume the sample is normal, we can use the t-distribution to carry out a hypothesis test for the mean.

#### Example
Let $$n = 20$$, $$\sum{x} = 21.7$$, $$\sum{x^2} = 28.4$$. Test the mean is larger than one at a 10% significance level.

###### Hypothesis
$$
H_0: \mu = 1.00\\
H_1: \mu > 1.00
$$

###### Test statistic
$$
\bar{x} = \frac{21.7}{20} = 1.085\\
s = \sqrt{\frac{1}{20 - 1} \times (28.4 - \frac{21.7^2}{20})} = 0.5055
$$
$$
\frac{1.085 - 1}{\frac{0.5055}{\sqrt{20}}} = 0.752
$$

###### Critical value
$$
t = t_{19}(0.90) = 1.3278
$$

###### Conclusion
$$0.752 < 1.3278$$ so accept $$H_0$$ and reject $$H_1$$, their is not evidence to support the statement that the mean is larger than one.