# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer: I discovered that numerous jobs can execute simultaneously within the same application thanks to multithreading. Because all threads share the same memory space and each represents a distinct path of execution, communication between them is accelerated.

Additionally, I learnt about the various stages that a thread might be in during execution, including New, Runnable, Running, Waiting, and Terminated. This made it easier for me to comprehend how the CPU handles several threads.

The way scheduling algorithms like Round-Robin regulate thread execution order is another crucial idea I learned. Despite the fact that there are several threads, they share the CPU according to time slices.**

[Write your answer here. Discuss specific concepts like thread creation, thread states, how threads execute concurrently, what surprised you, etc.]

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer: Correctly implementing the Round-Robin scheduling algorithm was the most difficult aspect of this project. Although the concept is straightforward, it took considerable attention to manage the ready queue and make sure processes are correctly re-added.

Additionally, tracking the execution path through the output was challenging, particularly when numerous processes were continuously switching. It was occasionally difficult to understand when a process should go to the end of the queue.**

[Describe the specific challenge. Was it understanding the code? Implementing a feature? Using Git? Explain what made it difficult and how it relates to the course concepts.]

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer: I overcome these difficulties by decomposing the issue into manageable chunks. Prior to using the scheduling notion in code, I concentrated on comprehending it.

Additionally, I employed debugging strategies like reporting the ready queue's condition following each operation. This made it easier for me to see when processes were re-queued and how they moved.

I also went over lesson materials and examples, which strengthened my comprehension and helped me fix implementation errors.**

[Describe your problem-solving approach. Did you read documentation? Ask for help? Debug systematically? What resources did you use? What strategies worked?]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer: Many real-world applications use multithreading, such as web browsers, where multiple threads manage background operations, user interaction, and page loading concurrently.

It is also utilized in games, where threads concurrently handle user input, physics computations, and visual rendering. Both performance and user experience are enhanced by this.

I gained a better understanding of how scheduling impacts performance and how threads can be used to effectively handle several activities thanks to this project.**

[Give specific examples from real applications you use (web browsers, games, mobile apps, etc.). Explain why threads are useful in those scenarios. Connect to what you learned in this assignment.]

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?
I feel confident in understanding basic multithreading concepts such as thread creation, execution, and scheduling. However, I still need more practice with advanced topics like synchronization and concurrency issues.
[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
