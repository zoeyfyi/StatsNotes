## Quality of tests and estimators

### Type I and II errors

When we are conducting hypothesis tests their are two possible errors that can occur.

| $ $ | $H_0$ is true | $H_0$ is false |
| --- | --- | --- |
| **Accept** $H_0$ | OK | Type II error |
| **Reject** $H_0$ | Type I error | OK |

#### Probability of an error
To find the probability of an error do the following:

Given $H_0: p = \frac{1}{4}$, $H_1: p > \frac{1}{4}$, $\text{critical region}: X \geq 9$ and $X \sim B(20, \frac{1}{4})$

$$
\begin{align}
P(\text{type I error}) &= P(\text{Reject } H_0 \text{ when } H_0 \text{ is true}) \\
                                  &= P(X \geq 9 | X \sim B(20, 0.25))\\
                                  &= 0.0409
\end{align}
$$

Given $p$ is actually equal to $0.35$:

$$
\begin{align}
P(\text{type II error}) &= P(\text{Accept } H_0 \text{ when } H_0 \text{ is false}) \\
                                  &= P(X \leq 8 | X \sim B(20, 0.35))\\
                                  &= 0.7624
\end{align}
$$

### Power and size

The **size** of a test is equal to $P(\text{Type I Error})$. The **power** of a test is equal to the $P(\text{Rejecting } H_0 | H_0 \text{ is false})$ or $1 - P(\text{Type II Error})$. It follows that increasing the sample size will increase the power of the test, since it will decrease $P(\text{Type II Error})$.

To calculate $P(\text{Type II Error})$ you must have a population parameter which would not usually be known. In these cases we create a **power function** which returns the power of the test for any value of the population parameter.

#### Example
Given $P(\text{Type II Error}) = P(X \leq 6 | \lambda > 3.5)$
$$
\begin{align}
  P(\text{Type II Error}) &= e^{-\lambda}  + \lambda e^{-\lambda} + \frac{\lambda^2}{2!} e^{-\lambda} + \frac{\lambda^3}{3!} e^{-\lambda} + \frac{\lambda^4}{4!} e^{-\lambda} + \frac{\lambda^5}{5!} e^{-\lambda} + \frac{\lambda^6}{6!} e^{-\lambda}\\
                                     &= e^{-\lambda} (1  + \lambda + \frac{\lambda^2}{2!} + \frac{\lambda^3}{3!} + \frac{\lambda^4}{4!} + \frac{\lambda^5}{5!} + \frac{\lambda^6}{6!})\\
\text{Power}(\lambda) &=  1 - e^{-\lambda} (1  + \lambda + \frac{\lambda^2}{2!} + \frac{\lambda^3}{3!} + \frac{\lambda^4}{4!} + \frac{\lambda^5}{5!} + \frac{\lambda^6}{6!})\\
\end{align}
$$

As a table of values:
| $\lambda$ | Power |
| --- | --- |
| 4 | 0.1107 |
| 5 | 0.2376 |
| 6 | 0.3937 |
| 7 | 0.5503 |
| 8 | 0.6866 |
| 9 | 0.7932 |
| 10 | 0.8699 |

### Comparing estimators
Let $S = \frac{\bar{X} + \bar{Y}}{2}$ and $T = \frac{6\bar{X} + 4\bar{Y}}{10}$. 

We can easily prove these are both unbiased estimators of $\mu$:
$$
\begin{align}
E(S) &= E(\frac{\bar{X} + \bar{Y}}{2})\\
       &= \frac{1}{2} E(\bar{X} + \bar{Y})\\
       &= \frac{1}{2} E(\bar{X}) + \frac{1}{2} E(\bar{Y})\\
       &= \frac{1}{2} \mu + \frac{1}{2} \mu\\
       &= \mu
\end{align}
$$

$$
\begin{align}
E(T) &= E(\frac{6\bar{X} + 4\bar{Y}}{10})\\
       &= \frac{1}{10} E(6\bar{X} + 4\bar{Y})\\
       &= \frac{6}{10} E(\bar{X}) + \frac{4}{10} E(\bar{Y})\\
       &= \frac{6}{10} \mu + \frac{4}{10} \mu\\
       &= \mu
\end{align}
$$

But which is the better estimator. If the estimator with the smaller variance will be closer to the mean, hence be the better estimator. So between $S$ and $T$ given $\bar{X} = \frac{1}{6}\sigma^2$ and $\bar{Y} = \frac{1}{4}\sigma^2$:
$$
\begin{align}
Var(S) &= Var(\frac{\bar{X} + \bar{Y}}{2})\\
       &= \frac{1}{2}^2 Var(\bar{X} + \bar{Y})\\
       &= \frac{1}{4} Var(\bar{X}) + \frac{1}{4} Var(\bar{Y})\\
       &= \frac{1}{4} \times  \frac{1}{6}\sigma^2  + \frac{1}{4} \times \frac{1}{4}\sigma^2\\
       &= \frac{1}{24}\sigma^2 + \frac{1}{8}\sigma^2\\
       &= \frac{5}{48}\sigma^2
\end{align}
$$

$$
\begin{align}
Var(T) &= Var(\frac{6\bar{X} + 4\bar{Y}}{10})\\
       &= \frac{1}{10}^2 Var(6\bar{X} + 4\bar{Y})\\
       &= \frac{1}{100} Var(\bar{X}) + \frac{1}{100} Var(\bar{Y})\\
       &= \frac{1}{100} \times  \frac{36}{6}\sigma^2  + \frac{1}{100} \times \frac{16}{4}\sigma^2\\
       &= \frac{36}{600}\sigma^2 + \frac{16}{400}\sigma^2\\
       &= \frac{1}{10}\sigma^2
\end{align}
$$

$\frac{5}{48} > \frac{1}{10}$ so $T$ is the better estimator since it has a smaller variance.

### Consistent estimators
Estimators are **consistent** if their variation approaches zero as the sample size approaches infinity. An **asymptotically unbiased** estimator for $\theta$ occurs when the expectation of a distribution approaches the value of $theta$ as the sample size approaches infinity.

#### Example 1
$Var(\bar{X}) = \frac{\sigma^2}{n}$ is a consistent estimator since as $n \to \infty$, $ \frac{\sigma^2}{n} \to 0$

#### Example 2
Let $p$ be the probability of rolling a 6, $X$ the number of sixes in one trial with $n samples$ and $Y$ the number of sixes with the same sample size.

Show $\hat{p_1} = \frac{3\bar{X} + 4\bar{Y}}{7n}$ is unbiased and consistent.

$$
\begin{align}
E(\hat{p_1}) &= E(\frac{3\bar{X} + 4\bar{Y}}{7n})\\
             &= \frac{1}{7n}E(3\bar{X} + 4\bar{Y})\\
             &= \frac{3}{7n}E(\bar{X}) + \frac{4}{7n}E(\bar{Y})\\
             &= \frac{3np}{7n} + \frac{4np}{7n}\\
             &=\frac{3}{7}p + \frac{4}{7}p\\
             &=p
\end{align}
$$

$$
\begin{align}
Var(\hat{p_1}) &= Var(\frac{3\bar{X} + 4\bar{Y}}{7n})\\
               &= \frac{1}{49n^2} Var(3\bar{X} + 4\bar{Y})\\
               &= \frac{9}{49n^2} Var(\bar{X}) + \frac{16}{49n^2} Var(\bar{Y})\\
               &= \frac{9np(1-p)}{49n^2} + \frac{16np(1-p)}{49n^2} \\
               &= \frac{9np(1-p) + 16np(1-p)}{49n^2}\\
               &= \frac{25np(1-p)}{49n^2}\\
               &= \frac{25p-25p^2}{49n}\\
\end{align}
$$

as $n \to \infty $, $\frac{25p-25p^2}{49n} \to 0$, hence $\hat{p_1}$ is a consistent estimator for $p$.