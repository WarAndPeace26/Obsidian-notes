# The Requirements of a CS problem Solution
***
1. Mutual Exclusion
2. Progress
3. Bounded Waiting

#### Mutual Exclusion
***
>>>> No two processes can execute their critical section at the same time
#### Progress
***
>>>> When no threads are in their critical sections and multiple processes want to get into their CSs, one will be allowed to do so
#### Bounded Waiting
***
>>>> After a thread makes a request to enter its CS, there is a limit on the number of times other threads will be allowed to enter before the request has been granted.