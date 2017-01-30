## Contingency tables
So far we have looked at the frequency a single event happens, but sometimes your interested in the frequencies of two criteria happening.

#### Example
Trains from 3 stations leave late or on-time, test at 5% is their is any association.

|   | On Time | Late |
| --- | --- | --- |
| A | 26 | 14 |
| B | 30 | 10 |
| C | 44 | 26 |

Hypothesis
$$H_0$$: No association
$$H_1$$: Association

Calculate the expected and $$\chi^2$$ values

| $$O_i$$ | $$E_i$$ | $$\frac{(O_i - E_i)^2}{E_i}$$ |
| --- | --- | --- |
| 26 | $$\frac{80}{3}$$ | $$\frac{1}{60}$$ |
| 30 | $$\frac{80}{3}$$ | $$\frac{5}{12}$$ |
| 44 | $$\frac{140}{3}$$ | $$\frac{1}{60}$$ |
| 14 | $$\frac{40}{3}$$ | $$0.152$$ |
| 10 | $$\frac{40}{3}$$ | $$\frac{1}{30}$$ |
| 16 | $$\frac{70}{3}$$ | $$0.305$$ |

$$
\chi^2 = 1.757
$$



Critical region
$$
v = (3-1)*(2-1) = 2
$$$$
\chi^2_2(0.95) = 5.991
$$

$$1.757 < 5.991$$ so accept $$H_0$$, evidence suggests stations and lateness are not associated.