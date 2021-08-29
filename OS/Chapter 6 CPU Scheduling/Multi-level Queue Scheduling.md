# Multilevel Queue Scheduling
***
For when processes are easily classified into groups. A common classification is
- Foreground (Interactive) processes
- Background (Batch) processes

They have different response-time requirements and thus different scheduling needs.

## The Multilevel Queue
The Ready Queue is partitioned into several separate queues based on:
- Memory Size
- Process priority
- Process type

```ad-attention
title: Separate Queues

***Each queue has its own scheduling algorithm.***

While the Background queue follows the FCFS algorithm, the foreground queue may follow RR

```
![[Pasted image 20210824181210.png]]
```ad-attention
title: Precedency

Each queue, however, has absolute priority over its lower queue. No process in the interactive Queue would get any CPU time unless System processes was completely empty.

Another possibility, however, is time slicing. The foreground processes could get 80% of the CPU time while the Background processes get 20%.

```
