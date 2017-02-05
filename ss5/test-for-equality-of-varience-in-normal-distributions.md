# Test for mean equality
Sometimes we are interested in the difference between two independent populations.

To test two distributions we can use the rules for combining distributions to derive this test statistic for two normal distributions $$X$$ and $$Y$$:
$$
Z = \frac{\bar{X} - \bar{Y} - (\mu_x - \mu_y)}
{\sqrt{\frac{\sigma_x^2}{n_x}+\frac{\sigma_y^2}{n_y}}}
$$

If $$n_x$$ and $$n_y$$ are larger enough, this statistic can be used for distributions where $$X$$ and $$Y$$ are not normal.

#### Example
A study weighs children in area $$A$$ and area $$B$$. The results are as follows:

| | $$n$$ | $$\bar{x}$$ | $$s$$ |
| --- | --- | --- | --- |
| $$A$$ | 220 | 37.8 | 3.6 |
| $$B$$ | 180 | 38.6 | 4.1 |

Test at a 5% level of significance the difference in the mean weight of two children.	

###### Hypothesis
$$
H_0: \mu_A = \mu_B\\
H_1: \mu_A \neq \mu_B\\
$$

###### Test statistic
$$
\begin{align}
z &= \frac{\bar{x}_A - \bar{x}_B - (\mu_A - \mu_B)}{\sqrt{\frac{\sigma_A^2}{n_A}+\frac{\sigma_B^2}{n_B}}}\\
  &= \frac{37.6 - 38.6}{\sqrt{\frac{3.6^2}{220}+\frac{4.1^2}{180}}}\\
  &= -2.56243...\\
  &= -2.56\\
\end{align}
$$

###### Critical value
$$z = \pm1.96$$


###### Conclusion
Since $$-2.56 < -1.96$$, the result is significant so reject $$H_0$$, their is evidence that the mean weight is different in the two areas.

# Two sample t-test
If the sample size is small we can use the z-test so if we assume that the populations have the same variance and are normally distributed we can use a similar method called the two sample t-test. 

#### Example
Conduct a two sample t-test at a 10% significance level with the following data:

| $$X$$ | $$40$$ | $$37$$ | $$45$$ | $$34$$ | $$30$$ | $$41$$ | $$42$$ | $$43$$ | $$36$$ |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| $$Y$$ | $$38$$ | $$43$$ | $$36$$ | $$45$$ | $$35$$ | $$44$$ | $$41$$ |


###### Hypothesis
$$
H_0: \mu_x = \mu_y \\
H_1: \mu_x \ne \mu_y
$$

###### Test statistic
$$
n_x = 9\\
\bar{x} = 38.667\\
s_x^2 = 23 
$$
$$
n_y = 7\\
\bar{y} = 40.286\\
s_y^2 = 15.905 
$$

$$
s_p^2 = \frac{(9 - 1) \times 23 + (7 - 1) \times 15.905}{9 + 7 - 2} = 19.959\\
$$
$$
t = \frac{38.667 - 40.286}{\sqrt{19.959 \times (\frac{1}{9} + \frac{1}{7})}} = -0.719\\
$$

###### Critical value
$$
t_{9 + 7 - 2}(0.95) = t_{14}(0.95) = 1.761
$$

###### Conclusion
$$-1.761 < -0.719 < 1.761$$ so accept $$H_0$$, evidence suggests their is no difference in the means of the two groups.