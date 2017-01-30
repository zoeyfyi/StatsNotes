### Sign test

The sign test is a **distribution free** test since it doesn't require the data to follow a particular distribution. Its also very simple, just find the sign of the difference ignoring any pairs that are equal. Then use $$P(X < min(a, b) | X \sim B(n, \frac{1}{2})$$ where $$a$$ and $$b$$ are the number of each sign and n is number of all valid signs \(not Nan\). This tests the median value of the data.

#### Example

Test is their is a difference in the aerosols average effectiveness at a 10% significance level.

###### Hypothesis

$$H_0$$: Population mean difference $$\eta_d = 0$$  
$$H_1$$: Population mean difference $$\eta_d \neq 0$$

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
X \sim B(9, \frac{1}{2})\\
\begin{align}
P(X \leq min(2, 7)) &= P(X \leq 2)\\
                    &= 0.0898
\end{align}
$$


###### Conclusion

$$0.0898 > 0.05$$ so accept $$H_0$$, the evidence suggests their is no difference in the average effectiveness of the aerosols.

