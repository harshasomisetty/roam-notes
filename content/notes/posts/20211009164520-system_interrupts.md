+++
title = "System Interrupts"
author = ["Harsha Somisetty"]
tags = ["Operating", "Systems"]
draft = false
+++

## Constant interrupts to manage all programs {#constant-interrupts-to-manage-all-programs}


### i/o or hardware interrupts {#i-o-or-hardware-interrupts}

normal completion or error


### Program Exception {#program-exception}

unusual condition


### Timer Interrupts {#timer-interrupts}

automatic interrupting for better scheudling, since if process is running, OS is not running


#### force context swtiching and timesharing {#force-context-swtiching-and-timesharing}

queue maintains all programs running, every process gets a slice of spu (all in scheduing)


#### poll Hardware and Bookeeping {#poll-hardware-and-bookeeping}


### Hardware Failure {#hardware-failure}


### Software Interrup {#software-interrup}

illegal instructions (faulting or aporting), signals to another process