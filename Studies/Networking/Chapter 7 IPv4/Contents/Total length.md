# Total Length
***
This field is 16 bit and contains the length of the whole Datagram (Not just the header)

```ad-attention
title: Length of Data

Length of Data = Total Length - Length of Header (Hlen x 4)

```

This field also tells the processor whether there's padding there in the datagram or not.
 ![[Pasted image 20210904150846.png]]

```ad-info
title: Ethernet Protocol Size Restriction

Ethernet protocol has a restriction on the minimum and maximum size of data that can be encapsulated in a frame (46 - 1500 bytes)

```
