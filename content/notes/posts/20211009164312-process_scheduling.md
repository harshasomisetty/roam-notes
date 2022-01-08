+++
title = "Process Scheduling"
author = ["Harsha Somisetty"]
tags = ["Operating", "Systems"]
draft = false
+++

## Preemptive and non-preemptive scheduling {#preemptive-and-non-preemptive-scheduling}


### **CPU** scheduler: a process that selects which process to pick next {#cpu-scheduler-a-process-that-selects-which-process-to-pick-next}


### **Dispatcher** gives control fo the cpu to the process selected byt he spu scheduler {#dispatcher-gives-control-fo-the-cpu-to-the-process-selected-byt-he-spu-scheduler}


#### dispatch latency is the time it takes to stop one process and start another process {#dispatch-latency-is-the-time-it-takes-to-stop-one-process-and-start-another-process}


### Process must be swtched when: {#process-must-be-swtched-when}


#### terminated, running to waiting, waiting to running, running to ready {#terminated-running-to-waiting-waiting-to-running-running-to-ready}

<!--list-separator-->

-  first two must always be scheudled, but last two, can decide to give back contorl to process ,or give it to a differnet process


#### Preemptive is when cpu is taken away before completion (3, 4), {#preemptive-is-when-cpu-is-taken-away-before-completion--3-4}

<!--list-separator-->

-  bad when first process didn't finish a result, but second process reads this unfinsihed data


#### Non-preemptive si when cpu is taken away only after comletion {#non-preemptive-si-when-cpu-is-taken-away-only-after-comletion}


## Algorithm Criteras {#algorithm-criteras}


### CPU Utilization {#cpu-utilization}


#### keeping cpu as busy as possible, ideally from 40-90% {#keeping-cpu-as-busy-as-possible-ideally-from-40-90}


### Throughput {#throughput}


#### how many processes are completed per unit of time {#how-many-processes-are-completed-per-unit-of-time}


#### POV of cpu {#pov-of-cpu}


### Turnaround Time = Completion time - arrival time {#turnaround-time-completion-time-arrival-time}


#### Interval of time to submit a process to completing the process {#interval-of-time-to-submit-a-process-to-completing-the-process}


#### Sum of periods waiting to get into memory, waiting in ready queue, executing, and doing IO {#sum-of-periods-waiting-to-get-into-memory-waiting-in-ready-queue-executing-and-doing-io}


#### POV of process {#pov-of-process}


### Waiting time = Turn Around time - Burst Time {#waiting-time-turn-around-time-burst-time}


#### number of periods spent waiting inthe read queue {#number-of-periods-spent-waiting-inthe-read-queue}


### Response Time {#response-time}


#### tiem from the submission of a request to when the first response is produced {#tiem-from-the-submission-of-a-request-to-when-the-first-response-is-produced}


## Algorithms {#algorithms}


### [First Come First Serve]({{< relref "20211013111904-first_come_first_serve.md" >}}) {#first-come-first-serve--20211013111904-first-come-first-serve-dot-md}


### [Shortest Job First]({{< relref "20211013111934-shortest_job_first.md" >}}) {#shortest-job-first--20211013111934-shortest-job-first-dot-md}


### [Priority Scheduling]({{< relref "20211013112009-priority_scheduling.md" >}}) {#priority-scheduling--20211013112009-priority-scheduling-dot-md}


### [Round Robin]({{< relref "20211013112035-round_robin.md" >}}) {#round-robin--20211013112035-round-robin-dot-md}


### [Multilevel Queue Scheduling]({{< relref "20211013112116-multilevel_queue_scheduling.md" >}}) {#multilevel-queue-scheduling--20211013112116-multilevel-queue-scheduling-dot-md}


### [Multilevel Feedback Queue Scheduling]({{< relref "20211013112148-multilevel_feedback_queue_scheduling.md" >}}) {#multilevel-feedback-queue-scheduling--20211013112148-multilevel-feedback-queue-scheduling-dot-md}