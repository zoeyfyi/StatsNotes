## F-distribution
Suppose we take $$n_x$$ observations from a $$N(\mu_x, \sigma_x^2)$$ distribution and a independent sample of size $$n_y$$ from a $$N(\mu_y, \sigma_y^2)$$ distribution.

As with earlier, we know $$\frac{(n_x-1)s_x^2}{\sigma_x^2} \sim \chi^2_{n_x-1}$$ and $$\frac{(n_y-1)s_y^2}{\sigma_y^2} \sim \chi^2_{n_y-1}$$

So if follows that:
$$
\frac{\frac{s_x^2}{\sigma_x^2}}{\frac{s_y^2}{\sigma_y^2}} \sim \frac{\frac{\chi^2_{n_x-1}}{(n_x-1)}}{\frac{\chi^2_{n_y-1}}{(n_y-1)}}
$$
and 
$$
\frac{\frac{s_y^2}{\sigma_y^2}}{\frac{s_x^2}{\sigma_x^2}} \sim \frac{\frac{\chi^2_{n_y-1}}{(n_y-1)}}{\frac{\chi^2_{n_x-1}}{(n_x-1)}}
$$

This is the F-distribution and it has two parameters $$(n_x - 1)$$ and $$(n_y - 1)$$ usually written as $$F_{v1, v2}$$ where $$v1$$ and $$v2$$ correspond to the two parameters.

If the parameters are the other way round (y on top) we can convert them with: 
$$
F_{v2, v1} = \frac{1}{F_{v1, v2}}
$$

#### Example
$$X \sim F_{8, 10}$$, find $$P(\frac{1}{5.81} < X < 5.06)$$

$$
\begin{align}
P(\frac{1}{5.81} < X < 5.06) &= P(X < 5.06) - P(X < \frac{1}{5.81})\\
                             &= 0.99 - P(F_{10, 8} > 5.81)\\
                             &= 0.99 - (1 - P(F_{10, 8} < 5.81))\\
                             &= 0.99 - (1 - 0.99)\\
                             &= 0.98
\end{align}
$$

Note: to find the values on the table, look at each F-distribution table and look for the value closest to the right hand side value, in this case $$5.057$$ (which rounds to $$5.06$$) was found on the $$p = 0.99$$ table.