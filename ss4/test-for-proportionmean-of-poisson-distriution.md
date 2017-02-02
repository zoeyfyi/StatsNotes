## Hypothesis test with the possion distribution
A hypothesis test using the possion distribution is very simular previous hypothesis tests.

#### Process
1. Write down hypothesis.
2. Find the probability that the positon distribution with the parameter of the null hypothesis is greater than the sample.
3. Compare against the significance level, if it is less than the significance level, reject $$H_0$$.

#### Example
Last year their was an average of 8 complaint emails per week. On the first week of next year 16 complaints were received. Test at the 5% level, weather the mean number of complaints has increased.

###### Hypothesis
$$
H_0: \mu = 8 \\ 
H_1: \mu > 8
$$

###### Test statistic
$$
X \sim Po(8)\\
$$$$
\begin{align}
P(X \geq 16) &= 1 - P(X \leq 15) \\
&= 0.00823\\
\end{align} 
$$

###### Conclusion
$$0.00823 < 0.05$$ so reject $$H_0$$, the is no evidence to support the mean number of emails has increased.