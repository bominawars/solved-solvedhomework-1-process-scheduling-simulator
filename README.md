Download Link: https://assignmentchef.com/product/solved-solvedhomework-1-process-scheduling-simulator
<br>
SpecificationsYou are to simulate the execution of processes by a cheap tablet with a large memory (assume all processes can fit in memory concurrently), one touch screen display, a dual core CPU and one solid-state drive (SSD). Each process will be described by its start time followed by a sequence of resource requests. The resources requested will include the CPU (CPU), SSD requests (SSD) and touch screen input/output requests (INP). The input to your program will be a sequence of (request, time) pairs where all times will be expressed in milliseconds. Your program should read input from a file named input.txt located in the same working directory as the program itself.NEW 100 // New process (P0) with start time 100msCPU 5 // P0 requests CPU for 5msINP 5 // P0 requests I/0 which will take 5msCPU 5 // P0 requests CPU for 5msNEW 105 // New process (P1) with start time 105msCPU 5 // P1 requests CPU for 5msYou can assume there will be no more than 150 pairs and 25 total processes in any file.You can also assume that memory is large enough to hold all the processes and that context switching times can be ignored.CPU Scheduling: Your program should have a single ready queue. That queue should be a FIFO queue and should keep all processes ordered according to their queue arrival time in a first come first served order.SSD: SSD scheduling should be done on a first come first served basis.If multiple requests are made at the same time you should allocate (1) CPU, (2) SSD, and (3) INPI/O: Assume that processes never have to wait for the touch screen to become available. However, they cannot be also using a processor or the SSD while handling an I/O event (the process must wait until the I/O is complete)Your program should have one process table that keeps track of all the processes currently in the system. The process states available are: RUNNING = currently executing on a CPU READY = waiting for a CPU allocation (in the ready queue) WAITING = waiting for INPUT or SSD to finish (or to become available) FINISHED = process has finished executingEvery time a process starts, changes state or terminates, your program should print:a) The current simulated time in millisecondsb) The states for each process in the process table as well as some information about the current (command) location in each processWhen all the processes in your input file have completed your simulator should print a summary report, containing:a) The total number of processes that have completedb) The total number of SSD accessesc) The average duration of an SSD access (including the wait time in the SSD queue)d) The total time elapsed since the start of the first processe) The CPU utilization, that is, the average number of busy cores (between zero and two)f) The SSD utilization, that is, the fraction of time the device was busy (between zero and one)Write Up(1) Draw the state transition diagram for the tablet you are modeling. Make sure you include all possible transitions(2) Draw (a) diagram(s) of the major structures (queues, arrays, etc) that your group is using to keep track of the different devices and processes. Explain briefly the role of each structure, how you decided on its configuration, and how it is used in the program(3) Explain (using a diagram if necessary) how your group chose to represent a process. What information do you store on each process and why?(4) What were the major stumbling blocks your group encountered while working on this project? What were the most difficult design decisions to make? Write a 2-3 paragraph reflection on the process of developing this program.Sample Output (not showing summary data)(Please note, this is for informational purposes only. Your output may differ, and may be formatted differently)INPUT FILENEW 100CPU 5INP 5CPU 5NEW 105CPU 5OUTPUTTime = 0PROCESS 0: Current State = READY, Next Index = 0PROCESS 1: Current State = READY, Next Index = 4Time = 100PROCESS 0: Current State = RUNNING, Next Index = 2PROCESS 1: Current State = READY, Next Index = 4Time = 105PROCESS 0: Current State = WAITING, Next Index = 3PROCESS 1: Current State = RUNNING, Next Index = 6Time = 110PROCESS 0: Current State = RUNNING, Next Index = 4PROCESS 1: Current State = FINISHED, Next Index = 6Time = 115PROCESS 0: Current State = FINISHED, Next Index = 4PROCESS 1: Current State = FINISHED, Next Index = 6