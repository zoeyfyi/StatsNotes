## Approximating a binomial distribution using the normal distribution
When the sample size becomes large its difficult to calculate the probabilty for a binomial distribution, so we can approximate it using the normal distribution. For the approximation to be valid $$n$$ must be large ($$n > 20$$) and $$p$$ must not be to close to zero or one ($$0.05 < p < 0.95$$)

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

