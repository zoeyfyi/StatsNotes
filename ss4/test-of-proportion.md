## Test of proportion
The test of proportion test the population parameter $$p$$ (proportion) in a given sample, to access whether the sample represents the true proportion of the entire population.

#### Process
1. Write the hypothesis
2. Create a binomial distribution with parameters $$n$$ and $$p$$ where n is the sample size and $$p$$ is the null hypothesis propotion.
3. Find the probability the binomial distribution is less than the amount success in the sample
4. Compare the probability, if it is less that the significance level reject $$H_0$$

#### Example
40% of passengers rated an airliners food bad. The airliner claimed to improve the food and re ran the survey, after which 6 out of 20 passengers said the food was bad. Test at a 5% significance level if the rating the meal bad had reduced.

###### Hypothesis
$$
H_0: p = 0.4\\
H_1: p < 0.4
$$

###### Test statistic
$$
X \sim B(20, 0.4)
$$$$
P(X \leq 6) = 0.250
$$

###### Conclusion
$$0.250 > 0.05$$ so accept $$H_0$$, no evidence that the proportion of passengers rating the meal bad had reduced.

#### Example (with approximation)
Past experience suggests that 40% of households donate to charity. In a sample 1240 households where asked if they donate, 476 had. Test the hypothesis that the number of households that donate is 40%.

###### Hypothesis
$$
H_0: p = 0.4\\
H_1: p \ne 0.4
$$

###### Test statisitc
$$
X \sim B(1240, 0.4)\\
\mu = 1240 \times 0.4 = 496\\
\sigma^2 = 1240 \times 0.4(1 - 0.4)\\
X \approx N(496, 297.6)
$$$$
z = \frac{476.5 - 496}{\sqrt{297.6}} = -1.13
$$

###### Critical value
$$
\text{cv} = \pm 1.96
$$

###### Conclusion
$$-1.96 < -1.13 < 1.96$$ so accept $$H_0$$, evidence support claim that 40% of households make a donation.














