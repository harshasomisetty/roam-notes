+++
title = "Linear Regression"
author = ["Harsha Somisetty"]
tags = ["Statistics", "Estimators"]
draft = false
+++

## Finding a correlation between many features and some result {#finding-a-correlation-between-many-features-and-some-result}


### Basically a scoring system of the most important feature {#basically-a-scoring-system-of-the-most-important-feature}

Y<sub>pred</sub> = &beta;_1 X<sub>1</sub> + &beta;_2 X_2 ... + &beta;_0
Y_pred =  &beta;^T X<sub>new</sub> + &beta;_0

&beta;^T X<sub>new</sub> = &sum;_1^p X<sub>new,j</sub>&beta;_j (X and &beta; are both p dimensional vectors)

Then, we can just add the &beta;_0 to the beta vector and add a 1 to X<sub>new</sub>, so
Y_pred =  &beta;^T X<sub>new</sub>


## Linear regression is about minimizing the difference between Y values and the &beta; X value {#linear-regression-is-about-minimizing-the-difference-between-y-values-and-the-and-beta-x-value}


### goal {#goal}

Find \\(\hat{\beta}\\) so that
&sum;_1^n (Y<sub>train,i</sub> - &beta;^T X<sub>new</sub>)^2 is minimized, or
\\(\hat{\beta}\\) = argmin<sub>&beta;</sub> ||Y-X&beta;||^2_2

Y is a (n \* 1) vector, X is (n \* (p+1)), B is ((p+1)\*1),
Then, the p norm is just squared summation


#### Notation {#notation}

[wiki pnorm](https://en.wikipedia.org/wiki/Norm_(mathematics)#p-norm) [stack overflow](https://stats.stackexchange.com/questions/181620/what-is-the-meaning-of-super-script-2-subscript-2-within-the-context-of-norms): Essentially finding the squared euclidean norm (subscript implies p norm, superscript implies squaring)


### Closed form solution {#closed-form-solution}

\\(\hat{\beta}\\) = (X^T X)<sup>-1</sup> X^T Y
(check [these notes page 3](</ox-hugo/Linear regression note.pdf>))


#### More results {#more-results}

so then, we can calculate the


### CAUTION {#caution}


#### Correlation between features {#correlation-between-features}

remember that the predictors &beta; can change together, but regression relies on the predictors staying the same

essentially, if the feature for one predict increases, it should not affect the appropriate value of a different predictor

like if you have x_1 coins, x_2 pennies, x_3 nickles, x_4 dimes, and you want to predict amount of change, if you increase the number of pennies, it decreases the overall change you have, if the number of coins stay the same (the appropriate value of a different predictor should not change, but it did)


#### Not predictive {#not-predictive}

You can't use a linear model to see what to change to get a different result

for ex, if you have a model on number of bedrooms and sqft living to calculate price, you can't just increase sqft to increase price of home a certain amount (price would go up, but might not go up as much as expected since there might be other factors)


## Ridged Linear Regression {#ridged-linear-regression}


### Good against data that has multicolinearity {#good-against-data-that-has-multicolinearity}


### Forces some parameters to 0 {#forces-some-parameters-to-0}


### has closed form solution {#has-closed-form-solution}


### [Training, Validation, Overfitting]({{< relref "20211102171337-training_validation_overfitting.md" >}}) {#training-validation-overfitting--20211102171337-training-validation-overfitting-dot-md}


#### Higher &lambda;, higher bias, lower variance (under fitting to training data) {#higher-and-lambda-higher-bias-lower-variance--under-fitting-to-training-data}


#### Lower &lambda;, Higher variance, lower bias (overfitting to training) {#lower-and-lambda-higher-variance-lower-bias--overfitting-to-training}