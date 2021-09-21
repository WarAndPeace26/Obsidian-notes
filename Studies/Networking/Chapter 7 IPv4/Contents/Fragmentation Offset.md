# Frag Offset
***
![[Pasted image 20210905013329.png]]

```ad-attention
title: Value of Frag Offset

Remember that the value of the offset is measured in units of 8 bytes. 

This is done because the length of the offset field is only 13 bits long and cannot represent a sequence of bytes **greater than 8191**. This forces hosts or routers that fragment datagrams to choose the size of each fragment so that the first byte number is divisible by 8.
```
![[Pasted image 20210905013651.png]]