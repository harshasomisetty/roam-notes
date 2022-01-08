+++
title = "Maximum Likelihood Estimation"
author = ["Harsha Somisetty"]
tags = ["Statistics", "Point-estimation"]
draft = false
+++

## Understanding {#understanding}


### uses [Likelihood Principle]({{< relref "20211120093444-likelihood_principle.md" >}}) to find parameter with greatest liklihood {#uses-likelihood-principle--20211120093444-likelihood-principle-dot-md--to-find-parameter-with-greatest-liklihood}


#### Done by maximizing a likelihood function" {#done-by-maximizing-a-likelihood-function}


#### log so math is easier, then get derivative at 0, then solve for parameter {#log-so-math-is-easier-then-get-derivative-at-0-then-solve-for-parameter}


## Example {#example}


### Binomial {#binomial}

You want to estimate parameter p of Bernoulli. Say you have 6 bernoulli trials, 5 successes. (This sample does not change, so this is likelihood)
this is binomial dist with X = 5, n = 6, so pdf is f(x|p) = \\(n \choose 5\\)p^x (1-p)<sup>n-x</sup>
then log is

\begin{align\*}
log({n \choose 5} ) + x log(p) + (n-x) log(1-p)
\end{align\*}

then derivative is

\\(\frac{x}{p} + \frac{- (n-x)}{1-p} = 0 \\)
then solving, we get \\( \hat{p} = \frac{x}{n} \\)
in this case, we know X = 5, n = 6, so
\\( \hat{p} = \frac{5}{6} \\)