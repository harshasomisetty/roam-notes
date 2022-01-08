+++
title = "Peterson's Solution"
author = ["Harsha Somisetty"]
tags = ["Operating", "Systems", "Processes"]
draft = false
+++

## Software solution with good algorithimic intuition to solution. But doens't work properly on modern computer architecture {#software-solution-with-good-algorithimic-intuition-to-solution-dot-but-doens-t-work-properly-on-modern-computer-architecture}


### Restricted to 2 alternating processes that alternate btwn critical and remainder {#restricted-to-2-alternating-processes-that-alternate-btwn-critical-and-remainder}


### 2 data items to be shared btwn processes {#2-data-items-to-be-shared-btwn-processes}


#### int turn: who's turn it is {#int-turn-who-s-turn-it-is}


#### bool flag: if a process is ready to enter critical {#bool-flag-if-a-process-is-ready-to-enter-critical}


### The algo is "humble" in that it lets the other process go first {#the-algo-is-humble-in-that-it-lets-the-other-process-go-first}

```c
do {
  flag[i] = true; /*cur process is ready to execute*/
  turn = j; /* other process gets turn first */
  while(flag[j] && turn == j) ; /* forever loop while the other process wants to execute, but if not, breaks*/
  cur critical section
  flag[i] = false;
  remainder
    } while (true);
```