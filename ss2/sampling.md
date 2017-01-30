## Sampling

> Sampling frame: A list of every single member which could be included in a sample

### Census
Observes/measures every member of the population e.g. taking the height of all students in a certain sixth form.

**Advantages**

 - Completely accurate results

**Disadvantages**

- Time consuming and expensive
- Doesn't work when measurement destroys sample
- Difficult to process large amount of data

### Simple Random Sample
Simple random sample is sampling without replacement where every member of the population has an equal chance of being selected. 

**Advantages**

- Cheap and simple
- Standard formula work for analysis
- Each member included only once
- Random
- Known chance of element selection

**Disadvantages**

- Not suitable for large populations
- Sampling frame required 

Their are two types of simple random sample:

#### Random Number Sampling
Each element in the sampling frame is assigned a number then, using a random number generator, select a random element and add it to the sample until the sample size is reached, ignoring any duplicate numbers or numbers larger than the population.

#### Lottery Sampling
Each member in the population is written down on a ticket and put into a container. Tickets are then drawn one at a time (without replacement) until the sample size is met.

### Systematic sampling
Take every $$k^{th}$$ element from an ordered list of samples where: 

$$
k = \frac{\text{population size} (N)}{\text{sample size} (n)}
$$

So that the first element of the population is not always selected the first item is selected randomly e.g. start at the $$3^{rd}$$ element and pick every $$4^{th}$$ element.

Its easy to introduce bias with certain data e.g. if you had 100 years of rainfall data and $$k$$ was 12 month, you would be selecting the same month.

**Advantages**

- Simple to use
- Sutible for large samples

**Disadvantages**

- Only random if ordered list is truly random
- Can introduce bias

### Stratified sampling
The populating is divided into mutually exclusive groups called strata. Within each strata a simple random sample is used such that each stratum is representative of the overall population.

$$
\text{stratum sample size} = \frac{\text{stratum size}}{\text{population size}} * \text{sample size}
$$

**Advantages**

- Suitable for large samples.
- More accurate estimates when clear strata are present.
- Reflects population structure.

**Disadvantages**

- Within the strata, same disadvantages as a simple random sample.
- Strata my overlap if not clearly defined.

### Quota sampling
Quota sampling is a non random sampling method where you interview each person and, based on there response, the relevant quota is incremented until the quota has been filled. An example of quota sampling would be taking a sample of the amount of people in your constituency that are going to vote for you, if 20% of people in that area are 18-29 then 20% of the interviews should be of 18-29 year olds.

 **Advantages**

- Can be done quickly as representative sample requires only a small sample size.
- Cheap.
- Simple.

**Disadvantages**

- Can't estimate sampling errors (because its not random).
- Interviewer must select whos included (could introduce bias).
- Non-responses are not recorded.

## Types of data

### Primary data
Collected by, or on behalf of, the person who is going to use it.

 **Advantages**

- Known collection method.
- Known accuracy.
- Exact data is collected.

**Disadvantages**

- Costs time, money and effort.

### Secondary data
Sourced elsewhere, not collected for the person who is going to use it.

 **Advantages**

- Cheap to obtain.
- Large quantity's of data available.
- Much data has been collected yearly allowing analisis of trends.

**Disadvantages**

- Bias is not always stated.
- Can be in a form that is difficult to process.

## Estimation, confidence intervals and tests

### Statistics and sampling distributions

> **Statistic**: A characteristic of a sample, if $$X_1, X_2, X_3, ..., X_n$$ is a random sample of size $$n$$ then a statistic $$T$$ is a random variable made of any function of $$X_i$$.

For example $$\frac{X_1 + X_2 + X_3}{3}$$ is a statistic because it only uses the samples, $$\sum_{i=1}^{n} (\frac{|X_i - \mu|}{n})$$ is not a statistic because it contains $$\mu$$, a population parameter.

> **Sampling Distribution**: Since sampling can be repeated, the sampling distribution of $T$ is a probability distribution for the given statistic.

### Estimating population parameters

> **Population parameter**: A characteristic of a population.
###### 
> **Estimator**: A statistic used to estimate a population parameter.

#### Example 1
For a random sample $$X_1, X_2, ..., X_n$$ with a distribution $$X \sim N(\mu, \sigma^2)$$ show that $$E(\bar{X}) = \mu$$

$$
\begin{align}
    \bar{X} &= \frac{1}{n}(X_1 + ... + X_n)\\
E(\bar{X}) &= \frac{1}{n}E(X_1 + ... + X_n)\\
                 &= \frac{1}{n}[E(X_1) + ... + E(X_n)]\\
                 &= \frac{1}{n}[\mu + ... + \mu]\\
                 &= \frac{n\mu}{n})\\
                 &= \mu
\end{align}
$$

$$
\begin{align}
    &\bar{X} = \frac{1}{n}(X_1 + ... + X_n)\\
&E(\bar{X}) = \frac{1}{n}E(X_1 + ... + X_n)\\
                 &= \frac{1}{n}[E(X_1) + ... + E(X_n)]\\
                 &= \frac{1}{n}[\mu + ... + \mu]\\
                 &= \frac{n\mu}{n})\\
                 &= \mu
\end{align}
$$

This means that $$\bar{X}$$ is an estimator for $$\mu$$ and on average, should give the correct result. This means $$\bar{X}$$ is an unbiased estimator for $$\mu$$

#### Example 2
Bolts of lengths 5cm and 10cm are produced in the ration 2:1 respectively. For a random sample of 3 bolts calculate the bias of the estimator of the mode.

Population mode is 5cm, because their are twice as many 5cm bolts as their are 10cm bolts.

All possible samples
$$
(5, 5, 5),\\
(5, 5, 10), (5, 10, 5), (10, 5, 5),\\
(5, 10, 10), (10, 5, 10), (10, 10, 5),\\
(10, 10, 10)\\
$$
Let $M$ be the sampling distribution for the population mode.
$$
\begin{align}
P(M = 5) &= (\frac{2}{3}^3 \times 1) + (\frac{2}{3}^2 \times \frac{1}{3} \times 3) \\
              &= \frac{8}{27} + \frac{4}{27} \times 3 \\
              &= \frac{20}{27}\\
\end{align}
$$

$$
\begin{align}
P(M = 10) &= (\frac{1}{3}^3 \times 1) + (\frac{2}{3} \times \frac{1}{3}^2 \times 3) \\
              &= \frac{1}{27} + \frac{2}{27} \times 3 \\
              &= \frac{7}{27}\\
\end{align}
$$

estimator of mode:
$$
\begin{align}
E(M) &= 5 \times \frac{20}{27} + 10 \times \frac{7}{27}\\
              &= \frac{100}{27} + \frac{70}{27} \\
              &= \frac{170}{27}
\end{align}
$$

bias:
$$
\begin{align}
\text{bias} &= E(M) - \text{mode}\\
              &= \frac{170}{27} - 5 \\
              &= \frac{35}{27} \\
              &= 1.30...
\end{align}
$$