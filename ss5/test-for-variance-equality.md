## Test equal variances of two normal distributions

If we assume $$\sigma^2_x = \sigma^2_y$$ then 
$$
\frac{\frac{s_y^2}{\sigma_y^2}}{\frac{s_x^2}{\sigma_x^2}} \sim F_{n_x-1, n_y-1}
$$

becomes

$$
\frac{s_y^2}{s_x^2} \sim F_{n_x-1, n_y-1}
$$

which is are test statistic

#### Example
It is believed that wood stored inside has less variable hardness than wood stored outside, conduct a test at a 0.05 significance level stating any assumptions made.

|  | Outside | Inside |
| --- | --- | --- |
| **Sample size** | 25 | 21 |
| **Mean hardness** | 110 | 122 |
| **Sample variance** | 216.25 | 198.6 |

Hypothesis

$$
H_0: \sigma_o^2 = \sigma_i^2\\
H_1: \sigma_o^2 > \sigma_i^2\\
$$

Test statistic

$$
\begin{align}
F_{\text{test}} &= \frac{216.25}{198.6}\\
                &= 1.089
\end{align}
$$

Critical region
$$
\begin{align}
F_{\text{crit}} &= F_{25-1, 21-1}(0.05)\\
                &= F_{24, 20}(0.05)\\
                &= 2.08
\end{align}
$$

$$1.089 < 2.08$$ so accept $$H_0$$, wood stored inside is just as variable as wood stored outside.