+++
title = "Multilevel Feedback Queue Scheduling"
author = ["Harsha Somisetty"]
tags = ["Operating", "Systems", "Processes"]
draft = false
+++

## Multilevel feedback-queue scheduling {#multilevel-feedback-queue-scheduling}


### allows processes to move between queues, {#allows-processes-to-move-between-queues}


#### if too much cpu time is used, process is moved down a queue {#if-too-much-cpu-time-is-used-process-is-moved-down-a-queue}


#### i/o and itneractive processes are in higher queus {#i-o-and-itneractive-processes-are-in-higher-queus}


#### process that is in lower priority for too long is aged and moved up {#process-that-is-in-lower-priority-for-too-long-is-aged-and-moved-up}


### bunch of parameters that controls this algo {#bunch-of-parameters-that-controls-this-algo}


#### number of total queues {#number-of-total-queues}


#### scheudling algo for each queue {#scheudling-algo-for-each-queue}


#### method to promote and demote processes to new queues {#method-to-promote-and-demote-processes-to-new-queues}


#### method to know which queue a process should be assigned toc {#method-to-know-which-queue-a-process-should-be-assigned-toc}