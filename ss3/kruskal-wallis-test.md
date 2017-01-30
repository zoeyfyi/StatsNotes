# Kruskal-Wallis test

Kruskal-Wallis test is a non-parametric version of an ANOVA test to test if their is a difference between some samples. We use this test instead of an ANOVA test if the data is not normally distributed.

#### Process
1. Write hypothesis
2. Rank the data (as if it was just a single set) and calculate the sum of the ranks of each set.
3. Calculate the test statistic using: $$
H = \frac{12}{N(N + 1)} \times \sum{\frac{T_i^2}{n_i}} - 3(N + 1)
$$ where $$T_i$$ is the sum of all ranks in a set of size $$n_i$$ and $$N$$ is the sum of all sample sizes.
4. Find the degrees of freedom, which is the number of samples minus one.
5. Use the $$\chi^2$$ distribution to find the critical value.
6. Compare statistic and critical value, if statistic is larger than critical value reject $$H_0$$.

#### Example
Carry out a Kruskal-Wallis test to see if their is a difference between the fish prices from three different markets at 5% significance level.

| A | B | C |
| --- | --- | --- |
| 220.3 | 190.1 | 228.7 |
| 226.3 | 209.7 | 231.3 |
| 227.3 | 223.4 | 249.6 |
| 228.1 | 224.2 | 260.7 |
| 242.4 | 226.4 | 289.7 |

###### Hypothesis
$$H_0$$: Samples from the same population
$$H_1$$: Samples from the different populations

###### Rank data
| A | B | C |
| --- | --- | --- |
| 3 | 1 | 10 |
| 6 | 2 | 11 |
| 8 | 4 | 13 |
| 9 | 5 | 14 |
| 12 | 7 | 15 |

###### Test statistic
$$
\begin{align}
T_A &= 3 + 6 + ... + 12 = 38\\
T_B &= 1 + 2 + ... + 7 = 19\\
T_C &= 10 + 11 + ... + 15 = 63\\
\end{align}
$$

$$
\begin{align}
\sum\frac{T_i}{n_i} &= \frac{38^2}{5} + \frac{19^2}{5} + \frac{63^2}{5}\\
               &= 1154.8
\end{align}
$$

$$
\begin{align}
H &= \frac{12}{15(15 + 1)} \times 1154.8 - 3(15 + 1)\\
  &= 9.74
\end{align}
$$

###### Critical value
$$
v = 3 - 1 = 2
$$

$$
\chi^2_2(5\%) = 5.991
$$

###### Conclusion
$$9.74 > 5.991$$ so reject $H_0$, samples are not from identical populations