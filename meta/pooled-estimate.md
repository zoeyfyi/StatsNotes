### Pooled estimate for variance
Say you have two random variables with equal (but unknown) variance, a better estimate of the variance would be to combine the two estimators for variance from each distribution.

To derive the pooled estimate we first take the indivdual estimators

$$
s_x^2 = \frac{\sum{(x - \bar{x}_x)^2}}{n_x-1}
$$
and
$$
s_y^2 = \frac{\sum{(x - \bar{x}_y)^2}}{n_y-1}
$$

adding the sum of squares
$$
\sum{(x - \bar{x}_x)^2} + \sum{(x - \bar{x}_y)^2} = s_x^2(n_x-1) + s_y^2(n_y-1)
$$
and if we treat the combined samples as a single sample
$$
\begin{align}
\frac{\sum{(x - \bar{x}_x)^2} + \sum{(x - \bar{x}_y)^2}}{(n_x-1) + (n_y-1)} &= \frac{s_x^2(n_x-1) + s_y^2(n_y-1)}{(n_x-1) + (n_y-1)}\\
s^2_p &= \frac{s_x^2(n_x-1) + s_y^2(n_y-1)}{n_x + n_y - 2}
\end{align}
$$

