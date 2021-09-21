# The Dispatcher
The dispatcher is the **module** responsible for giving the CPU to the process selected by the [[Short-term Scheduler]]

This function involves the following:
- Switching context
- Switching to User Mode
- Jumping to the proper location in the user program to restart that program.

Dispatchers ought to be fast because they are used in ***Every*** process switch. The time it takes for the Dispatcher to stop one process and start another is known as the **DISPATCH LATENCY**.