Suppose we are interested in a single unknown [[Population|population]] parameter $\theta$ for example $\mu$ ect. 
We define the null and alternative hypotheses like so:
- $H_{0}$: the null hypothesis that $\theta$ is equal to the value $r$
- $H_{a}$: the alternate hypothesis, which denies the null hypothesis (the type of denial makes it a one-sided or a two-sided test)
For example a two-sided test would look like:
- $H_{0}:\theta=r$
- $H_{a}:\theta \neq r$
And a one-sided test would look like:
- $H_{0}:\theta=r$
- $H_{a}:\theta>r$ or $H_{a}:\theta<r$
Given a particular [[Samples|sample]], should we reject the null hypothesis or not?
## Method: Two-Sided Case
If we have:
- A two-sided hypothesis (as above)
- An estimator for $\theta$ e.g. $\bar{X}\sim N\left( \mu, \frac{\sigma^{2}}{n} \right)$
- The sampling distribution of the estimator (as a function of $\theta$)
- A level of significance $\alpha$
Then we can construct a $(1-\alpha)$ confidence interval for $\theta$, and then we:
- Reject $H_{0}$ if $r$ lies outside the confidence interval, and we find the test statistically significant at the $\alpha$% level of significance
- Fail to reject $H_{0}$ if $r$ is in the confidence interval and find the test not signifiicant at the $\alpha$% level of significance 
## Method: One-Sided Case
If we have:
- A one-sided hypothesis (as above)
- An estimator for $\theta$ e.g. $\bar{X}\sim N\left( \mu, \frac{\sigma^{2}}{n} \right)$
- The sampling distribution of the estimator (as a function of $\theta$)
- A level of significance $\alpha$
Then we can contruct a $(1-2\alpha)$ confidence interval for $\theta$, and then we:
- Reject $H$ if $r$ falls to the right/left of the confidence interval
- Fail to reject $H_{0}$ otherwise
## Example
For cuckoo egg data, we had a $95\%$ confidence interval for $\mu$ (mean egg length) $[22.36,22.78]$
This would suggest evidence against $\mu=22$ as it is not inside the interval
We can perform hypothesis testing by checking whether a proposed value of $\mu$ lies inside the confidence interval 