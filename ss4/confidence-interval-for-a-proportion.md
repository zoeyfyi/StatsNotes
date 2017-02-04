# Confidence interval for a proportion
Given an estimator for sample proportion $$\hat{p}$$ we can caluate the confidence interval for the population proportion using:
$$
\hat{p} \pm z \times \left(\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}\right)
$$
where $$z$$ is the Z-value for the significance level

#### Example
Marzena buys Simsons matches. Of a random sample of 85 such matches, 27 broke when he struck them. Calculate an approximate 95% confidence interval for the proportion of Simsons matches which will break when Marzena strikes them.
$$
\hat{p} = \frac{27}{85} = 0.31765\\
$$$$
0.31765 \pm 1.96 \times \sqrt{\frac{0.31765(1-0.31765)}{85}}\\
0.31765 \pm 0.09897\\
(0.219, 0.417)
$$