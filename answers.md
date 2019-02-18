# Assignment 8: Scheduling  
*Author: Feck-Melzer  
 Class: 3AHIF   
 Answers for Assignment 8: Scheduling*

#### Answer 1
  | needs 30 Quanta to complete|
  |---|---|---|---|---|
  |  Run  | 1  |  2 | 3 | 4 | 5 |
  | Quanta | 1  | 2  |  4 |  8 | 15 |
  |  Acc | 1  | 3  | 7  | 15  | 30 |

    At run 5 the acc reaches a value above 30, wich tells us the process has to be swapped 5 times
    before it runs at all.
#### Answer 2

| Process Name | 1st run | 2nd run | 3rd run | 4th run |
| -- | -- | -- | -- | -- |
| A | 50 msec | 150 msec | 300 msec | 85 msec |
| B | 300 msec | 150 msec | 85 msec | 50 msec |

    Formula: T0/8 + T1/8 + T2/4 + T3/2

    for process A: 50/8 + 150/8 + 300/4 + 85/2 = 142.5ms
    for process B: 300/8 + 150/8 + 85/4 + 50/2 = 102.5ms

    The scheduler is working with the "Shortest Process Next" stragegy,
    therefore it will choose process B, wich is 40ms faster.
#### Answer 3
    CPU-Bound Processes: The "Bottleneck" of the programm/process would be the CPU, if it was faster, the
    process/programm would be faster.

    I/O-Bound Processes: The "Bottleneck" of the programm/process would be any Input/Output subsystem,
    e.g: reading data from a disk. In this case the whole process/programm would be faster, if the disk
    could be read faster.

  * If speeding up the CPU doesn't speed up your program, it may be I/O bound.

  * If speeding up the I/O (e.g. using a faster disk) doesn't help, your program may be CPU bound.

#### Answer 4

###### A system is schedulable if it holds the condition:
The sum of all (CPU-time divided through period-time P) has to be equal to or smaller than 1.

    formula: (35/50) + (20/100) + (10/200) + (x/250) <= 1   |
              0.7 + 0.2 + 0.05 + (x/250) <= 1               | - 0.95
              x/250 <= 0.05                                 | * 250
              x <= 12.5
    this shows that 12.5ms is the largest value x can have, while the system is still schedulable.
