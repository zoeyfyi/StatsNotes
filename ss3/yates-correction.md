### Yates correction
For contingency tables that are 2x2 we uses yates correction since it gives us a better result.

$$\chi^2_\text{Yates} = \frac{(|O_i - E_i| - 0.5)^2}{E_i}$$

#### Example
Test the results of a drug trial at a 5% significance level.
| $ $ | Cold | No cold |
| --- | --- | --- |
| **Drug** | 34 | 66 |
| **Dummy pill** | 45 | 55 |

Hypothesis
$H_0$: No association
$H_1$: Association

Calculate the expected and $\chi^2$ values

| $$O_i$$ | $$E_i$$ | $$\frac{(|O_i - E_i| - 0.5)^2}{E_i}$$ |
| --- | --- | --- |
| 34 | 39.5 | 0.633 |
| 45 | 39.5 | 0.633 |
| 66 | 60.5 | 0.413 |
| 55 | 60.5 | 0.413 |

$$
\chi^2 = 2.09
$$

Critical region
$$
v = (2-1)*(2-1) = 1
$$$$
\chi^2_1(0.95) = 3.841
$$

$$2.09 < 3.841$$ so accept $$H_0$$, no evidence to show drug is effective.