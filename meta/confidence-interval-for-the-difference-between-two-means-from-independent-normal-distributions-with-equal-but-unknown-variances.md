# Confidence interval for the difference between two means from independent normal distributions with equal but unknown variances.
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

