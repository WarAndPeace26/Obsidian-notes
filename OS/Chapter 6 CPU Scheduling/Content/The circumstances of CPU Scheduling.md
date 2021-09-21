# Preemptive Scheduling
The circumstances for CPU Scheduling are:
1. When a process switches from the running state to waiting state.
2. Running state to Ready state
3. Waiting to Ready State
4. Process Terminates.


### Nonpreemptive/Cooperative Scheduling Scheme
***
When scheduling takes place on the situations 1 and 4.
It does not require special hardware (e.g. a Timer)

### Complication with Preemption
***
During the procession of a system call, the kernel may be busy with an activity. Such activities may involve changing important Kernel Data.

What happens if the process is preempted in the middle of these changes and the kernel (Or device driver) needs to read or modify the same structure?

Most versions of UNIX deals with this problem by waiting either for a system call to complete or for an I/O block to take place before doing a [[Context Switch]]. But this **Kernel-Execution** method is bad for real time computing.


### Real Time Solution
***

Because interrupts can occur any time, the sections of code affected by interrupts must be guarded from simultaneous use.
Not accepting interrupts at all times may cause:
- Lost input
- Output overwritten
So that these sections of code are not accessed concurrently, they disable Interrupts upon entry and re-enable them at exit.
```ad-note
title: Characteristics of Interrupt Disabling Codes

These sections of codes contain few instructions and don't occur very often

```
