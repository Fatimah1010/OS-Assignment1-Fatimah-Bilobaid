# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer: A process is a stand-alone program that is running and has its own memory and system resources. It is more secure because each process operates independently of the others, but it is also more costly to create and maintain.

In contrast, a thread is a smaller execution unit that shares memory and resources with other threads in the same process. Because of this, threads can be created and switched between more quickly than processes.

The primary distinction is that threads share memory, whereas processes are segregated. This makes it possible for threads to communicate more effectively, but it also necessitates careful synchronization to prevent problems.

The simulation in this assignment operates within a single program and necessitates the usage of threads rather than processes Because the simulation operates within a single program and necessitates shared access to data structures like the ready queue, threads were employed in place of processes in this assignment. By lowering overhead, the scheduling simulation becomes more effective and manageable.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer: A process in Round-Robin scheduling is pushed to the end of the ready queue to wait for its next turn if it does not complete within its time quantum. This guarantees equity and permits the advancement of all procedures.**

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
```
▶ P1 executing quantum [5000ms]
⏸ P1 completed quantum 5000ms │ Overall progress: 73%
   Remaining time: 1769ms
↻ P1 yields CPU for context switch

➕ P1 added to ready queue │ Burst time: 6769ms | Priority: 5
```

**Explanation of example:**
P1 began running with a quantum of 5000 ms but failed to complete its 6769 ms total burst period. It was placed at the end of the ready line once the quantum was finished. When P1 reaches the front of the queue, it will execute once more, allowing P2, P3, and P4 to use the CPU equitably before P1 restarts.

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**
New:
Process P1 is in the New state when it is created but has not started execution yet. In the output, this corresponds to the line:
➕ P1 added to ready queue │ Burst time: 6769ms | Priority: 5

At this point, the thread exists but has not been scheduled.

Runnable:
P1 enters the Runnable state when the scheduler is ready to execute it. In the ready queue snapshot:
┌─ Ready Queue ──────────────
│ [P2 → P3 → P4 → ... → P1]

P1 is now waiting for CPU allocation, ready to run.

Running:
P1 is Running when the CPU executes its quantum. From the output:
▶ P1 executing quantum [5000ms] 
⏸ P1 completed quantum 5000ms │ Overall progress: 73%
Remaining time: 1769ms

This shows P1 actively using CPU cycles.

Waiting:
P1 is in Waiting when it yields the CPU after completing a quantum but still has remaining time. From the output:
↻ P1 yields CPU for context switch
➕ P1 added to ready queue │ Burst time: 6769ms | Priority: 5

Here, P1 waits in the ready queue until its next turn.

Terminated:
P1 reaches Terminated state when it finishes all remaining burst time. From the output:
▶ P1 executing quantum [1769ms] 
⏸ P1 completed quantum 1769ms │ Overall progress: 100%
Remaining time: 0ms
✓ P1 finished execution!

This indicates that P1 has fully completed execution and is removed from the ready queue.

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: Web server

**Description**: A web server manages several client requests concurrently. A different thread can handle each request.


**Why Round-Robin works well here**: Round-Robin makes sure that each client request receives an equal amount of CPU time. This increases responsiveness and stops one request from obstructing others. It is particularly helpful when numerous people are using the server at once.


### Example 2: operating System Task scheduling

**Description**: Scheduling algorithms are used by operating systems to handle several running applications, such as background processes, audio players, and browsers.


**Why Round-Robin works well here**: By allocating a predetermined time slice to each activity, Round-Robin ensures fairness. This guarantees that all applications stay responsive and that no process starves. It is appropriate for time-sharing systems since it is straightforward and predictable.


---

## Summary

**Key concepts I understood through these questions:**
1. The distinction between processes and threads
2. How operations are managed by Round-Robin scheduling
3. The thread's life cycle and states
   

**Concepts I need to study more:**
1. Synchronization of threads
2. Race situations and deadlocks 
