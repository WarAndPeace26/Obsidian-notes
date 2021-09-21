%% [[Lectures]]%%
# Connecting Devices
![[Pasted image 20210920225817.png]]
### Repeater
***
No filtering capability
### Bridge (AKA Transparent/Learning Bridge )
***
1. Layer 2 device
2. Can read source-dest mac address. 
3. Has filtering ability
4. Reaches up to data-link layer

Maintains a Bridge table.
![[Pasted image 20210920230159.png]]
```ad-attention
title: No changes

A bridge doesn't change anything on the frame unlike routers. 
That's why bridges are called *transparent* bridges

```

#### Learning bridge
***
![[Pasted image 20210920230614.png]]

When a bridge receives a packet it checks the source address and adds it to the table. And then if the destination address is not on its table, it broadcasts the data. 

All invalid destinations discard it.

A bridge learns only from source addresses
##### Looping Problem
![[Pasted image 20210920231044.png]]


## VLAN
Main motivation -> ***Security***