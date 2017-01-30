## Testing correlation coefficient is zero
We may be interested in conducting a test to show their is no correlation between two random variables. First we find the correlation coefficient, then get the critical value from the appropriate table.

#### Example
Test to see if their is no correlation between English and maths marks at the 5% significance level.

| Student | A | B | C | D | E | F | G | H |
| --- |
| **English** | 25 | 18 | 32 | 27 | 21 | 35 | 28 | 30 |
| **Mathematics** | 16 | 11 | 20 | 17 | 15 | 26 | 32 | 20 |

Calculate the product moment correlation coefficient
$$
\begin{align}
\sum{x_i} &= 216\\
\sum{y_i} &= 157\\
\sum{x_i^2} &= 6052\\
\sum{y_i^2} &= 3391\\
\sum{x_i y_i} &= 4418\\
S_{xx} &= 6052 - \frac{216^2}{8} = 220\\
S_{yy} &= 3391 - \frac{157^2}{8} = 309.875\\
S_{xy} &= 4418 - \frac{216 \times 157}{8} = 179\\
r &= \frac{179}{\sqrt{220 \times 309.875}} = 0.686
\end{align}
$$

Hypothesis
$$
H_0: \rho = 0\\
H_1: \rho \ne 0
$$ 

Critical value from tables
$$
\pm0.7067
$$

$$-0.7067 < 0.686 < 0.7067$$ so value is not in critical region, accept $H_0$, evidence to suggest product moment correlation coefficient is zero.