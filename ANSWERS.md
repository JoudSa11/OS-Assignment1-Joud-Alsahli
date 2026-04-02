# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**
A process is a full program running in memory, while a thread is a smaller unit inside the process that executes tasks. Threads share the same memory, but processes have separate memory spaces. Because of that, threads are faster to create and switch between compared to processes.

In this assignment, we used threads instead of processes because they are lighter and easier to manage. Also, since all processes in the simulation share the same data structure (like the ready queue), using threads makes communication simpler.

Another difference is that creating a process takes more resources, while threads have lower overhead. Also, communication between threads is faster because they share memory, unlike processes.
[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**
In Round Robin scheduling, if a process does not finish within its time quantum, it is removed from the CPU and added back to the end of the ready queue. This allows other processes to get their turn.

In my program, after a process runs for its time quantum, if it still has remaining time, it is re-added to the queue using the method that adds it again. Then it waits until its next turn.

For example, in the output, we can see that a process runs, then prints that it is yielding the CPU, and later appears again in the queue. This shows that it did not finish and was re-queued.

This behavior ensures fairness, since all processes get a chance to execute instead of one process taking all the CPU time.
[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [When is P1 in New state?]
P1 is in the New state when the thread is created using new Thread(process), but before it starts execution.
2. **Runnable**: [When does P1 become Runnable?]
After the process is added to the ready queue, it becomes ready to run and waits for its turn, so it is in the Runnable state.
3. **Running**: [When is P1 Running?]
When start() is called on the thread, P1 begins execution and enters the Running state, where it uses the CPU for its time quantum.
4. **Waiting**: [When/why would P1 be Waiting?]
P1 goes into the Waiting state when join() is used, because the main program waits for the thread to finish. Also, during sleep(), the thread is temporarily paused.
5. **Terminated**: [When is P1 Terminated?]
When the process finishes completely and its remaining time becomes zero, the thread enters the Terminated state and does not return to the queue.
---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Operating System (CPU Scheduling)]

**Description**: 
[Describe the real-world scenario or application]
In operating systems, multiple processes need to share the CPU. The system schedules them so each process gets a chance to run.
**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]
Round Robin works well because it gives each process a fair amount of CPU time. It prevents one process from taking all the CPU. It also improves responsiveness since every process gets a turn quickly.
### Example 2: [Web Server (Handling Multiple Requests)]

**Description**: 
[Describe the real-world scenario or application]
Web servers receive many requests from users at the same time. Each request can be handled using a separate thread.
**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]
Round Robin helps in managing multiple requests fairly. Each request gets a small time to execute, so no request waits too long. This makes the system faster and more responsive for users.

---

## Summary

**Key concepts I understood through these questions:**
1. The difference between thread and process
2.  How Round Robin scheduling works using a ready queue
3. Context switching between processes

**Concepts I need to study more:**
1. Thread states in more detail
2. Waiting time calculation and how it is updated
