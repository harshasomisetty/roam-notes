+++
title = "Physical Networking Devices"
author = ["Harsha Somisetty"]
tags = ["CS", "Tech", "Networking"]
draft = false
+++

## Cables: made of either copper or fiber, transfer bits, etc {#cables-made-of-either-copper-or-fiber-transfer-bits-etc}


### Copper made of either 5 or 6 twists, (Cat5 or Cat6), affects speed and resistance . {#copper-made-of-either-5-or-6-twists--cat5-or-cat6--affects-speed-and-resistance-dot}


#### 5e replaced 5 to reduce crosstalk to reduce data interference, less data needs to be retransferred {#5e-replaced-5-to-reduce-crosstalk-to-reduce-data-interference-less-data-needs-to-be-retransferred}


#### 6 is much faster, but less masimum distance {#6-is-much-faster-but-less-masimum-distance}


### Fiber transfer pulses of lights to transfer data, fragile, trasnfer overs long distances, resistant to EM interference {#fiber-transfer-pulses-of-lights-to-transfer-data-fragile-trasnfer-overs-long-distances-resistant-to-em-interference}


## Hubs and Switches {#hubs-and-switches}


### Hub allows for connections from many computers at once (all devices talks to everyone, individuals choose to ignore data) {#hub-allows-for-connections-from-many-computers-at-once--all-devices-talks-to-everyone-individuals-choose-to-ignore-data}


#### **Collision Domain** network degment where only one device can talk at a time (if multple talk, then too much interference, slows down) {#collision-domain-network-degment-where-only-one-device-can-talk-at-a-time--if-multple-talk-then-too-much-interference-slows-down}


#### This is why its rare {#this-is-why-its-rare}


### Switches are a layer 2 device, can inspect contents of ethernet protocol, and only send the data to the indented device (hgiher througput) {#switches-are-a-layer-2-device-can-inspect-contents-of-ethernet-protocol-and-only-send-the-data-to-the-indented-device--hgiher-througput}


## connect devices over Local Area Network (LAN) {#connect-devices-over-local-area-network--lan}


## Routers: device that forwards data between independent networks (layer 3), can inspect IP data to see where to send thigns {#routers-device-that-forwards-data-between-independent-networks--layer-3--can-inspect-ip-data-to-see-where-to-send-thigns}


### store internat data to transfer data all over the world {#store-internat-data-to-transfer-data-all-over-the-world}


### routers for home devices have a very minimal routihn table (from local home to ISP, then ISP's router takes over for the entire world) {#routers-for-home-devices-have-a-very-minimal-routihn-table--from-local-home-to-isp-then-isp-s-router-takes-over-for-the-entire-world}


### Boundary Gateway Protocol - most optimal path to send data to each other for big ISP routers {#boundary-gateway-protocol-most-optimal-path-to-send-data-to-each-other-for-big-isp-routers}


## Servcrs and clients - former gives data, clients requests data (both nodes and individual laptops can be either) {#servcrs-and-clients-former-gives-data-clients-requests-data--both-nodes-and-individual-laptops-can-be-either}