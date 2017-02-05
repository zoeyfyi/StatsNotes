# Testing a discrete uniform distribution

Conditions for a discrete uniform distribution:

* Random variable $$X$$ defined over a set of values
* Each value is equally likely.

Since the its uniform, their are no parameters to estimate so: $$v = \text{number of cells} - 1$$

#### Example

The following table shows some observed values:

| $$x$$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| $$O_i$$ | 12 | 24 | 18 | 20 | 25 | 17 | 21 | 23 |

Conduct a goodness of fit test for weather its a discrete uniform distribution.

###### Hypothesis
$$H_0$$: The observations _can_ be modeled by a discrete uniform distribution
$$H_1$$: The observations _cannot_ be modeled by a discrete uniform distribution

###### Expected frequency
$$
\begin{align}
E_i &= \frac{\sum{O_i}}{8} \\
&= \frac{160}{8} \\
&= 20
\end{align}
$$

###### Test statisitic
| $$x$$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| $$O_i$$ | 12 | 24 | 18 | 20 | 25 | 17 | 21 | 23 |
| $$E_i$$ | 20 | 20 | 20 | 20 | 20 | 20 | 20 | 20 |
| $$\frac{(O_i - E_i)^2}{E_i}$$ | 3.2 | 0.8 | 0.2 | 0 | 1.25 | 0.45 | 0.05 | 0.45 |

$$
\sum{\frac{(O_i - E_i)^2}{E_i}} = 6.4
$$

###### Critical value
$$
\begin{align}
v &= 8 - 1 \\
&= 7\\
\end{align}
$$
$$
\chi^2_7(5\%) = 14.067...
$$

###### Conclusion
$$6.4 < 14.067...$$ so accept $$H_0$$ and reject $$H_1$$, their is evidence that the observations fits a discrete uniform distribution