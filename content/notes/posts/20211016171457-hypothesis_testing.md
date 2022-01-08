+++
title = "Hypothesis Testing"
author = ["Harsha Somisetty"]
tags = ["Statistics"]
draft = false
+++

## An assertion of a distribution of a random variable {#an-assertion-of-a-distribution-of-a-random-variable}


### decide to accept/reject a value of a parameter, based on how unlikely something is {#decide-to-accept-reject-a-value-of-a-parameter-based-on-how-unlikely-something-is}


## You can either accept a null or reject the null, but each choice comes with [Type 1 Error]({{< relref "20211016171143-type_1_error.md" >}}) and [Type 2 Error]({{< relref "20211016173402-type_2_error.md" >}}) {#you-can-either-accept-a-null-or-reject-the-null-but-each-choice-comes-with-type-1-error--20211016171143-type-1-error-dot-md--and-type-2-error--20211016173402-type-2-error-dot-md}


### Boy who cried wolf: type 1 error when falsely calling for wolf, then type 2 when village assumes lie {#boy-who-cried-wolf-type-1-error-when-falsely-calling-for-wolf-then-type-2-when-village-assumes-lie}


### Type 1 corressponds to &alpha;, 2 corress to &beta;. {#type-1-corressponds-to-and-alpha-2-corress-to-and-beta-dot}


#### These probabilities are inversely related, since if you make it easier to accept null (decrease &alpha;) you make it more likely to accept null when not true (increase &beta;) {#these-probabilities-are-inversely-related-since-if-you-make-it-easier-to-accept-null--decrease-and-alpha--you-make-it-more-likely-to-accept-null-when-not-true--increase-and-beta}


## Neyman-Pearson Theory talks about the [Power]({{< relref "20211016172954-power_of_a_test.md" >}}) of a test and maximizing 1-&beta; {#neyman-pearson-theory-talks-about-the-power--20211016172954-power-of-a-test-dot-md--of-a-test-and-maximizing-1-and-beta}


### A crit region for H_0 : &theta; = &theta;_0 against H_1: &theta; = &theta;_1 is best if the power of the test is max at H_1 {#a-crit-region-for-h-0-and-theta-and-theta-0-against-h-1-and-theta-and-theta-1-is-best-if-the-power-of-the-test-is-max-at-h-1}


### Dtermine the C by doing {#dtermine-the-c-by-doing}

\begin{align\*}
\frac{L\_{0}}{L\_{1}} \leq k \quad \text{ inside C}\\\\
\frac{L\_{0}}{L\_{1}} \geq k \quad \text{ outside C}
\end{align\*}

then C is a most power crit region of size A for testing &theta;_1 and &theta;_0