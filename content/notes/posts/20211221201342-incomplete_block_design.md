+++
title = "Incomplete Block Design"
author = ["Harsha Somisetty"]
tags = ["DOE", "Block"]
draft = false
+++

## When not enough units in block to test all treatments {#when-not-enough-units-in-block-to-test-all-treatments}


### Balanced incomplete: can run all combinations of incomplete blocks {#balanced-incomplete-can-run-all-combinations-of-incomplete-blocks}


#### k is block size {#k-is-block-size}


#### B is number of blocks {#b-is-number-of-blocks}


#### G is number of treatments {#g-is-number-of-treatments}


#### r is number of times treatment is replicated {#r-is-number-of-times-treatment-is-replicated}


#### &lambda; is number of times each treatment pair occurs in block {#and-lambda-is-number-of-times-each-treatment-pair-occurs-in-block}

&lambda; being the same fo all pairs of treatments makes it balanced (variance of estimated iff in treatment effects is same for all pairs)
N = kB = rG

need

\begin{align\*}
\lambda = \frac{r(k-1)}{(G-1)}
\end{align\*}

to be whole number

all possible combiations results in needing  \\(G \choose k\\) blocks, which might be large
but if small number, then randomly assing blocks to each treatment grouping
randomly assing units to each letter in grouping
randomly assign letters to correspong to actual treatments