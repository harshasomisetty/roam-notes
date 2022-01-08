+++
title = "Border Gateway Protocol"
author = ["Harsha Somisetty"]
tags = ["CS", "Tech", "Networking"]
draft = false
+++

## Random class notes {#random-class-notes}


### local attribute protocol, takes pref over path?? {#local-attribute-protocol-takes-pref-over-path}


### MED value, if you have 2 AS paths, cna make other traffice go through path with less {#med-value-if-you-have-2-as-paths-cna-make-other-traffice-go-through-path-with-less}


#### only applies if you ae a transit autonomous system {#only-applies-if-you-ae-a-transit-autonomous-system}


#### LOCAL PREFERENCE, DEPENDS on POLICY {#local-preference-depends-on-policy}


### <span class="org-todo todo TODO">TODO</span> Next hop for intrabgp router {#next-hop-for-intrabgp-router}


### <span class="org-todo todo TODO">TODO</span> bunch of rules of of BGP decision process? decision for What {#bunch-of-rules-of-of-bgp-decision-process-decision-for-what}


### TTL count drops packets automatically, but doesn't happen in an interior AS because packets are sent as annouuncmebents {#ttl-count-drops-packets-automatically-but-doesn-t-happen-in-an-interior-as-because-packets-are-sent-as-annouuncmebents}


#### to avoid, need to be fully connected to (one one forward), but many links would be needed, so you use a router refected lmfao {#to-avoid-need-to-be-fully-connected-to--one-one-forward--but-many-links-would-be-needed-so-you-use-a-router-refected-lmfao}

<!--list-separator-->

-  this created a multirooted tree, which apparently stops announcement


## BGP is the core algorithm behind the internet {#bgp-is-the-core-algorithm-behind-the-internet}


### Different ASes (nodes) have their own internal routing, but they connect to each other with this path vector algorithm {#different-ases--nodes--have-their-own-internal-routing-but-they-connect-to-each-other-with-this-path-vector-algorithm}


#### Goal is for nodes to exchange reachabiliyt information between each other {#goal-is-for-nodes-to-exchange-reachabiliyt-information-between-each-other}


#### Nodes send Updates (advertise a new/updated path towards a prefix) and Withdraws (indicating a previous prefix is unreachable) {#nodes-send-updates--advertise-a-new-updated-path-towards-a-prefix--and-withdraws--indicating-a-previous-prefix-is-unreachable}

<!--list-separator-->

-  a Path or route contains reachable destinations in a IP Prefix (

<!--list-separator-->

-  Also contains attributes of paths which lists the AS numbers the current message has already passed AS_PATH


## Problems {#problems}


### Lots of these messes causes high CPU load on smaller routers, causes many failures {#lots-of-these-messes-causes-high-cpu-load-on-smaller-routers-causes-many-failures}


### Path vectors causes Path exploration problme when route becomes unavailable {#path-vectors-causes-path-exploration-problme-when-route-becomes-unavailable}


#### This requires BGP Converge, "Routers may advertise paths that they consdier valid although they are also affect by the failure [citation](https://link.springer.com/content/pdf/10.1007%2F978-3-642-01399-7_39.pdf) {#this-requires-bgp-converge-routers-may-advertise-paths-that-they-consdier-valid-although-they-are-also-affect-by-the-failure-citation}


## Routing Dynamic {#routing-dynamic}


### The flow of exchange of information between routers, irregular dynamics cause the problems above {#the-flow-of-exchange-of-information-between-routers-irregular-dynamics-cause-the-problems-above}


#### Dynamics include normal BGP stuff, and those that results from BGP problems {#dynamics-include-normal-bgp-stuff-and-those-that-results-from-bgp-problems}


#### Basically actions that BGP does {#basically-actions-that-bgp-does}


### Classification {#classification}


#### AADiff {#aadiff}

<!--list-separator-->

-  An alterantive route is announced right after a primary route is announced


#### WADiff {#wadiff}

<!--list-separator-->

-  After a route to dest is withdrawn, a different route to same dest is announced


#### WADup (Error) {#wadup--error}

<!--list-separator-->

-  After a route to dest is withdrawn, same route is reannounced

    <!--list-separator-->

    -  caused by topological failure, or pathological oscillation


#### WWDup (Error) {#wwdup--error}

<!--list-separator-->

-  After route is withdrawn, it is withdrawn again


#### AADup {#aadup}

<!--list-separator-->

-  Type 1 (pathological)

    <!--list-separator-->

    -  After a route is announced, the same exact route is reannounced

        <!--list-separator-->

        -  Not expected since BGP is an incremental protocol

<!--list-separator-->

-  Type 2

    <!--list-separator-->

    -  Like Type1, but some small atribute is difference, reflecting a routing policy change