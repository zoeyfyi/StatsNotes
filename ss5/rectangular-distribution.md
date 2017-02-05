# Rectangle distribution
The rectangular distribution is a random variable that takes any value in given range within an interval, the pdf of which is:
$$
f(x) = 
\begin{cases}
\frac{1}{b - a} & a \leq x \leq b\\
0 & \text{otherwise}
\end{cases}
$$
The mean can be found by finding the expectation of $$X$$:
$$
\begin{align}
E(X) = &= \int^{\infty}_{-\infty}{x \times f(x)}\\
&= \int^{b}_{a}{x \times \frac{1}{b - a}}\\
&= \frac{1}{b - a} \times \int^{b}_{a}{x}\\
&= \frac{1}{b - a} \times \left[\frac{x^2}{2}\right]^{b}_{a}\\
&= \frac{1}{b - a} \times \left[\frac{b^2}{2} - \frac{a^2}{2}\right]\\
&= \frac{1}{b - a} \times \frac{b^2 - a^2}{2}\\
&= \frac{b^2 - a^2}{2(b - a)}\\
&= \frac{(b - a)(b + a)}{2(b - a)}\\
&= \frac{b + a}{2}\\
\end{align}
$$
Likewise the varience can be found by finding the varience of $$X$$:
$$
\begin{align}
E(X^2)
&=\int^{b}_{a}{x^2 \times f(x)}\\
&= \int^{b}_{a}{x^2 \times \frac{1}{b - a}}\\
&= \frac{1}{b - a} \times \int^{b}_{a}{x^2}\\
&= \frac{1}{b - a} \times \left[\frac{x^3}{3}\right]^{b}_{a}\\
&= \frac{1}{b - a} \times \left[\frac{b^3}{3} - \frac{a^3}{3}\right]\\
&= \frac{1}{b - a} \times \frac{b^3 - a^3}{3}\\
&= \frac{b^3 - a^3}{3(b - a)}\\
&= \frac{b^3 - a^3}{3(b - a)}\\
&= \frac{(b - a)(b^2 + ab + a^2)}{3(b - a)}\\
&= \frac{b^2 + ab + a^2}{3}\\
\end{align}
$$
$$
\begin{align}
Var(X) 
&= E(X^2) - E(X)^2\\
&= \frac{b^2 + ab + a^2}{3} - \left(\frac{b + a}{2}\right)^2\\
&= \frac{b^2 + ab + a^2}{3} - \frac{b^2 + 2ab + a^2}{4}\\
&= \frac{4b^2 + 4ab + 4a^2}{12} - \frac{3b^2 + 6ab + 3a^2}{12}\\
&= \frac{4b^2 + 4ab + 4a^2 - 3b^2 - 6ab - 3a^2}{12}\\
&= \frac{b^2 -2ab + a^2}{12}\\
&= \frac{(b - a)^2}{12}\\
\end{align}
$$
And the cumulative distribution function can be found by integrating $$f(x)$$ between x and the lower bound. For example let $$f(x)$$ be defined as:
$$
f(x) = 
\begin{cases}
\frac{1}{29} & -7 \leq x \leq 22\\
0 & \text{otherwise}
\end{cases}
$$

The cumulative distribution function would be:
$$
\begin{align}
F(x) 
&= \int^{x}_{-\infty}{f(x)}\\
&= \int^{x}_{-7}{\frac{1}{29}}\\
&= \left[\frac{x}{29}\right]^{x}_{-7}\\
&= \left[\frac{x}{29} - \frac{-7}{29}\right]\\
&= \frac{x + 7}{29}\\
\end{align}
$$