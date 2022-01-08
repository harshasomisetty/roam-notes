+++
title = "Confidence Intervals"
author = ["Harsha Somisetty"]
tags = ["Statistics", "Estimation", "Confidence"]
draft = false
+++

## Core idea is to describe how much information a point estimate is based on, and determine the size of error {#core-idea-is-to-describe-how-much-information-a-point-estimate-is-based-on-and-determine-the-size-of-error}

We need to find the \\(\hat{\theta\_1}, \hat{\theta\_{2}}\\) (estimates) of RV \\(\hat{\Theta\_1}, \hat{\Theta\_{2}}\\) st \\(P(\hat{\Theta\_{1}} < \theta < \hat{\Theta\_{2}}) = 1 - \alpha\\). The estimators for those &Theta; are the (1-&alpha;)100% confidence interval for &theta;


## CI Formulas {#ci-formulas}


### Mean {#mean}

When its just one mean, we know that a sample of size has variance \\(\frac{\sigma}{\sqrt{n}}\\), so CI is \\( \mu - \bar{x} < |z\_{\alpha/2} \* \frac{\sigma}{\sqrt{n}}|\\)
(for one sided, take z<sub>&alpha;</sub>), and just upper or lower bound
and if small smaple size, use T dist, with DF n-1


### Between means {#between-means}

Can have different or same variances, so use appropriate estimator (if same, can be a [Pooled Statistic]({{< relref "20211122114511-pooled_statistic.md" >}})


### Proportions {#proportions}


### Variances {#variances}