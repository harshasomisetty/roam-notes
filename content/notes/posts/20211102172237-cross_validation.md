+++
title = "Cross Validation"
author = ["Harsha Somisetty"]
tags = ["Machine", "Learning", "Bias", "Variance"]
draft = false
+++

## If you want to compare multiple models, we can't just train every model on just training data {#if-you-want-to-compare-multiple-models-we-can-t-just-train-every-model-on-just-training-data}


### Say suppose model a trains on 2 parameters, and  model b has 10 parameters, then model B has more [Degrees of Freedom]({{< relref "20211102172436-degrees_of_freedom.md" >}}), and overfits relative to the first model {#say-suppose-model-a-trains-on-2-parameters-and-model-b-has-10-parameters-then-model-b-has-more-degrees-of-freedom--20211102172436-degrees-of-freedom-dot-md--and-overfits-relative-to-the-first-model}


## Instead, we take the training data, split it up into chunks, and keep one chunk as validation, rest as training {#instead-we-take-the-training-data-split-it-up-into-chunks-and-keep-one-chunk-as-validation-rest-as-training}


### then, each model is trained on different chunks so the DoF phenomenon doesn't happen, and tested ont he different validation error {#then-each-model-is-trained-on-different-chunks-so-the-dof-phenomenon-doesn-t-happen-and-tested-ont-he-different-validation-error}

the more general the model, the smaller the training error