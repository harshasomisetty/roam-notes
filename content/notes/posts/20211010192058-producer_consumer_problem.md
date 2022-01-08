+++
title = "Producer Consumer Problem"
author = ["Harsha Somisetty"]
tags = ["Operating", "Systems", "Data"]
draft = false
+++

## Producer Process produces info consumed by consumer process {#producer-process-produces-info-consumed-by-consumer-process}


## Simultaneous incremnet and decrementing of a variable {#simultaneous-incremnet-and-decrementing-of-a-variable}


### when changing a variable, the variable data is stored to register, register incremented, then stored back to variable {#when-changing-a-variable-the-variable-data-is-stored-to-register-register-incremented-then-stored-back-to-variable}


### However, if 2 process go at same time, the registers could store value right after each other, so only one change is saved {#however-if-2-process-go-at-same-time-the-registers-could-store-value-right-after-each-other-so-only-one-change-is-saved}


#### **Race condition** several process access same data, and the outcome depends on the sequence of data access {#race-condition-several-process-access-same-data-and-the-outcome-depends-on-the-sequence-of-data-access}


## Bounded Buffer Problem {#bounded-buffer-problem}


### buffer of n slots, 2 process go simultaneously, producer fills, consumer consumes {#buffer-of-n-slots-2-process-go-simultaneously-producer-fills-consumer-consumes}


#### Producer must not fill when buffer is full {#producer-must-not-fill-when-buffer-is-full}

```c
do{
  wait (empty); // wait until empty > 0, then decrement
  wait (mutex); //get mutex lock of the buffer
  /* critical section */
  signal (mutex); //release mutex lock of buffer
  signal (full); // filled part of buffer
  }while (TRUE)
```


#### consumer must not consume when buffer is empty {#consumer-must-not-consume-when-buffer-is-empty}

```C
do{
  wait (full); //wait until atleast one buffer slot is filled
  wait (mutex); //wait until buffer is not being modified
  /* critical sec */
  signal (mutex); //release mutex control
  signal (empty); // one more empty slot now
} while(TRUE)
```


#### both can't go at the same time {#both-can-t-go-at-the-same-time}


#### Can solve using [Semaphores]({{< relref "20211012093505-semaphores.md" >}}) {#can-solve-using-semaphores--20211012093505-semaphores-dot-md}

<!--list-separator-->

-  m (mutex)

<!--list-separator-->

-  empty (counting semaphore, init is size of buffer)

<!--list-separator-->

-  full (counting semaphore, init is 0, count of filled slots)


###  {#}