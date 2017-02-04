## Confidence interval for Poisson
For an observation from a Poisson distribution we know that we can approximate it to a normal distribution, given $$\lambda$$ is large enough. Given this, it can be show that the confidence interval for a single observation would be: 
$$
\lambda \pm \frac{z}{\sqrt{\lambda}}
$$
where $$z$$ is the Z-value for the significance level.

#### Example
Voters arrived between 6pm and 9pm. In the first hour 51 voters showed up. Assuing the arrivals can be moddled by a poisson distribution, calculate a 95% confidence interval
$$
51 \pm \frac{1.96}{\sqrt{51}} = (37.0, 65.0)
$$