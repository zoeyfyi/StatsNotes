# Test for the variance of a normal distribution

To do a hypothesis test for the variance of a normal distribution we use the $$\chi^2$$ distribution to find are critical value and $$\frac{(n-1)s^2}{\sigma^2}$$ as the test statistic.

#### Example
Some random observations (2.1, 2.3, 3.5, 4.6, 5.0, 6.4, 7.1, 8.6, 8.7, 9.1) are thought to have a variance of 4.1. Test this at a 5% significance level.

###### Hypothesis
$$
H_0: \sigma^2 = 4.1\\
H_1: \sigma^2 \ne 4.1
$$

###### Test statistic
$$
\begin{align}
\bar{x} &= 5.74 \\
s^2 &= 6.940
\end{align}
$$

$$
\frac{9 \times 6.940}{4.1} = 15.234
$$

###### Critical region
$$
\begin{align}
\chi^2_9(0.975) &= 19.023\\
\chi^2_9(0.025) &= 2.700\\
\end{align}
$$

###### Conclusion
$$2.700 < 15.234 < 19.023$$ so accept $$H_0$$