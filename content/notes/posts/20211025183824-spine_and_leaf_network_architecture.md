+++
title = "Spine and Leaf Network Architecture"
author = ["Harsha Somisetty"]
tags = ["Networking"]
draft = false
+++

## A horizontally scaling efficent way of compute and bandwith for data centers {#a-horizontally-scaling-efficent-way-of-compute-and-bandwith-for-data-centers}

Have server pods of computers and rack switches
the rack switches connect to spine switches.

every leaf is connected to every spine, and the converse. This minimizes bottlenecks and latency, and easy to fix errors.
to increase bandwith, just add another spine, to increase capacity, add another pod.