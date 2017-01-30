## Wilcoxon signed-rank test

Wilcoxon signed-rank test is also a distribution free test, for when we can use a z or t test. Its similar to the sign test except we rank the differences \(ignoring the signs, smallest first\), then add the ranks with the same signs.

#### Example

Test if the distributions of mock and a-level results are the same.

Hypothesis

$$H\_0$$: Population median difference = 0  
$H\_1$: Population median difference &gt; 0

| Candidate | Mock | A level | Difference | Rank | $+$ Rank | $-$ Rank |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 40 | 45 | 5 | 7 | 7 |  |
| 2 | 65 | 68 | 3 | 4 | 4 |  |
| 3 | 53 | 47 | -6 | 9.5 |  | 9.5 |
| 4 | 79 | 75 | -4 | 6 |  | 6 |
| 5 | 87 | 88 | 1 | 1 | 1 |  |
| 6 | 87 | 88 | 18 | 13 | 13 |  |
| 7 | 80 | 77 | -3 | 4 |  | 4 |
| 8 | 63 | 69 | 6 | 9.5 | 9.5 |  |
| 9 | 51 | 60 | 9 | 12 | 12 |  |
| 10 | 82 | 88 | 6 | 9.5 | 9.5 |  |
| 11 | 27 | 30 | 3 | 4 | 4 |  |
| 12 | 71 | 73 | 2 | 2 | 2 |  |
| 13 | 29 | 35 | 6 | 9.5 | 9.5 |  |


$$
T_+ = \sum{+ \text{Rank}} = 71.5\\
T_- = \sum{- \text{Rank}} = 19.5\\
T = 19.5
$$


Critical value $ = 21$

$19.5 &lt; 21$ so reject $H\_0$, evidence students did better in their A Level.

