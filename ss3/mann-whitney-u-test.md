# Mann-Whitney U-Test

Mann-Whitney U-Test is another non-parametric test that is used to test if two sample were taken from the same population. It is used when we can do a t-test because the data is not normal.

#### Process

1. Write hypothesis.
2. Rank the data (as if it was just a single set) and calculate the sum of the ranks of each set.
3. Calculate the statistic for each set using $$U = T - \frac{n(n+1)}{2}$$ where $$T$$ is the sum of the ranks and $$n$$ is the sample size. The test statistic is the minimum of the two $$U$$ values
4. Find the critical value on table 11
5. Compare the statistic and critical value, if the statistic is less than the critical value reject $$H_0$$

#### Example
Nine random plants from two sides of a valley where weighed, carry out a Mann-Whitney U test at 5% level of significance.

| East Side | $$27.1$$ | $$40.3$$ | $$15.7$$ | $$36.4$$ | $$16.3$$ | $$15.3$$ | $$32.0$$ | $$15.7$$ | $$27.5$$ |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **West side** | $$11.7$$ | $$14.7$$ | $$19.1$$ | $$22.0$$ | $$6.7$$ | $$14.1$$ | $$20.1$$ | $$24.4$$ | $$15.4$$ |

###### Hypothesis
$$H_0$$: Samples taken from identical populations
$$H_1$$: Samples not taken from identical populations

###### Ranking
| East Side | $$14$$ | $$18$$ | $$7.5$$ | $$17$$ | $$9$$ | $$5$$ | $$16$$ | $$7.5$$ | $$15$$ |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **West side** | $$2$$ | $$4$$ | $$10$$ | $$12$$ | $$1$$ | $$3$$ | $$11$$ | $$13$$ | $$6$$ |

$$
\begin{align}
T_E &= 14 + 18 + ... + 15 = 109\\
T_W &= 2 + 5 + ... + 6 = 62
\end{align}
$$

###### Test statistic
$$
\begin{align}
U_E &= 109 - \frac{9 \times (9 + 1)}{2} = 64\\
U_W &= 62 - \frac{9 \times (9 + 1)}{2} = 17\\
U &= min(64, 17) = 17
\end{align}
$$

###### Critical value
$$
cv = 18
$$

###### Conclusion

$$17 < 18$$, so reject $$H_0$$. The population average weight differs across each side.




