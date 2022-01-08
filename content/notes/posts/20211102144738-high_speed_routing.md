+++
title = "High Speed Routing"
author = ["Harsha Somisetty"]
tags = ["Network", "Layer"]
draft = false
+++

## Used for pushing data faster and handling traffic {#used-for-pushing-data-faster-and-handling-traffic}


## Has a forwarding table as well as routing table {#has-a-forwarding-table-as-well-as-routing-table}


### based on destination network, can quicklydetermine outgoing port Ijust keeiing prefix {#based-on-destination-network-can-quicklydetermine-outgoing-port-ijust-keeiing-prefix}


#### Need longest prefix match {#need-longest-prefix-match}


### budget for lookup is very small, inverese relted to linerate {#budget-for-lookup-is-very-small-inverese-relted-to-linerate}


### need mutex since multiple threads access the oruting table {#need-mutex-since-multiple-threads-access-the-oruting-table}

<!--list-separator-->

-  but mutex is too slow, so instread, the writing thread makes a cooy, and then chantges the pointer to the rable


### Essentially, the traffic is distributed, so each forwarding engine is not overloaded. {#essentially-the-traffic-is-distributed-so-each-forwarding-engine-is-not-overloaded-dot}


#### Each {#each}


### The only thing that the linecard does is move the packet header. It changes, atached back to packet, then send the total packet to the right port {#the-only-thing-that-the-linecard-does-is-move-the-packet-header-dot-it-changes-atached-back-to-packet-then-send-the-total-packet-to-the-right-port}


### Movement of packet is from linecard to line card {#movement-of-packet-is-from-linecard-to-line-card}


#### header is from linecard to FE, FE to FE, FE to linecard (asks range of bytes {#header-is-from-linecard-to-fe-fe-to-fe-fe-to-linecard-asks-range-of-bytes}


## GPU for faster processing {#gpu-for-faster-processing}


### Normally, you process one packet at a time, but with gpu with K cores, you can process K packets at a time {#normally-you-process-one-packet-at-a-time-but-with-gpu-with-k-cores-you-can-process-k-packets-at-a-time}