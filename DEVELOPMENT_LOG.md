# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [March 27, 2026, 10:00 AM]
**What I did**:Set up the project and understood the basic structure of the code.

**Details**: 
-Created GitHub account with university email
- Changed student ID on line 92 to my actual ID (445052278)
- Reviewed the assignment instructions
- Ran the program to make sure it works
  
**Challenges**: I had difficulty understanding how the Process class works with threads.

**Solution**: I read the code step by step and followed how execution moves from main to the process.

**Time spent**: 45 min  

---

### Entry 2 - [March 27, 2026, 6:00 PM]
**What I did**: Studied how Round Robin scheduling is implemented in the code.

**Details**:
-Analyzed how time quantum is used
-Observed how processes move in the ready queue
-Understood how remaining time is updated
-Followed how threads are executed

**Challenges**: I was confused about why a new thread is created each time the process returns to the queue.

**Solution**: I learned that a thread cannot be restarted after finishing, so a new thread must be created.

**Time spent**: 40 min

---

### Entry 3 - [March 28, 2026, 5:00 PM]
**What I did**: Implemented Feature 1 (Priority).

**Details**: 
- Added a priority variable to the Process class
-Assigned random priority values from 1 to 5
-Updated the constructor
-Displayed priority when adding processes to the queue
**Challenges**: 
I wanted to add priority without affecting the scheduling order.
**Solution**: 
I kept Round Robin unchanged and used priority only for display purposes.
**Time spent**: 40 min 

---

### Entry 4 - [March 29, 2026, 7:30 PM]
**What I did**: 
Implemented Feature 2 
**Details**: 
 -Added a counter variable
 -Increased it every time a new process starts
 -Displayed total context switches at the end

**Challenges**: 
I was unsure where exactly to increment the counter.
**Solution**: 
I placed it inside the main scheduler loop before starting each process.
**Time spent**: 30 min 

---

### Entry 5 - [March 3, 2026, 5:30 PM]
**What I did**: Implemented Feature 3 
**Details**:
-Added variables to track waiting time
-Calculated waiting time before each process runs
-Stored completed processes
-Created a summary table
-Calculated average waiting time

**Challenges**: Waiting time needed to be accumulated across multiple queue entries.

**Solution**: I updated waiting time every time the process starts and tracked last ready time.

**Time spent**: 60 min 

---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary

**Total time spent on assignment**: [3 hours and 35 min ]

**Most challenging part**: 
The most challenging part was understanding how multithreading works with the scheduler, especially how processes move between execution and waiting states. It was also difficult to calculate the waiting time correctly since each process can enter the ready queue multiple times, which required careful tracking and updating.

**Most interesting learning**: 
The most interesting part was learning how Round Robin scheduling works in practice and how threads can simulate CPU behavior. I also found it interesting to see how context switching happens and how waiting time affects the performance of processes.


**What I would do differently next time**: 
Next time, I would spend more time understanding the base code before starting implementation. I would also plan the features earlier and divide the work more clearly, which would make the development process smoother and faster.
