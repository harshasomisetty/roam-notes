+++
title = "Fork and Exec Sys Calls"
author = ["Harsha Somisetty"]
tags = ["Operating", "Systems", "System", "Calls"]
draft = false
+++

## Fork and Exec System Calls: executes new programs {#fork-and-exec-system-calls-executes-new-programs}


### Fork {#fork}


#### creates a new seperate dubplicate process, from the point of execution in the program,  has a totally new pid {#creates-a-new-seperate-dubplicate-process-from-the-point-of-execution-in-the-program-has-a-totally-new-pid}


#### PROBLEM: if thread in a multithreaded process calls fork, does all threads in procress get duplicated, or just the current thread? {#problem-if-thread-in-a-multithreaded-process-calls-fork-does-all-threads-in-procress-get-duplicated-or-just-the-current-thread}

<!--list-separator-->

-  Unix has 2 versions of fork, you can choose.

<!--list-separator-->

-  if exec is called right after fork, then since the entire process gets replaced anyway, only choose to fork the single thread

<!--list-separator-->

-  if exec is not called, then you could duplicate all the threads if you want, but again only if you want to


#### Fork returns pid of child, and 0 if it is the child process {#fork-returns-pid-of-child-and-0-if-it-is-the-child-process}

<!--list-separator-->

-  the new process has identical but seperate address spaces, so all the previous variables and data are replicated, but data now changes seperately

    <!--list-separator-->

    -  [good link for more info](https://www.csl.mtu.edu/cs4411.ck/www/NOTES/process/fork/create.html)

        ```C
        #include <stdio.h>
        #include <sys/types.h>
        #include <unistd.h>

        int main(){
          fork();
          fork();
          fork();
          printf("hey harsha! PID = %d\n", getpid());
          }
        ```

<!--list-separator-->

-  The parent needs to know child id (since it can have multiple children) so it can wait on the right process

<!--list-separator-->

-  The child only has one parent, which is eaisly identifiable through the context


### Exec: {#exec}


#### program in parameter replaces the rest of the original process, has the same pid {#program-in-parameter-replaces-the-rest-of-the-original-process-has-the-same-pid}


#### when exec is called, entire process gets replaced {#when-exec-is-called-entire-process-gets-replaced}