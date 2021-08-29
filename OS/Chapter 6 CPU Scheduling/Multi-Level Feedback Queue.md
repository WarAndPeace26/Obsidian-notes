# Multilevel Feedback Queue
***
In [[Multi-level Queue Scheduling]], the processes are assigned to their queues permanently. In Multilevel feedback queue, however, the processes can jump queue to queue

## Quirks
1. If a process uses too much CPU time, it'll be sent to a lower-priority queue. This leaves I/O-bound and interactive processes in the higher priority queues.
2. If a process waits too long in a lower priority queue, it'll be moved up.

## Example 
![[Pasted image 20210824182349.png]]

1. A process entering the ready queue is given a time quantum of 8 milliseconds or less. If it does not finish within this time, it will be moved to the tail of queue 1.
2. If queue 0 is empty, the process at the head of queue 1 is given a quantum of 16 ms. If it does not completed. It is *Preempted* and moved to queue 2.
3. Queue 2 is run on an FCFS basis but only when Q0 and Q1 are empty.
4. Long processes automatically sink to queue 2 and are served in FCFS order.

### Parameters
***
- Number of Queues
- Scheduling Algorithm for each queue
- Upgrading to higher priority method
- Demotion method
- The process to determine which queue a process will enter when that process needs service.