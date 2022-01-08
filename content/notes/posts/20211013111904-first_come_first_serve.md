+++
title = "First Come First Serve"
author = ["Harsha Somisetty"]
tags = ["Operating", "Systems", "Processes"]
draft = false
+++

## First Come First Serve {#first-come-first-serve}


### process that requests cpu first gets cpu first, implemented with FIFO queue {#process-that-requests-cpu-first-gets-cpu-first-implemented-with-fifo-queue}


### PCB is added to the tail fo the queue, then when cpu is free, head of queue is taken and allocated and removed from queue {#pcb-is-added-to-the-tail-fo-the-queue-then-when-cpu-is-free-head-of-queue-is-taken-and-allocated-and-removed-from-queue}


### the avf waiting time changes (larger time if longer processes arrive first) {#the-avf-waiting-time-changes--larger-time-if-longer-processes-arrive-first}


#### convoy effect, when smaller processes hav eot wait longer since long processes came first {#convoy-effect-when-smaller-processes-hav-eot-wait-longer-since-long-processes-came-first}


### NONPREEMPTIVE algo {#nonpreemptive-algo}


### _very bad for timesharing, since each process can't get cpu at regular intervals_ {#very-bad-for-timesharing-since-each-process-can-t-get-cpu-at-regular-intervals}


### can calcuate efficiency if there is a overhead (useful time/ total time) {#can-calcuate-efficiency-if-there-is-a-overhead--useful-time-total-time}