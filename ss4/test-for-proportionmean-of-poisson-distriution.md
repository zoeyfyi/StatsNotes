## Hypothesis test with the possion distribution
A hypothesis test using the possion distribution is very simular previous hypothesis tests/

#### Process
1. Write down hypothesis 
2. Find the expectation $$\lambda n$$, then us the tables to find the test statistic
3. Compare against the significance level, if it is greater than the significance level, reject $$H_0$$

#### Example
An existing make of car is known to break down on average one and a half times per year. A new model is introduced and the manufacturer claims that this model is less likely to break down. Ten randomly selected cars break down a total of eight times within the first year. Test the manufacturer's claim at a 55% significance level.

###### Hypothesis
$$
H_0: \lambda = 1.5\text{,} \\ 
H_1: \lambda < 1.5. 
$$

###### Test statistic
$$
\begin{align}
X \sim Po(1.5)\\
1.5 \times 10 &= 15\\
P(X < 15) &= 0.0374\\
\end{align} 
$$

## Conclusion
$$0.0374 < 0.05$$ so accept $$H_0$$, the is no evidence to support the average amount of cars breaking down has decreased.