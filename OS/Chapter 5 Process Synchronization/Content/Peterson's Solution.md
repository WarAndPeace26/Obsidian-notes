# Peterson's Solution
***
#### Attribute
***
1. Software based
2. Not scalable; works for only two processes.
3. Assumes that LOAD and STORE are **Atomic** instructions hence cannot be interrupted.
4. The shared variables are 
	1. **int** turn
		- Indicates whose turn it is to enter CS
	2. **Boolean** flag[2]
		- if flag[i] is true, then Pi is ready to enter CS.

#### The Solution
***

![[Pasted image 20210911234052.png]]
```ad-attention
title: Flags and Turns
Flag[1] = true can mean that process 1 is executing. Hence if flag 1 is true, we check the turn.

Each turn points at the other process. So if the turn is 1 and flag[1] is true, it means that the last process to change the turn was process 0. That can mean that process 1 is currently being executed.
```

