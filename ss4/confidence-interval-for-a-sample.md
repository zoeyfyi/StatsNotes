## Confidence interval for a sample
If we have a small sample of values and we assume they came from a normal distribution, we can use the t-distribution to find the confidence interval for the sample using:
$$
\bar{x} \pm t_{n-1}(\alpha) \times \frac{s}{\sqrt{n}}
$$
where $$\bar{x}$$ is the sample mean, $$n$$ is the sample size, $$\alpha$$ is $$\frac{1 - \text{significance level}}{2}$$ and $$s$$ is the sample standard deviation.

#### Example
Let $$n = 26$$, $$\bar{x} = 122$$ and $$s^2 = 225$$. Calculate a 95% confidence interval.

$$
\begin{align}
122 \pm t_{26-1}(0.025) \times \frac{\sqrt{225}}{\sqrt{26}} &=\\
122 \pm 2.060 \times 3.132&= (115.941, 128.059)\\
\end{align}
$$

