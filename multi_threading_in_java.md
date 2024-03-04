---
title: "MultiThreading using GitHub Copilot"
description: "MultiThreading with GitHub Copilot"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## MultiThreading in java using GitHub Copilot
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### Description
Multithreading is a Java feature that allows concurrent execution of two or more parts of a program for maximum utilization of CPU. Each part of such program is called a thread. So, threads are light-weight processes within a process.

Using GitHub Copilot we can get idea about what is Multithreading in Java.
GitHub Copilot can be used to get explaination about multithreading. If you add comment as `//what is Multithreading in java`, it will give you appropriate answer to your question.
Also , we can create thread using GitHub Copilot. 

Threads can be created by using two ways : 

1. Extending the Thread class 
2. Implementing the Runnable Interface

GitHub Copilot can give you suggestion to create thread using both the ways. Also, it will give you efficient way to create thread.

#### Example
- **Exercise 1**
    ##### Input Code
    ```java
    public class Multithreading {
    public static void main(String[] args) {
        // What is Multithreading in Java
        }
    }
    ```

    ##### Result Suggested by Copilot

    ```java
    public class Multithreading {
        public static void main(String[] args) {
            // What is Multithreading in Java
            // Multithreading in Java is a process of executing multiple threads simultaneously. Thread is a lightweight sub-process, the smallest unit of processing. Multiprocessing and multithreading, both are used to achieve multitasking.
            // However, we use multithreading than multiprocessing because threads share a common memory area. They don't allocate separate memory area so saves memory, and context-switching between the threads takes less time than process.
        
            // What is the difference between Process and Thread
            // A process is a program under execution. It is an active entity, and it is heavy-weight. A thread is a subset of a process. It is a passive entity, and it is lightweight.

            // What is the difference between Multitasking and Multithreading
            // Multitasking and multithreading, both are used to achieve multitasking. Multitasking is when multiple tasks share common processing resources such as a CPU. Multithreading is when multiple threads in a process share common processing resources.
        }

    }
    ```
- **Exercise 2**
    ##### Input Code
    ```java
    public class Multithreading {
        public static void main(String[] args) {
            //Create Thread using Thread Class
        }
    }
    ```
    
    ##### Result Suggested by Copilot
    
    ```java
    public class Multithreading {
        public static void main(String[] args) {
       //Create Thread using Thread Class
        // Thread class provides constructors and methods to create and perform operations on a thread. Thread class extends Object class and implements Runnable interface.
        Thread thread = new Thread();
        thread.start();
        }
    }
    ```

