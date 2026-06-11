The basic concepts here are:
Grid
 └─ Block
      └─ Thread
### Thread
This is the smallest unit of execution.
```
Thread 0
Thread 1
Thread 2
```
### Block
This is a group of threads.
```
 Block
      └─ Thread 0
      └─ Thread 1
      └─ Thread 2
      └─ Thread 3
```
### Grid
This is a collection of blocks.
```
 Grid
      └─ Block 0
      └─ Block 1
      └─ Block 2
      └─ Block 3
```

---
## Memory Hierarchy
CUDA memory is critical for performance
`GPU Memory`
`│`
`├─ Global Memory`
`├─ Shared Memory`
`├─ Constant Memory`
`└─ Registers`
Speed comparison:
`Registers      Fastest`
`Shared Memory`
`Global Memory  Slowest`