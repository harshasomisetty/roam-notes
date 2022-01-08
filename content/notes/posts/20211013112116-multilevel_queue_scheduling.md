+++
title = "Multilevel Queue Scheduling"
author = ["Harsha Somisetty"]
tags = ["Operating", "Systems", "Processes"]
draft = false
+++

## Multilevel queue scheduling {#multilevel-queue-scheduling}


### when processes can be grouped into types, can use more appropriate types of schelding {#when-processes-can-be-grouped-into-types-can-use-more-appropriate-types-of-schelding}


#### foregroudn processes need faster response, background doesn't need as muchz {#foregroudn-processes-need-faster-response-background-doesn-t-need-as-muchz}

<!--list-separator-->

-  Round robin for foreground

<!--list-separator-->

-  Background by an FCFS (longer waiting time, but doesn't matter)

<!--list-separator-->

-  **Fixed priority preemptive scheudlign**, so that foreground queue would always have priority over the background queue


#### different priority levels {#different-priority-levels}


#### based on property of process like memory size, priority, process type {#based-on-property-of-process-like-memory-size-priority-process-type}


#### each queue has own algo {#each-queue-has-own-algo}


### so, all processes are paritions into different queues, and schelding takes place within and amoung the queues {#so-all-processes-are-paritions-into-different-queues-and-schelding-takes-place-within-and-amoung-the-queues}