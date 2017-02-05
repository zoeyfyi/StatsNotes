# Testing a binomial distribution

Conditions for a binomial distribution:

* Fixed number of trials
* Trials are independent
* Only success and faliures
* Probabilty of success is constant

You can estimate $$p$$ with:
$$
p = \frac{\text{total number of successes}}{\text{number of trials} \times \text{number of observations}}
$$


So if $$p$$ is estimated $$v = \text{number of cells} - 2$$, else $$v = \text{number of cells} - 1$$

#### Example

The following table shows observed and expected values for a binomial model.

| $$O_i$$ | 17 | 28 | 32 | 15 | 5 | 3 |
| --- | --- | --- | --- | --- | --- | --- |
| $$E_i$$ | 19.69 | 34.74 | 27.58 | 12.98 | 4.01 | 0.99 |

Test at a 5% significance level if the distribution fits a binomial model.

###### Test statistic
Since $$E_i \lt 5$$ in the last to columns, we must combine them to work out $$\chi^2$$:

| $$O\_i$$ | 17 | 28 | 32 | 15 | 9 |
| --- | --- | --- | --- | --- | --- |
| $$E_i$$ | 19.69 | 34.74 | 27.58 | 12.98 | 5 |
| $$\frac{(O_i - E_i)^2}{E_i}$$ | 0.368 | 1.31 | 0.708 | 0.314 | 1.8 |

$$
\sum{\frac{(O_i - E_i)^2}{E_i}} = 4.50
$$

###### Critical value
$$
\begin{align}
v &= 5 - 1 \\
   &= 4\\
\end{align}
$$

$$
\chi^2_4(5\%) = 9.49...
$$


###### Conclusion
Since $$4.50 \lt 9.49$$ accept $$H_0$$ and reject $$H_1$$, their is evidence to suggest the binomial model is a god fit.

