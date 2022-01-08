+++
title = "Efficiency of Estimators"
author = ["Harsha Somisetty"]
tags = ["Statistics"]
draft = false
+++

## Choosing estimator with smallest variance {#choosing-estimator-with-smallest-variance}


### **Minimum variance unbiased estimator** is the unbiased estimator with the smallest variance {#minimum-variance-unbiased-estimator-is-the-unbiased-estimator-with-the-smallest-variance}


###  {#}


## Cramer-Rao Inequality {#cramer-rao-inequality}

if \\( \hat{\Theta}\\) is an unbiased estimator of &theta;, and

\begin{align\*}
var(\hat{\Theta}) &= \frac{1}{n\*E\big[\big(\frac{\partial lnf(X)}{\partial\theta}\big)^{2}\big]} = \frac{1}{n\*E\big[\frac{\partial^{2} lnf(X)}{\partial^{}\theta^{2}}\big^{}\big]}
\end{align\*}

then &Theta; is a minimum variance unbiased estimator

The bottom term is the information of the parameter given by the sample
so smaller the variance, more information we have


### Explanation {#explanation}

if f is the log likihood function, the derivative shows how steep the curve is
if the curve is steep, then the function has a very specific max point, and we are more sure of our estimate, since there are only a very small number of other guese that even come close to that max point of the graph
then, if we take the inverse, since the wider liklihood functions have a smaller derivative, the have a higher inverse, and therefore a higher variance
the good graphs have a low variance, and we are good (since we try to minimize the variance)