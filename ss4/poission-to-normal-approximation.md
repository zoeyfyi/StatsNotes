## Approximate a Poisson distribution using the normal distribution
When $$\lambda$$ is large ($$\lambda > 20$$) the Poisson distribution can also be approximated using the normal distribution.

#### Example
Suppose that at a certain automobile plant the average number of work stoppages per day due to equipment problems during the production process is 12.0. What is the approximate probability of having 15 or fewer work stoppages due to equipment problems on any given day?

###### Find the mean and variance
$$
\begin{align}
\mu &= \lambda\\
&= 12\\
\end{align}
$$
$$
\begin{align}
\sigma^2 &= \lambda\\
&= 12\\
\end{align}
$$

###### Aproximate using normal distribution
$$
\begin{align}
Z &= \frac{X - \mu}{\sigma} \\
&=\frac{15.5 - 12}{\sqrt{12}}\\
&= 1.010\\
P(Z < 1.010) &= 0.844\\
\end{align}
$$