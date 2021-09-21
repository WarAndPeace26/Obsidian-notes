%%tags: #subsections %%
# Datagrams
***
## Intro
***
Packets in the network layer are called **Datagrams**.
They are 
- Variable length
	- 20-60 **bytes**
- Contains information essential to Routing and Delivery

![[Pasted image 20210904134333.png]]


### Fields of the Datagram
***
1. First level 32 bits (4 bytes)
	1. [[Version (Ver)]] 4 bits
	2. [[ Header Length (Hlen)]] 4 bits
	3. [[Service Type]] 8 bits
	4. [[Total length]] 16 bits
2. Second Level 32 bits
	1. [[Identification]] 16 bits
	2. [[Flags]] 3 bits
	3. [[Fragmentation Offset]] 13 bits
3. Third Level 32 bits
	1. [[Time to Live]] 8 bits
	2. [[Protocol]] 8 bits
	3. [[Header Checksum]] 16 bits
