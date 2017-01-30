### Estimating population parameters

> **Population parameter**: A characteristic of a population.
###### 
> **Estimator**: A statistic used to estimate a population parameter.

#### Example 1
For a random sample $X_1, X_2, ..., X_n$ with a distribution $X \sim N(\mu, \sigma^2)$ show that $E(\bar{X}) = \mu$

$$
\begin{align}
    \bar{X} &= \frac{1}{n}(X_1 + ... + X_n)\\
E(\bar{X}) &= \frac{1}{n}E(X_1 + ... + X_n)\\
                 &= \frac{1}{n}[E(X_1) + ... + E(X_n)]\\
                 &= \frac{1}{n}[\mu + ... + \mu]\\
                 &= \frac{n\mu}{n})\\
                 &= \mu
\end{align}
$$

$$
\begin{align}
    &\bar{X} = \frac{1}{n}(X_1 + ... + X_n)\\
&E(\bar{X}) = \frac{1}{n}E(X_1 + ... + X_n)\\
                 &= \frac{1}{n}[E(X_1) + ... + E(X_n)]\\
                 &= \frac{1}{n}[\mu + ... + \mu]\\
                 &= \frac{n\mu}{n})\\
                 &= \mu
\end{align}
$$

This means that $\bar{X}$ is an estimator for $\mu$ and on average, should give the correct result. This means $\bar{X}$ is an unbiased estimator for $\mu$

#### Example 2
Bolts of lengths 5cm and 10cm are produced in the ration 2:1 respectively. For a random sample of 3 bolts calculate the bias of the estimator of the mode.

Population mode is 5cm, because their are twice as many 5cm bolts as their are 10cm bolts.

All possible samples
$$
(5, 5, 5),\\
(5, 5, 10), (5, 10, 5), (10, 5, 5),\\
(5, 10, 10), (10, 5, 10), (10, 10, 5),\\
(10, 10, 10)\\
$$
Let $M$ be the sampling distribution for the population mode.
$$
\begin{align}
P(M = 5) &= (\frac{2}{3}^3 \times 1) + (\frac{2}{3}^2 \times \frac{1}{3} \times 3) \\
              &= \frac{8}{27} + \frac{4}{27} \times 3 \\
              &= \frac{20}{27}\\
\end{align}
$$

$$
\begin{align}
P(M = 10) &= (\frac{1}{3}^3 \times 1) + (\frac{2}{3} \times \frac{1}{3}^2 \times 3) \\
              &= \frac{1}{27} + \frac{2}{27} \times 3 \\
              &= \frac{7}{27}\\
\end{align}
$$

estimator of mode:
$$
\begin{align}
E(M) &= 5 \times \frac{20}{27} + 10 \times \frac{7}{27}\\
              &= \frac{100}{27} + \frac{70}{27} \\
              &= \frac{170}{27}
\end{align}
$$

bias:
\begin{align}
\text{bias} &= E(M) - \text{mode}\\
              &= \frac{170}{27} - 5 \\
              &= \frac{35}{27} \\
              &= 1.30...
\end{align}

### Standard error of the mean

 $$E(\bar{X}) = \mu$$  $$\text{Var}(\bar{X}) = \frac{\sigma^2}{n}$$ 
 Notice how the variance of the estimator decreases as the number of samples increases which means that the estimate for $\mu$ gets more accurate. In calculations its useful to find the standard error, a measure of a statistics accuracy, which is the standard deviation. The standard error of the estimator for $\mu$ is:
 $$\text{standard error} = \sqrt{\text{Var}(\bar{X})} = \sqrt{\frac{\sigma^2}{n}} = \frac{\sigma}{\sqrt{n}}$$ 

#### Example
Prospective army recruits are receiving a medial test across two days. Let $p$ be the independent probability a person parses, $n$ the number of people seen on the first day, $2n$ the number of people seen on the second day, $X_1$ the number who pass the test on the first day and $X_2$ those that pass on the second day.

1. Show that $X = \frac{1}{2}(\frac{X_1}{n} + \frac{X_2}{2n})$ is an unbiased estimator of $p$.
$$
\begin{align}
    X &= \frac{1}{2}(\frac{X_1}{n} + \frac{X_2}{2n})\\
E(X) &= \frac{1}{2}(\frac{E(X_1)}{n} + \frac{E(X_2)}{2n})\\
       &= \frac{1}{2}(\frac{np}{n} + \frac{2np}{2n})\\
       &= \frac{1}{2}(p + p)\\
       &= p\\
\end{align}
$$

2. Show that $Y = \frac{X_1 + X_2}{3n}$ is an unbiased estimator of $p$.
    Distribution is binomial so the mean: $np$
$$
\begin{align}
    Y &= \frac{X_1 + X_2}{3n}\\
E(Y) &= \frac{E(X_1) + E(X_2)}{3n}\\
       &= \frac{np + 2np}{3n}\\
       &= \frac{3np}{3n}\\
       &= p\\
\end{align}
$$

3. Which is the better statistics.
    Distribution is binomial so the variation: $np(1-p)$
$$
\begin{align}
\text{Var}(X) &= \text{Var}(\frac{1}{2} \times (\frac{X_1}{n} + \frac{X_2}{2n}))\\
                     &= \frac{1}{4}(\text{Var}(\frac{X_1}{n}) + \text{Var}(\frac{X_2}{2n}))\\
                     &= \frac{1}{4}(\frac{1}{n^2} \times np(1-p) + \frac{1}{4n^2} \times np(1-p))\\
                     &= \frac{1}{4}(\frac{p(1-p)}{n} + \frac{p(1-p)}{4n})\\
                     &= \frac{5p(1-p)}{16n}\\
\end{align} 
$$

$$
\begin{align}
\text{Var}(Y) &= \text{Var}(\frac{X_1 + X_2}{3n})\\
                     &= \frac{1}{9n^2}(\text{Var}({X_1}) + \text{Var}(X_2))\\
                     &= \frac{1}{9n^2}(3np(1-p))\\
                     &= \frac{p(1-p)}{3n}\\
\end{align} 
$$

$$
\frac{15p(1-p)}{48n} < \frac{16p(1-p)}{48n}\\
\text{Var}(X) < \text{Var}(Y)
$$
So X is the better estimator.