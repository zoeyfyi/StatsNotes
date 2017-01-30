## Goodness of fit tests

### Degrees of freedom

Degrees of freedom is a measure of the data _not_ used up. Every time a statistic is calculated or constraint put in place, a degree of freedom is used. For the purpose of testing the fit of a distribution the total frequency of the model must equal the observed frequency. This is an example of a constraint so we lose a degree of freedom. 

### Testing a discrete uniform distribution

Conditions for a discrete uniform distribution:

- Random variable $$X$$ defined over a set of values
- Each value is equally likely.

Since the its uniform, their are no parameters to estimate so: $v = \text{number of cells} - 1$

#### Example
The following table shows some observed values:

| $$x$$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| $$O_i$$ | 12 | 24 | 18 | 20 | 25 | 17 | 21 | 23 |
Conduct a goodness of fit test for weather its a discrete uniform distribution.

$$H_0$$: The observations _can_ be modeled by a discrete uniform distribution
$$H_1$$: The observations _cannot_ be modeled by a discrete uniform distribution
 
Expected frequency:
$$
\begin{align}
E_i &= \frac{\sum{O_i}}{8} \\
    &= \frac{160}{8}  \\
    &= 20
\end{align}
$$

Working out the test statistic $\chi^2$:

| $$x$$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| $$O_i$$ | 12 | 24 | 18 | 20 | 25 | 17 | 21 | 23 |
| $$E_i$$ | 20 | 20 | 20 | 20 | 20 | 20 | 20 | 20 |
| $$\frac{(O_i - E_i)^2}{E_i}$$ | 3.2 | 0.8 | 0.2 | 0 | 1.25 | 0.45 | 0.05 | 0.45 |



$$
\sum{\frac{(O_i - E_i)^2}{E_i}} = 6.4
$$

Critical value:

$$
\begin{align}
v &= 8 - 1 \\
   &= 7\\
\end{align}
$$

$$
\chi^2_7(5\%) = 14.067...
$$

Conclusion:

$$6.4 < 14.067...$$ so accept $$H_0$$ and reject $$H_1$$, their is evidence that the observations fits a discrete uniform distribution  

### Testing a binomial distribution

Conditions for a binomial distribution:

- Fixed number of trials
- Trials are independent
- Only success and faliures
- Probabilty of success is constant

You can estimate $p$ with:

$$p = \frac{\text{total number of successes}}{\text{number of trials} \times \text{number of observations}}$$

So if $p$ is estimated: $v = \text{number of cells} - 2$
Else: $v = \text{number of cells} - 1$

#### Example
The following table shows observed and expected values for a binomial model.
| $O_i$ | 17 | 28 | 32 | 15 | 5 | 3 |
| --- | --- | --- | --- | --- | --- | --- |
| $E_i$ | 19.69 | 34.74 | 27.58 | 12.98 | 4.01 | 0.99 |

##### a. Test at a 5% significance level
Since $E_i < 5$ in the last to columns, we must combine them to work out $\chi^2$:
| $O_i$ | 17 | 28 | 32 | 15 | 9 |
| --- | --- | --- | --- | --- | --- |
| $E_i$ | 19.69 | 34.74 | 27.58 | 12.98 | 5 |
| $\frac{(O_i - E_i)^2}{E_i}$ | 0.368 | 1.31 | 0.708 | 0.314 | 1.8 |

$$\sum{\frac{(O_i - E_i)^2}{E_i}} = 4.50$$


Critical value:
$$
\begin{align}
v &= 5 - 1 \\
   &= 4\\
\end{align}
$$

$$
\chi^2_4(5\%) = 9.49...
$$

Conclusion:

Since $4.50 < 9.49$ accept $H_0$ and reject $H_1$, their is evidence to suggest the binomial model is a god fit.

### Testing a Poisson distribution

Conditions for a Poisson distribution:

- Events occor independently
- Events occor singly and randomly in space or time
- Events occor at a constant rate
- Mean and variance are equal

You can estimate $\lambda$ with:
$$\lambda = \frac{\sum{r \times f_r}}{N}$$

So if $\lambda$ is estimated: $v = \text{number of cells} - 2$
Else: $v = \text{number of cells} - 1$

#### Example
Conduct a goodness of fit test between the observed values below and the distribution $Po(2)$
| $x$ | 0 | 1 | 2 | 3 | 4 | \>5 |
| --- | --- | --- | --- | --- | --- | --- |
| $O_i$ | 12 | 23 | 24 | 24 | 12 | 5 | 0 |

Work out $\chi^2$ using expected values from the $Po(2)$ distribution:
| $x$ | 0 | 1 | 2 | 3 | 4 | 5 | \>5 |
| --- | --- | --- | --- | --- | --- | --- |
| $O_i$ | 12 | 23 | 24 | 24 | 12 | 5 | 0 |
| $E_i$ | 13.53 | 27.07 | 27.07 | 18.04 | 9.02 | 3.61 | 1.66 | 

Since $E_i < 5$ we combine the last 2 columns:
 
| $x$ | 0 | 1 | 2 | 3 | 4 | \>4 |
| --- | --- | --- | --- | --- | --- |
| $O_i$ | 12 | 23 | 24 | 24 | 12 | 5 |
| $E_i$ | 13.53 | 27.07 | 27.07 | 18.04 | 9.02 | 5.27 | 
| $\frac{(O_i - E_i)^2}{E_i}$ | 0.173 | 0.612 | 0.348 | 1.969 | 0.985 | 0.0138 |

$$\sum{\frac{(O_i - E_i)^2}{E_i}} = 4.10$$

Critical value:
$$
\begin{align}
v &= 6 - 1 \\
   &= 5\\
\end{align}
$$

$$
\chi^2_6(5\%) = 11.07...
$$

Since $4.10 < 11.07$ accept $H_0$ and reject $H_1$, the distribution $Po(2)$ is a good model.