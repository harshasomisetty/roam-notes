+++
title = "Memory Management"
author = ["Harsha Somisetty"]
tags = ["Operating", "Systems", "Memory", "File", "Main"]
draft = false
+++

## memory needs to be allocated efficiently to pack as many processes into memory as possible {#memory-needs-to-be-allocated-efficiently-to-pack-as-many-processes-into-memory-as-possible}


### so that the CPU won't be idle just waiting for i/o {#so-that-the-cpu-won-t-be-idle-just-waiting-for-i-o}


## Goals for multiprograming {#goals-for-multiprograming}


### Transparency: make sure processes aren't aware memory is shared {#transparency-make-sure-processes-aren-t-aware-memory-is-shared}


#### works regardless of number of processes or location {#works-regardless-of-number-of-processes-or-location}


#### Processes can be _relocated_ due to swapping {#processes-can-be-relocated-due-to-swapping}


### protection: cna't corrupt OS, and read data of other processes {#protection-cna-t-corrupt-os-and-read-data-of-other-processes}


### Efficiency: don't waste memory resources and too much fragmentation {#efficiency-don-t-waste-memory-resources-and-too-much-fragmentation}


### Sharing: for processes that do work together, allow for sharing of address space {#sharing-for-processes-that-do-work-together-allow-for-sharing-of-address-space}


## Abstracting memory to each process {#abstracting-memory-to-each-process}


### Static Memory {#static-memory}


#### code and global variables {#code-and-global-variables}


### Dynamic Memory {#dynamic-memory}


#### Why {#why}

<!--list-separator-->

-  Don't know how much mem at compile time, need enough for worst case

<!--list-separator-->

-  don't know size of recursive calls

<!--list-separator-->

-  complex DS


#### Stack {#stack}

<!--list-separator-->

-  Used for procedure call frames (local variables and parameters


#### Heap {#heap}

<!--list-separator-->

-  Consists of free and allocated spaces

<!--list-separator-->

-  can be slow


## Memory Management Algos {#memory-management-algos}


### programs get virtual memory {#programs-get-virtual-memory}


#### address translation: hardware transofmr memory access call for a virtual address to a physical access {#address-translation-hardware-transofmr-memory-access-call-for-a-virtual-address-to-a-physical-access}


### Primitive Bare-machine (Hardware dynamic translation) {#primitive-bare-machine--hardware-dynamic-translation}


#### each cpu has a base and bound register, allows us to place address space anywhere in memeory {#each-cpu-has-a-base-and-bound-register-allows-us-to-place-address-space-anywhere-in-memeory}


#### each program thinks it starts at 0, but OS keeps track of specific location to load program, and [MMU]({{< relref "20211101144512-memory_management_unit.md" >}}) later translate the address from virtual to physical {#each-program-thinks-it-starts-at-0-but-os-keeps-track-of-specific-location-to-load-program-and-mmu--20211101144512-memory-management-unit-dot-md--later-translate-the-address-from-virtual-to-physical}


#### os needs to  find space for process, reclaim space after completion, and help in context switches {#os-needs-to-find-space-for-process-reclaim-space-after-completion-and-help-in-context-switches}


#### but inefficient because it causes internal fragmentation ( when a chunk of mem is much bigger than process, and too much space is just not used (can be fixed with best fit algo)) (since fixed sized slots are bad) {#but-inefficient-because-it-causes-internal-fragmentation--when-a-chunk-of-mem-is-much-bigger-than-process-and-too-much-space-is-just-not-used-can-be-fixed-with-best-fit-algo----since-fixed-sized-slots-are-bad}


### [Segmentation]({{< relref "20211220210331-segmentation.md" >}}) {#segmentation--20211220210331-segmentation-dot-md}


### [Paging]({{< relref "20211220210226-paging.md" >}}) {#paging--20211220210226-paging-dot-md}


### Combined paging and segmentation {#combined-paging-and-segmentation}


## Virtualizing Memory {#virtualizing-memory}


### Time Sharing memory: BAD {#time-sharing-memory-bad}


#### occasionally saving CPU registers to memory when process is idle {#occasionally-saving-cpu-registers-to-memory-when-process-is-idle}

<!--list-separator-->

-  can even save memory to disk to meta-virtualize


#### Veryyy slow, instead share space {#veryyy-slow-instead-share-space}


### Static Relocation {#static-relocation}


#### every switch to process, process is rewriten with new addresses and pointers {#every-switch-to-process-process-is-rewriten-with-new-addresses-and-pointers}


#### bad {#bad}

<!--list-separator-->

-  can accidently destroy os

<!--list-separator-->

-  no privacy

<!--list-separator-->

-  cannot move after being placed?


### Dynamic Relocation {#dynamic-relocation}


#### [MMU]({{< relref "20211101144512-memory_management_unit.md" >}}) dynamically changes process address every reference {#mmu--20211101144512-memory-management-unit-dot-md--dynamically-changes-process-address-every-reference}


#### needed to be supported by hardware {#needed-to-be-supported-by-hardware}

<!--list-separator-->

-  privileged mode, OS is running, can manipulate MMU

<!--list-separator-->

-  User mode: User process is running, translates between


####  {#}


### Segmentation {#segmentation}

Basically, we are extending RAM to hold large programs in secondary memory
the process of this is, all the data is stored in Vmem, a memory map tells where the data is located (ram vs secondary). if ram, gucci, if secondary, data is loaded into RAM, then put back

Demand paging is loading a page from secondary storage on demand, and the hardware implementation knows if a page is in sec memory based on the invalid bit.

When data is not in ram, (invalid bit), you get a page fault. Then you fetch the data, and restart the operation.

[Address Space]({{< relref "20211101144736-address_space.md" >}})