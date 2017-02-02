## Combination of random variables

Using the following rules from SS2, given that $$X$$ and $$Y$$ are random variables:
$$
\operatorname{E}(aX \pm bY) = a\operatorname{E}(X) \pm b\operatorname{E}(Y)
$$
and the following for $$X$$ and $$Y$$ are _independent_ random variables
$$
\operatorname{Var}(aX \pm bY) = a^2\operatorname{Var}(X) + b^2\operatorname{Var}(Y)
$$

It follows that, if $$X$$ and $$Y$$ are normally distributed:
$$
\begin{align}
aX \pm bY &\sim \operatorname{N}(E(aX \pm bX), Var(aX \pm bX))\\
&\sim \operatorname{N}(a\operatorname{E}(X) \pm b\operatorname{E}(Y), a^2\operatorname{Var}(X) + b^2\operatorname{Var}(Y))\\
&\sim N(a\mu_X \pm b\mu_Y, a^2\sigma_X^2 + b^2\sigma_Y^2)

\end{align}
$$