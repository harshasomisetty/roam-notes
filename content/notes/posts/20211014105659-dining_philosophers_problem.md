+++
title = "Dining Philosophers Problem"
author = ["Harsha Somisetty"]
tags = ["Operating", "Systems", "Process", "Synchronization", "Problems"]
draft = false
+++

## You have x process and x resourcs, and each process needs 2 resources (2 next to each other) {#you-have-x-process-and-x-resourcs-and-each-process-needs-2-resources--2-next-to-each-other}


### The base algo waits for resource i, then resource i+1 {#the-base-algo-waits-for-resource-i-then-resource-i-plus-1}


## This can cause a deadlock when all processes pick up resource i at the same time {#this-can-cause-a-deadlock-when-all-processes-pick-up-resource-i-at-the-same-time}


### Allow only x-1 processes at once, {#allow-only-x-1-processes-at-once}


### processes take resources in critical section (mutual exclusion) {#processes-take-resources-in-critical-section--mutual-exclusion}


### Even processes pbick i+1 then i, odd processes pick i then i+1 {#even-processes-pbick-i-plus-1-then-i-odd-processes-pick-i-then-i-plus-1}