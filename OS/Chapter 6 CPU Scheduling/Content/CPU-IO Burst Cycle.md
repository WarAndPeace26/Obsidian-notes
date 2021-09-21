# CPU-I/O Burst Cycle
***

Process execution consists of a **cycle** of CPU execution and I/O wait.
> Process execution begins with a CPU Burst
> Followed by an I/O burst

![[Pasted image 20210824004429.png]]

## Duration of Bursts
![[Pasted image 20210824004635.png]]

- An I/O bound program typically has many short CPU bursts
- A CPU bound program has a few long CPU bursts.

Important in picking the right CPU-scheduling algorithm.
=