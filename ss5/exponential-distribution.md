# Exponential distribution
The exponential distribution is the interval between the successive events of a Poisson distribution. Its density function is as follows:
$$
f(x)
\begin{cases}
\lambda e^{-\lambda x} & x > 0\\
0 & \text{otherwise}\\
\end{cases}
$$
where lambda is the parameter of the exponential distribution.

If you integrate between $$0$$ and $$x$$, you can find the cumulative distribution function:
$$
\begin{align}
\int^{x}_{0}{\lambda e^{-\lambda x}}
&= \left[-e^{-\lambda x}\right]^x_0\\
&= \left[-e^{-\lambda x} -- e^{0}\right]^x_0\\
&= \left[-e^{-\lambda x} + 1\right]\\
&= 1 - e^{-\lambda x}
\end{align}
$$

#### Example
The number of cars passing a point per minute is 0.8. Find the probability that the interval between two cars is longer than 2 minuets.

###### Define the densitiy function
$$
F(x) = 1 - e^{-0.8x}
$$

###### Find the probabilty
$$
\begin{align}
F(\infty) - F(2) 
&= (1 - e^{-0.8 \times \infty}) - (1 - e^{-0.8 \times 2})\\
&= (1 - 0) - (1 - e^{-1.6})\\
&= 0.202
\end{align}
$$