+++
title = "Critical Section Problem"
author = ["Harsha Somisetty"]
tags = ["Operating", "Systems"]
draft = false
+++

## **Critical Section** is the parts of a process that changes the variables, writing, etc in the shared memory {#critical-section-is-the-parts-of-a-process-that-changes-the-variables-writing-etc-in-the-shared-memory}


## Race Condition is when multiple threads enter the critical section at the same time {#race-condition-is-when-multiple-threads-enter-the-critical-section-at-the-same-time}


### want to make it so that only one process can execute critical section at once (by asking permission) {#want-to-make-it-so-that-only-one-process-can-execute-critical-section-at-once--by-asking-permission}


#### code has entry section before entering critical {#code-has-entry-section-before-entering-critical}


#### has exit session before leaving critical {#has-exit-session-before-leaving-critical}


#### rest of code is remainder section {#rest-of-code-is-remainder-section}


## The Problem is to design a protocol that the processes can use to cooperate {#the-problem-is-to-design-a-protocol-that-the-processes-can-use-to-cooperate}


### Want [Mutual Exclusion]({{< relref "20211011095955-mutual_exclusion.md" >}}) of threads {#want-mutual-exclusion--20211011095955-mutual-exclusion-dot-md--of-threads}


### Progress {#progress}


#### only processes that are not in the remainder section of code can decide which process can enter critical section next, and must be done quickly {#only-processes-that-are-not-in-the-remainder-section-of-code-can-decide-which-process-can-enter-critical-section-next-and-must-be-done-quickly}


### Bounded waiting {#bounded-waiting}


#### Limit on how many times a process's critical section request can be postponed, so that the process doesn't get starved {#limit-on-how-many-times-a-process-s-critical-section-request-can-be-postponed-so-that-the-process-doesn-t-get-starved}