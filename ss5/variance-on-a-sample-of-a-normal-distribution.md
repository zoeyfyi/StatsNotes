# Variance on a sample of a normal distribution

### Confidence interval for the variance of a normal distribution
For a random sample of $$N(\mu, \sigma^2)$$ it is known that $$\frac{(n-1)s^2}{\sigma^2}$$ has a $$\chi^2_{n-1}$$ distribution.

#### Example
Calculate a 95% confidence interval for the mean and variance of the set: 266, 254, 215, 220, 253, 230, 216, 248, 234, 244.

Sample mean and variances estimator
$$
\begin{align}
\bar{x} &= 238 \\
s^2 &= 313.111
\end{align}
$$

$$
\chi^2_9(0.975) < \frac{(n-1)s^2}{\sigma^2} < \chi^2_9(0.075)\\
\quad\\
\chi^2_9(0.975) < \frac{9 \times 313.111}{\sigma^2} < \chi^2_9(0.075)\\
\quad\\
\frac{9 \times 313.111}{\chi^2_9(0.975)} < \sigma^2 < \frac{9 \times 313.111}{\chi^2_9(0.075)}
\quad\\
\quad\\
148.128 < \sigma^2 < 1043.553\\
\quad\\
(148.128, 1043.553)\\
$$

### Hypothesis test for the variance of a normal distribution

To do a hypothesis test for the variance of a normal distribution we use the $$\chi^2$$ distribution to find are critical value and $$\frac{(n-1)s^2}{\sigma^2}$$ as the test statistic.

#### Example
Some random observations (2.1, 2.3, 3.5, 4.6, 5.0, 6.4, 7.1, 8.6, 8.7, 9.1) are thought to have a variance of 4.1. Test this at a 5% significance level.

Sample mean and variances estimator
$$
\begin{align}
\bar{x} &= 5.74 \\
s^2 &= 6.940
\end{align}
$$

Critical region
$$
\begin{align}
\chi^2_9(0.975) &= 19.023\\
\chi^2_9(0.025) &= 2.700\\
\end{align}
$$
So
$$
\begin{align}
\frac{(n-1)s^2}{\sigma^2} &\geq 19.023\\
\frac{(n-1)s^2}{\sigma^2} &\leq 2.700\\
\end{align}
$$

Test statistic
$$
\frac{9 \times 6.940}{4.1} = 15.234
$$

$$2.700 < 15.234 < 19.023$$ so accept $$H_0$$