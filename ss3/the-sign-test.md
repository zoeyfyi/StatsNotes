# Sign test

The sign test is a **distribution free** test since it doesn't require the data to follow a particular distribution. Its also very simple, just find the sign of the difference ignoring any pairs that are equal. Then use $P\(X &lt; min\(a, b\)\| X \sim B\(n, \frac{1}{2}\)$ where $a$ and $b$ are the number of each sign and n is number of all valid signs \(not Nan\).

\#\#\#\# Example

Data is collected about driver and passenger injury's. Test at 5% significance weather these are related.

Hypothesis

$H\_0$: Driver injury $=$ Passenger injury

$H\_1$: Driver injury $\ne$ Passenger injury

Signs

\| $ $ \| Driver \| Passenger \| sign \|

\| --- \| --- \| --- \| --- \|

\| 1 \| 42 \| 35 \| + \|

\| 2 \| 42 \| 35 \| + \|

\| 3 \| 34 \| 45 \| - \|

\| 4 \| 34 \| 45 \| - \|

\| 5 \| 45 \| 45 \| Nan \|

\| 6 \| 40 \| 42 \| - \|

\| 7 \| 42 \| 46 \| - \|

\| 8 \| 43 \| 58 \| - \|

\| 9 \| 45 \| 43 \| + \|

\| 10 \| 36 \| 37 \| - \|

\| 11 \| 36 \| 37 \| - \|

\| 12 \| 43 \| 58 \| - \|

\| 13 \| 40 \| 42 \| - \|

\| 14 \| 43 \| 58 \| - \|

\| 15 \| 37 \| 41 \| - \|

\| 16 \| 37 \| 41 \| - \|

\| 17 \| 44 \| 57 \| - \|

\| 18 \| 42 \| 42 \| Nan \|

Test statistic


$$
X \sim B\(18-2, \frac{1}{2}\)\\

\begin{align}

b &= P\(X &lt; min\(3, 13\)\)\\

   &= P\(X &lt; 3\)\\

   &= P\(X \leq 2\)\\

   &= 0.0021

\end{align}
$$


$0.0021 &lt; 0.05$ so reject $H\_0$, their is evidence of a difference in the distributions.

