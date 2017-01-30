## Spearman's rank correlation coefficient
The product moment correlation coefficient works when you have something to measure. Suppose you had an order, for example an order of preference in different blends of tea, this is when we use Spearman's rank correlation coefficient.

To calculate the Spearman's rank correlation coefficient we use the following:
$$
r_s = 1 - \frac{6\sum{d^2}}{n(n^2-1)}
$$
Where $$d_i$$ is the difference between rank $$x_i$$ and rank $$y_i$$ and $$n$$, the number of pairs.

#### Example
Two judges judge a competition, comment on how well they agree

| Competitor | A | B | C | D | E | F | G | H | I | J |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **Judge 1** | 7.8 | 6.6 | 7.3 | 7.4 | 8.4 | 6.5 | 8.9 | 8.5 | 6.7 | 7.7 |
| **Judge 2** | 8.1 | 6.8 | 8.2 | 7.5 | 8.0 | 6.7 | 8.5 | 8.3 | 6.6 | 7.8 |

Rank the scores

| Competitor | A | B | C | D | E | F | G | H | I | J |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| $x_i$ | 4 | 9 | 7 | 6 | 3 | 10 | 1 | 2 | 8 | 5 |
| $y_i$ | 4 | 8 | 3 | 7 | 5 | 9 | 1 | 2 | 10 | 6 |

Find the difference

| Competitor | A | B | C | D | E | F | G | H | I | J |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| $d_i$ | 0 | 1 | 4 | -1 | -2 | 1 | 0 | 0 | -2 | -1 |

Find the coefficient
$$
\begin{align}
r_s &= 1 - \frac{6 \times (0^2 + 2^2 +4^2 + ...)}{10(10^2-1)}\\
     &= 1 - \frac{168}{990}\\
     &= 0.830
\end{align}
$$

Fairly strong correlation between the judges, suggesting judges have similar criteria and standards.