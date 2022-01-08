+++
title = "Shortest Job First"
author = ["Harsha Somisetty"]
tags = ["Operating", "Systems", "Processes"]
draft = false
+++

## Shortest Job First {#shortest-job-first}


### each process has it's cpu burst time associated with it {#each-process-has-it-s-cpu-burst-time-associated-with-it}


#### remember, not full process length, but just the next burst {#remember-not-full-process-length-but-just-the-next-burst}


### When cpu is available, shortest burst process is done, and if two processes have same cpu, then FCFS is used {#when-cpu-is-available-shortest-burst-process-is-done-and-if-two-processes-have-same-cpu-then-fcfs-is-used}


### This has a lower avg waiting time compared to FCFS when non-premtive {#this-has-a-lower-avg-waiting-time-compared-to-fcfs-when-non-premtive}


### When Premtive, executing threads may stop, so it is shortest remaining time first scheduling. {#when-premtive-executing-threads-may-stop-so-it-is-shortest-remaining-time-first-scheduling-dot}


#### wait times are different, look at example if needed {#wait-times-are-different-look-at-example-if-needed}


### _practically, you don't know the length of the next cpu burst, so can't be used for short term scheduling_ {#practically-you-don-t-know-the-length-of-the-next-cpu-burst-so-can-t-be-used-for-short-term-scheduling}


#### however, we can approximate next burst by assumign it is similar to the last cpu burst time {#however-we-can-approximate-next-burst-by-assumign-it-is-similar-to-the-last-cpu-burst-time}