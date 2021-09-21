# Header Length
***
The length of a header goes from 20-60 bytes. The highest 4 bits can get is 15. 

**So the value is taken multiplied by 4.**

```ad-attention
title: Header Length Calculation

For a header with the length of 20, the Hlen field will be 5 (0101)

For a header with the length of 60, the Hlen field will be 15 (1111)

```
