# Database Management Systems

## Unit 4: Concurrency Control and Advanced Databases

### Centralised Database Architecture
- Centralised database systems are those that run on a single computer and do not interact with other computer systems.
- Such database systems span from single user database systems running on personal computers to high performance database systems running on high end server systems.

- Advantages:
  - Easy to use due to the simplicity provided by storing all the data in one place.
  - Helps to maximise data integrity and minimise data redundancy.
  - Data reliability is enhanced and accuracy and consistency of data is maintained.

### Client-Server Database Architecture
- A client-server database system splits functionality between a server system and multiple client systems.
- Functionality provided by such database systems can be divided into two parts - the front end and the back end.
- The back end manages access structures, query evaluation and optimisation and concurrency control.
- The front end consists of tools such as the SQL user interface, report generation tools, and data mining and analysis tools.

### Speed-up and Scale-up
- Running a given task in less time by increasing the degree of parallelism is called speed-up. Handling larger tasks by increasing the degree of parallelism is called scale-up.
- Suppose that the execution time of a task on a larger machine is $T_L$ and the execution of the same task on a smaller machine is $T_S$. The speed-up is defined as $T_S/T_L$.
- The system is said to demonstrate linear speed-up if the speed-up is $N$ when the larger machine has $N$ times as many resources as the smaller machine. If the speed-up is less than $N$, the system is said to demonstrate sub-linear speed-up.
- Let $Q$ be a task and $Q_N$ be a task that is $N$ times larger than $Q$. Suppose that the execution time of task $Q$ on a given small machine is $T_S$, and the execution time of task $Q_N$ on a parallel machine having $N$ times the resources of the smaller machine is $T_L$. The scale-up is then defined as $T_S/T_L$.
- The parallel system is said to demonstrate linear scale-up on task $Q$ if $T_L = T_S$. If $T_L > T_S$, the system is said to demonstrate sub-linear scale-up.

### Factors affecting Speed-up and Scale-up
- **Start-up costs:** There is a start-up cost associated with initiating a process. In a parallel operation, consisting of thousands of processes, the start-up time may overshadow the actual processing time, affecting speed-up adversely.
- **Interference:** Since processes in a parallel system often access shared resources, a slowdown may result from the interference of each new process as it competes with existing processes for shared resources. This affects both speed-up and scale-up.
- **Skew:** By breaking down a single step into a number of parallel steps, we reduce the size of the average step. However, the service time of the slowest step will determine the service time of the task as a whole. It is difficult to divide a task into exactly equal sized parts, and the distribution of sizes is often skewed. This also affects both speed-up and scale-up.

### Questions Asked
1. Explain centralised and client-server architecture. (6 marks)
2. Explain advantages of centralised databases. (3 marks)
3. Why is it necessary to have a client-server architecture for database management systems? (6 marks)
4. What are the key elements of parallel processing? (6 marks)
5. Explain speed-up and scale-up issues with respect to parallelism. (8 marks)
6. Compare speed-up and scale-up. (3 marks)
7. Draw and explain the architecture of parallel databases. (8 marks)
8. Explain different issues in design of parallel system. (4 marks)
9. Explain distributed database system. Explain its advantages. (8 marks)
10. What is distributed database? Discuss the different approaches used for data storage in distributed database. (8 marks)
11. Explain characteristics and advantages of distributed database system. (3 marks)
12. Compare horizontal and vertical fragmentation. (3 marks)
13. Write a short note of data fragmentation in distributed databases. (6 marks)