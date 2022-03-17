# Lec 2
***
## Endian
![[Pasted image 20220210222223.png]]
![[Pasted image 20220210222700.png]]
![[Pasted image 20220210223656.png]]

## Swap
![[Pasted image 20220210224316.png]]
**In step 1,**
```ad-attention
title:
Those that are common will become 0 in *y. The others are 1.
```
**In step 2,**
```ad-attention
title:
The 0's in y represent common. Therefore, they don't need to be changed. So, the 0's in x will XOR into x as they are corresponding with 0's in y. The 1's will XOR into 1 as they correspond to 0's in y.
```
**In step 3,**
```ad-attention
title:
Again, the common one's will follow x's bits as they are 0. The uncommon one's will flip x's bits and become to opposite bit
```

### Array swap
![[Pasted image 20220210231802.png]]
![[Pasted image 20220210231825.png]]

### Question
![[Pasted image 20220210231930.png]]
![[Pasted image 20220210232018.png]]

## Bitwise
![[Pasted image 20220211000408.png]]
```ad-note
title:
!(x^y)
```

### Shift operations
![[Pasted image 20220211000506.png]]

## Integer Representation
```ad-attention
title: Unsigned

![[Pasted image 20220211000702.png]]

```
```ad-attention
title: Signed

![[Pasted image 20220211000741.png]]

```

## Casting
### Any operand unsigned, all Unsigned

![[Pasted image 20220211015256.png]]
![[Pasted image 20220211015649.png]]

### Conversion
![[Pasted image 20220211020144.png]]
![[Pasted image 20220211020202.png]]
![[Pasted image 20220211020216.png]]
![[Pasted image 20220211020225.png]]
![[Pasted image 20220211020310.png]]
![[Pasted image 20220211020320.png]]

### Truncation
![[Pasted image 20220211020402.png]]
![[Pasted image 20220211020411.png]]