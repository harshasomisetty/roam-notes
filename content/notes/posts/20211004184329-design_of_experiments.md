+++
title = "Design Of Experiments"
author = ["Harsha Somisetty"]
tags = ["MOC"]
draft = false
+++

[Literature Notes]({{< relref "DOE" >}})

Design of Experiments is exploring causal relations by changing independent variables and studying effects


## Designs {#designs}


### [Completely Randomized Designs]({{< relref "20211018091950-completely_randomized_designs.md" >}}) {#completely-randomized-designs--20211018091950-completely-randomized-designs-dot-md}


#### [Factorial Design]({{< relref "20211019210029-factorial_design.md" >}}) {#factorial-design--20211019210029-factorial-design-dot-md}

<!--list-separator-->

-  [Contrasts]({{< relref "202110151506490-contrasts.md" >}})

    <!--list-separator-->

    -  Designing tests when treatment group means are actually different


### [Split Plot Design]({{< relref "20211209121834-split_plot_design.md" >}}) {#split-plot-design--20211209121834-split-plot-design-dot-md}


#### hard to change factors {#hard-to-change-factors}


### [Blocked Design]({{< relref "20211209121846-blocked_design.md" >}}) {#blocked-design--20211209121846-blocked-design-dot-md}


#### know something affects results, and you don't want to consider it {#know-something-affects-results-and-you-don-t-want-to-consider-it}


## Factors can be {#factors-can-be}


### [Nested Models]({{< relref "20211213015826-nested_models.md" >}}) or crossed {#nested-models--20211213015826-nested-models-dot-md--or-crossed}


### [Fixed effects]({{< relref "20220107200439-fixed_effects.md" >}}) and [Random Effects]({{< relref "20220107200603-random_effects.md" >}}) {#fixed-effects--20220107200439-fixed-effects-dot-md--and-random-effects--20220107200603-random-effects-dot-md}


### Covariates: information that isn't used but can be avoided? {#covariates-information-that-isn-t-used-but-can-be-avoided}


### [Multiple Testing]({{< relref "20211016171032-multiple_comparisons.md" >}}) {#multiple-testing--20211016171032-multiple-comparisons-dot-md}


### [DOE Assumptions]({{< relref "20211018095732-doe_assumptions.md" >}}) {#doe-assumptions--20211018095732-doe-assumptions-dot-md}


#### [Importance of Randomization]({{< relref "20211018092255-important_of_randomization.md" >}}) {#importance-of-randomization--20211018092255-important-of-randomization-dot-md}


## Keep in mind {#keep-in-mind}


### Mistakes {#mistakes}


#### randomize treatments, no control over which unit has which treatment {#randomize-treatments-no-control-over-which-unit-has-which-treatment}


#### have a comparision group to see how effective a treatment is {#have-a-comparision-group-to-see-how-effective-a-treatment-is}


#### tldr: one experiment is no bueno {#tldr-one-experiment-is-no-bueno}


## Definitions {#definitions}


### [Factors]({{< relref "20211213012754-factors.md" >}}) {#factors--20211213012754-factors-dot-md}


### _Experimental units_ recieve the treatments and produce the measurement units (we study the casual effects) {#experimental-units-recieve-the-treatments-and-produce-the-measurement-units--we-study-the-casual-effects}

clusterign can change exposure distriubtions in experiments

using clustering, you can reduce interaction affects, You can do least cut to form subgroups, and treat these groups as the new experiment units


## checklist for experiments {#checklist-for-experiments}


### define clear objectives {#define-clear-objectives}


### identify sources of variation {#identify-sources-of-variation}


#### treatment factors and levels {#treatment-factors-and-levels}


#### experimental units {#experimental-units}


#### blocking factors, noise factors, covariates {#blocking-factors-noise-factors-covariates}


### Choose rule for assigning experimental units to treatments {#choose-rule-for-assigning-experimental-units-to-treatments}


### specify measures to be made, experimental produced, difficulties, and model {#specify-measures-to-be-made-experimental-produced-difficulties-and-model}


### run experiment and analyze {#run-experiment-and-analyze}


## diet supplements and music genre on cow milk production {#diet-supplements-and-music-genre-on-cow-milk-production}

6 dairy farmers
40 cows per farmers
cows divided between 4 supplements

each farmer gets a music, 2 per music

overall, split plot design

2 replicates
whole plot factor: music genre
split plot factor: supplement
whole plot unit: farmer
split plot unit: cows


## shvaing cream on skin irritation {#shvaing-cream-on-skin-irritation}

30 individuals,
half of face for each shave
randomized which side of face

matched pairs randomized
outcome: irritation
treatment: type of cream
block or pair: individuals
unit: half of face


## shaving cream on skin irritation {#shaving-cream-on-skin-irritation}

prev question, but 5 different creams,
pp


## playgounds {#playgounds}

12 playgrounds (4 low use, 4 mid, 4 high)
2 levels of new surface (woodchips, grass)
3 levels of LED (positive, active, none), dif one each weekend

split plot with blocking on activity level

so outcome: amount of use
whole plot factor: surface
split plot factor: message
blocking: lvl of use
whole plot unit: playground
split plot unit: weekend


## Effect of drainage and variety of tulip on flower production {#effect-of-drainage-and-variety-of-tulip-on-flower-production}

12 plots
4 levels of soil drainage
15 levels of tulips

split plot, since hard to change soil drainage
whole plot factor: drainage
WP unit: site
SP factor: variety of tulip
SP unit: combiation


## effect of type of sales and coockie selection on sales {#effect-of-type-of-sales-and-coockie-selection-on-sales}

2 levels of sales
4 levels of cookie selection menu

WP factor: menu
WP unit: council
SP factor: type of sale
SP unit: troop


## effect of hours of light on Rodent activity {#effect-of-hours-of-light-on-rodent-activity}

3 levels of lgiht
Latin Squares
block factor: mice &amp; time
8 replications, 3 mice, block on time and mouse


## effect of meditaiton vids and cushions on stress {#effect-of-meditaiton-vids-and-cushions-on-stress}

4 levels of videos
3 levels of cushions

strip plot


## effect of announcement, scolding, and letter on student lateness {#effect-of-announcement-scolding-and-letter-on-student-lateness}

2 levels of teachers publically discussing lates
2 levels of individual confrontation

2 levels of letters