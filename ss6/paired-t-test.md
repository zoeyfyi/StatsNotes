### Paired t-test
Sometimes we are interested in the difference of two distributions such as before and after taking a drug. We can do this with a paired t-test. First we find the difference which we treat like a random sample from a $N(\mu, \sigma^2)$ distribution. If their is no difference in results we would expect the mean if differences to be zero i.e $\bar{D} \sim N(0, \frac{\sigma^2}{n})$. So the test statistic for a paired t-test is:
$$
t = \frac{(\bar{D} - \mu_D)}{\frac{S}{\sqrt{n}}} \sim t_{n-1}
$$

#### Example
Reaction times before and after drinking alcohol where recorded:
| Person | A | B | C | D | E | F | G | H | I | J |
| --- |
| Reaction time before | 0.8 | 0.2 | 0.4 | 0.6 | 0.4 | 0.6 | 0.4 | 0.8 | 1.0 | 0.9 |
| Reaction time after | 0.7 | 0.5 | 0.6 | 0.8 | 0.8 | 0.6 | 0.7 | 0.9 | 1.0 | 0.7 |

##### Test at 5% is the reaction times had increased

Calculate the difference:
| Person | A | B | C | D | E | F | G | H | I | J |
| --- |
| Difference | -0.1 | 0.3 | 0.2 | 0.2 | 0.4 | 0.0 | 0.3 | 0.1 | 0.0 | -0.2 |

Hypothesis
$$
H_0: \mu_d = 0\\
H_1: \mu_d > 0
$$

Statistic
$$
\bar{d} = 0.12\\
s^2 = 0.0373
$$
$$
\frac{0.12 - 0}{\frac{\sqrt{0.0373}}{\sqrt{10}}} = 1.965
$$

Critical region
$$
t_{10-1}(0.95) = 1.833
$$

$1.965 > 1.833$ so reject $H_0$ and accept $H_1$. Their is evidence that suggests alcohol effects reaction times in this sample.