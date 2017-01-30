### Sign test

The sign test is a **distribution free** test since it doesn't require the data to follow a particular distribution. It works by checking if their is a significant difference in the median value of the samples by comparing each value pair. Unlike the Wilcoxon test the distribution does not have to be symmetrical. 

#### Process
1. Set up hypothesis.
2. Find the sign of the difference ignoring any pairs that are equal. 
3. Count the number of positive and negative signs (these are your test statistics)
4. Find the value of $$P(X < min(a, b) | X \sim B(n, \frac{1}{2}))$$ where $$a$$ and $$b$$ are the number of each sign (test statistics) and $$n$$ is number of all valid signs \(not Nan\)
5. Compare this value with the significant level, if its less than the significant level reject $$H_0$$.

#### Example

Test is their is a difference in the aerosols average effectiveness at a 10% significance level.

###### Hypothesis

$$H_0$$: Population median difference $$\eta_d = 0$$  
$$H_1$$: Population median difference $$\eta_d \neq 0$$

###### Signs

| Patient | Aerosol A | Aerosol B | sign |
| --- | --- | --- | --- |
| 1 | 28 | 24 | + |
| 2 | 22 | 16 | + |
| 3 | 10 | 5 | + |
| 4 | 40 | 17 | + |
| 5 | 18 | 23 | - |
| 6 | 52 | 57 | - |
| 7 | 49 | 30 | + |
| 8 | 40 | 16 | + | 
| 9 | 34 | 14 | + |

###### Test statistic


$$
2^-, 7^+\\
X \sim B(9, \frac{1}{2})\\
\begin{align}
P(X \leq min(2, 7)) &= P(X \leq 2)\\
                    &= 0.0898
\end{align}
$$


###### Conclusion

$$0.0898 > 0.05$$ so accept $$H_0$$, the evidence suggests their is no difference in the average effectiveness of the aerosols.

