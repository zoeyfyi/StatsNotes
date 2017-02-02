## Approximating a binomial distribution using the poison distribution
When $$np < 10$$, $$n \geq 20$$ and $$p \leq 0.05$$ the binomial distribution can be approximated by the Poisson distribution.

#### Example
Based upon past experience, 1% of the telephone bills mailed to households are incorrect. If a sample of 20 bills is selected, find the probability that at least one bill will be incorrect.

###### Find the mean and varience
$$
\begin{align}
\mu &= \lambda\\
&= np\\
&= 20 * 0.01\\
&= 0.2
\end{align}
$$
$$
\begin{align}
\sigma^2 &= \lambda\\
&= np\\
&= 0.2\\
\end{align}
$$

###### Approximate using poisson
$$
\begin{align}
X &\sim Po(0.2)\\
P(X \geq 1) &= P(X \leq 0)\\
&= P(X = 0)\\
&= \frac{e^{-0.2} \times \lambda^0}{0!}\\
&= 0.819
\end{align}
$$