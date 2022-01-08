+++
title = "Likelihood-ratio-test"
author = ["Harsha Somisetty"]
tags = ["Hypothesis", "Power", "Chi", "Squared"]
draft = false
+++

## Compares 2 tests to see which model has the better liklihood {#compares-2-tests-to-see-which-model-has-the-better-liklihood}


### generalization of [Neyman-Pearson Lemma]({{< relref "20211219103931-neyman_pearson_lemma.md" >}}) {#generalization-of-neyman-pearson-lemma--20211219103931-neyman-pearson-lemma-dot-md}


### one model's params are nested inside others, so it automatically fits worse, but we want to see if this is statistically significant {#one-model-s-params-are-nested-inside-others-so-it-automatically-fits-worse-but-we-want-to-see-if-this-is-statistically-significant}


#### we do this by comparing log likelhoods of both models, {#we-do-this-by-comparing-log-likelhoods-of-both-models}


## Math: {#math}

\begin{align\*}
\lambda &= \frac{Max L\_{0}}{Max L\_{1}}\\\\
LR &= 2 ( log \frac{ L(\theta\_{{H\_{1}}})}{L(\theta\_{{H\_{0}}})}) \sim X^{2}\_{q}
\end{align\*}

q is how many parameter restrictions are placed on the null

in the first defintiion, it is just a ratio, we reject H_0 if frac is close to 0 (denom is much greater), accept if H_0 is close enough, so near 1
in the second defition, it is a chi-squared dist, so we accept if total likelihoods are close enough (resulting in 0), and reject if signficantly different