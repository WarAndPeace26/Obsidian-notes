%% tags: #subsections%%
# IPv4 Intro
***
IP (Internet Protocol) is a **Best effort delivery service** which is 
1. [[Connectionless]]
2. unreliable.

#### Best effort
***
It means that the IP packets can be 
- corrupted
- lost
- arrive out of order
- be delayed and
- may create **congestion** for the network

#### Ensuring IP Reliability
***
To ensure reliability, IP is often paired with reliable protocols such as TCP. 

```ad-note
title: Post Office Analogy

Post offices are best effort delivery services. In the event of a failure, the post office does not keep track of the failure. 

It is up to the sender or the would-be recipient to 
- discover the loss and 
- rectify the problem 
```

#### Datagrams
***
As IP is a connectionless protocol for a packet switching network, it uses the Datagram approach.

This means that
- Each Datagram is handled separately
- They can follow a different route to the destination
	- This, however, implies that the Datagrams sent from the same source to the same destination may arrive out of order.


```ad-attention
title: Data Corruption

The Datagram approach may cause the data to be corrupted but IP relies on higher-level protocols to take care of these problems

```
