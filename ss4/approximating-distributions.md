## Continuity corrections
When we go from a discrete distribution to a continuous distribution, we must account for the discrete nature of the problem in are calculations.

For example, let $$X$$ be the number of heads after 10 flips of a coin, find the $$P(X = 4)$$. If we approximate the value with a continuose distribution we must find the area under the curve between $$0.35$$ and $$0.45$$ since these are the lower and upper limits of $$4$$.

## Aproximating a binomial distribution using the normal distribution
When the sample size becomes large its difficult to calculate the probabilty for a binomial distribution, so we can approximate it using the normal distribution (given the sample size is large).

#### Example
Suppose that a sample of $$n = 1600$$ tires of the same type are obtained at random from an ongoing production process in which 8% of all such tires produced are defective. What is the probability that in such a sample 150 or fewer tires will be defective?

###### Find mean and varience 
$$
\begin{align}
\mu &= np\\
&= 1600 \times 0.08 = 128\\
\end{align}
$$
$$
\begin{align}
\sigma^2 &= np(1-p)\\
&= 1600 \times 0.08 \times (1 - 0.08)\\
&= 117.76\\
\end{align}
$$

###### Aproximate using normal distribution
$$
\begin{align}
Z &= \frac{X - \mu}{\sigma} \\
&= \frac{150.5 - 128}{\sqrt{117.76}}\\
&= 2.073\\
P(Z < 2.073) &= 0.981
\end{align}
$$

## Aproximate a poission distribution using the normal distribution
When $$\lambda$$ is large the poission distribution can also be approximated using the normal distribution.

#### Example
Suppose that at a certain automobile plant the average number of work stoppages per day due to equipment problems during the production process is 12.0. What is the approximate probability of having 15 or fewer work stoppages due to equipment problems on any given day?

###### Find the mean and varience
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


## Aproximating a binomial distribution using the poison distribution
When $$np < 10$$, $$n \geq 20$$ and $$p \leq 0.05$$ the binomial distribution can be approximated by the poision distribution.

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






