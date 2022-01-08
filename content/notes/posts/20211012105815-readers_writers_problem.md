+++
title = "Readers-Writers Problem"
author = ["Harsha Somisetty"]
tags = ["Operating", "Systems", "Processes", "Synchronization"]
draft = false
+++

## Shared db, some reader process that only read, some writers processes that only want to write {#shared-db-some-reader-process-that-only-read-some-writers-processes-that-only-want-to-write}


### 2 readers are okay, but one writer and one reader would mess things up {#2-readers-are-okay-but-one-writer-and-one-reader-would-mess-things-up}


#### So, we give one writer exclusive access to db, and all readers access to db {#so-we-give-one-writer-exclusive-access-to-db-and-all-readers-access-to-db}


## Solve using [Semaphores]({{< relref "20211012093505-semaphores.md" >}}) {#solve-using-semaphores--20211012093505-semaphores-dot-md}


### variables {#variables}


#### Mutex mutual exlusion for when reader count goes up or down (remember the increment and decrementing problem) {#mutex-mutual-exlusion-for-when-reader-count-goes-up-or-down--remember-the-increment-and-decrementing-problem}


#### WRT if held by writer, then no readers can start, but if reader holds, then no writer can write {#wrt-if-held-by-writer-then-no-readers-can-start-but-if-reader-holds-then-no-writer-can-write}


#### Readcount integer variable (see if there are atleast 1 readers, if only 1, we activate and deactivate permission for writer {#readcount-integer-variable-see-if-there-are-atleast-1-readers-if-only-1-we-activate-and-deactivate-permission-for-writer}


### Processes {#processes}


#### Writer {#writer}

First waits for writer sema, then does crt and releases writer sema


#### Reader {#reader}

First waits for mutex to increment reader count properly
increment reader count, release mutex
IF this is the first reader, take control of wrt
do reading, once done, get mturex, end process decrement reader count
IF Last reader, then release writer