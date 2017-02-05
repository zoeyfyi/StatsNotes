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

