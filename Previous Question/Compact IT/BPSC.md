# BPSC — Written Examination Questions

Source: BPSC.pdf | 38 Pages | Questions Only

The PDF contains multiple BPSC examination question sets. The questions are organized below by examination, with original numbering maintained. Answers and solutions are excluded.

## Exam 1: BPSC — Network/Website Manager (CSE)

Ministry of Food | Exam Date: 21 May 2025

### Question 1 — Object-Oriented Programming

Explain the concept of polymorphism in Object-oriented Programming with example.

### Question 2 — Graph Theory / Algorithm

Write an Algorithm to detect a cycle in a directed graph.

### Question 3 — Data Structure

Design a full adder using XOR and AND or gate?

### Question 4 — Operating System / Memory Management

Compare "Paging" and "Segmentation" memory management technique?

### Question 5 — Cybersecurity

What is a Man-in-The Middle (MitM) attack? How can it be prevented?

### Question 6 — C Programming / Recursion

Write a C program to find the sum of digits of an integer number using "recursion".

### Question 7 — Computer Architecture

Write down the names of different stages of instruction pipelining in a multi-cycle datapath architecture. What is a data-hazard in a pipelined datapath?

### Question 8 — Operating System / CPU Scheduling

There are 3 tasks P1, P2, and P3. The arrival time and duration of each task is given below. Apply the round-robin scheduling algorithm with quantum size = 20 to schedule the tasks in a single-core machine. Calculate the turnaround time for each task. (All tasks have the same priority.)

| Task | Arrival Time (ms) | Duration (ms) |
| ---- | ----------------- | ------------- |
| P1   | 0                 | 40            |
| P2   | 5                 | 40            |
| P3   | 10                | 20            |

### Question 9 — Computer Networking / TCP

Show the pictorial representation of TCP 3-way handshaking protocol for establishing a connection between a server and a client.

### Question 10 — Computer Networking / IP Addressing

Find the network address, subnet mask, broadcast address, and usable host IP range for the following IP address: `192.9.205.31/16`.

### Question 11 — Algorithms / Binary Search

Write down the Pseudo Code for recursive binary search algorithm. Use the following function's definition:

`binarySearch(array, target, low, high)`

### Question 12 — Database / Normalization

Explain the differences between Second Normal Form (2NF) and Third Normal Form (3NF) with examples.

### Question 13 — Database / SQL

Given a Patient table in a hospital database below.

| Patient_ID | Disease_Name |
| ---------- | ------------ |
| 1          | Covid-19     |
| 2          | Dialysis     |
| 3          | Covid-19     |
| 4          | Dengue       |

Write down an SQL query to display the total number of patients under each disease category.

### Question 14 — Software Engineering

Write down the differences between Agile model and Waterfall model in Software development. What is white box testing?

### Question 15 — Artificial Intelligence / Machine Learning

Briefly explain supervised learning, unsupervised learning & reinforcement learning.

### Question 16 — Cybersecurity

Briefly explain phishing attack and denial-of-service (DoS) attack.

<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


# Exam 2: BPSC — Network/Website Manager (ICT)

Ministry of Food | Exam Date: 21 May 2025

### Question 1 — Computer Hardware

(a) Define the term "SSD". Briefly describe the working principle of "SSD".

(b) Compare CPU and GPU.

### Question 2 — Memory Management / Boolean Algebra

(a) Write about notes on:

(i) Virtual memory (ii) Cache memory

(b) Use the Karnaugh Map to simplify the following function.

\\[ F(A,B,C)=\bar A\bar B\bar C+A\bar B\bar C+A\bar BC+ABC \\]

### Question 3 — Computer Networking / Subnetting

The IP address of a device in a network is `172.16.128.123/22`. Answer the following questions:

(i) What is the network address?

(ii) What is the subnet mask for the given network?

(iii) What is the broadcast address?

(iv) What is the maximum number of devices in this network?

(v) What is the IP address of the first host device in the network?

### Question 4 — Programming / OOP

(a) Suppose you are working with an array of size 10. It contains all the numbers from 1 to 10 exactly once in a random order. But accidentally, one of the numbers in the array got replaced by a zero (0). Write a C/C++ programme using functions, to restore the lost number.

(b) What is polymorphism in the context of an object-oriented paradigm? Explain the method of overloading and method of overriding with suitable examples.

### Question 5 — Database Management / SQL

Given the following two tables (Students and Marks) in a database, write down the output of the given SQL queries and write down the SQL queries for the outputs.

Students

| StudentId | StudentName |
| --------- | ----------- |
| 1         | Mr. A       |
| 2         | Mr. B       |
| 3         | Mr. C       |
| 4         | Mr. D       |

Marks

| StudentId | Subject | Mark |
| --------- | ------- | ---- |
| 1         | Math    | 70   |
| 2         | Math    | 90   |
| 3         | Math    | 30   |
| 1         | Bangali | 50   |
| 2         | Bangali | 60   |
| 3         | Bangali | 70   |
| 1         | Physics | 80   |
| 2         | Physics | 70   |
| 3         | Physics | 60   |

(i) What is the output of this query?

```
SELECT Count(*)
FROM Students S LEFT JOIN Marks M;
```

(ii) What is the output of this query?

```
SELECT StudentName
FROM Students S JOIN Marks M
ON S.StudentId=M.StudentId
GROUP BY S.StudentId, S.StudentName
HAVING SUM(Mark)>=200;
```

(iii) List all the students' name and number of subjects they have completed.

(iv) List all the students who have not completed any subject.

(v) List all the subject names.

### Question 6 — Data Mining / Machine Learning

(a) Define the term "Data Mining". Explain supervised and unsupervised classification with suitable example.

(b) How can we validate and check reliability of a machine learning model?

### Question 7 — Software Engineering / Artificial Intelligence

(a) What are the advantages and disadvantages of the Agile Model compared to the Waterfall Model in software development?

(b) Distinguish between Generative AI and Large Language Models (LLMs).

### Question 8 — Algorithms / Sorting

(a) Why is Merge Sort preferred over Quick Sort in certain applications, despite having higher space complexity?

(b) Suppose you have a list of items: 41, 25, 87, 57, 80, 79, 19, 36, 42, 7. Using Quick Sort algorithm sort this list. You should explain each step.

<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>

# Exam 3: BPSC — Assistant Director (ICT)

Ministry of Power, Energy & Mineral Resources | Exam Date: 29 May 2025

### Question 1 — Digital Logic & Computer Organization

(a) Consider the following logic circuit.

(i) Derive the Boolean expression algebraically for T1 through T4. Derive F1 and F2 as a function of the three inputs A, B and C.

(ii) Use K-map to simplify these expressions F1 and F2, and show that they are equivalent to the ones obtained in (i).

The original logic circuit is provided on PDF page 18 (printed page 92).

(b) Represent −25 in 8-bit binary using 2's complement.

(c) Compare TTL and CMOS logic family in terms of:

(i) Speed (ii) Noise (iii) Power consumption

### Question 2 — Database Management System

(a) Design an ER diagram for a library management system where:

(i) A library has multiple books.

(ii) Each book can have multiple copies.

(b) Consider the following database schema:

```
employee(employee_name, street, city)
works(employee_name, company_name, salary)
company(company_name, city)
```

Write the SQL commands to perform the following operations:

(i) Find the names of all employees who live in the city "Dhaka".

(ii) Find the names of all employees whose salary is greater than BDT 1,00,000.

(c) Why normalization is required in Database? Write shortly about 3NF.

### Question 3 — Operating System / Computer Architecture

(a) Consider a computer system with the following specifications:

- Physical memory (RAM): 4 GB
- Page size: 4 KB
- Virtual address space: 32 bits
- Page table entry size: 8 bytes

(i) How many pages are there in the virtual address space? Explain your answer.

(ii) What is the size of the page table? Explain your answer.

(b) What is process? Describe different states of a process.

(c) Define context switch with proper example.

(d) What is cache memory? Explain the concepts of:

(i) Cache hit (ii) Cache miss

### Question 4 — Computer Networking

(a) A network has been assigned the IP address `200.1.2.0/24`. It has 3 subnets. Determine the following for each subnet:

(i) Total number of IP addresses (ii) Range of usable IP addresses (iii) Network address (iv) Direct broadcast address (v) Limited broadcast address (vi) Direct broadcast address

(b) Draw the diagram of TCP/IP protocol suite and mention the name of protocols used in different layers of TCP/IP.

(c) Compare circuit switching and packet switching.

### Question 5 — Artificial Intelligence / Machine Learning

(a) Describe the following terms:

(i) Supervised learning (ii) Unsupervised learning (iii) Reinforcement learning

(b) Given following values:

- True Positive (TP) = 560
- True Negative (TN) = 330
- False Positive (FP) = 60
- False Negative (FN) = 50

Calculate the following:

(i) Accuracy (ii) Precision (iii) Recall (iv) F1 Score

(c) What is activation function in Deep Neural Network? What is the usability of this?

### Question 6 — Cybersecurity / Computer Fundamentals

(a) What is 2-factor authentication? Describe it with an example.

(b) What is hash table? What are the advantages of using hash table?

(c) Explain the role of BIOS (Basic Input Output System) in the booting process of a PC. Describe the steps involved in booting a computer from power on to loading operating system.

### Question 7 — C Programming / Object-Oriented Programming

(a) Write a program in any high level language to read an integer and display a pattern like below. For example, if the given integer number is 1234, then the following pattern will be printed.

```
1234
 234
  34
   4
```

(b) What is friend function? Given the following class, show how to add a friend function, named `isneg()` that takes one parameter of type `myclass` and return true if `num` is negative and false otherwise.

```
class myclass {
    int num;
public:
    myclass(int i) {num = i;}
};
```

### Question 8 — Data Structure / Graph Algorithms

(a) Apply the Kruskal's algorithm for the following graph to find out the cost of the minimum spanning Tree (MST).

The original weighted graph is provided on PDF page 27 (printed page 101).

(b) What is heap sort? Build a heap tree from the following list of numbers:

`44, 30, 50, 22, 60, 55, 77, 55`

<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


## Exam 4: BPSC — Assistant Programmer

Ministry of Home Affairs | Exam Date: 19 July 2026

Additional examination included in the uploaded PDF

### Question 1 — Distributed Systems / Computer Architecture / Scheduling

(a) What is a Distributed Computing System? Explain its advantages and disadvantages.

(b) What is Cloud Computing? Explain different types of cloud computing systems.

(c) Clock cycle and clock frequency:

A processor operates at a clock frequency of 3.5 GHz. Calculate the clock cycle/time period and explain the relevant relationship.

(d) Consider the following processes:

| Process | Burst Time (ms) | Priority |
| ------- | --------------- | -------- |
| P1      | 15              | 3        |
| P2      | 2               | 1        |
| P3      | 4               | 3        |
| P4      | 2               | 4        |
| P5      | 8               | 2        |

(i) Draw the Gantt Chart using FCFS and SJF scheduling algorithms.

(ii) Find the turnaround time using these scheduling algorithms.

### Question 2 — Computer Networking

(a) Differentiate between MAC Address and IP Address.

(b) Classify Classful and Classless IP Addresses.

Determine the classes of the following IP addresses:

(i) `00000001 00001011 00000011 11101111`

(ii) `211.10.15.4`

### Question 3 — Computer Graphics / Algorithms

(a) Differentiate between Vector Graphics and Raster Graphics.

(b) Solve the following Knapsack problem.

| Item   | 1  | 2  | 3  | 4  | 5  |
| ------ | -- | -- | -- | -- | -- |
| Value  | 20 | 15 | 12 | 14 | 20 |
| Weight | 4  | 3  | 2  | 2  | 5  |

Knapsack Capacity = 25.

(i) Using the Fractional Knapsack method, find the maximum value.

(ii) Determine the selected items and their order.

### Question 4 — Digital Logic / Computer Networking

(a) What is Color Model? Explain RGB, CMY and CMYK color models.

(b) Prove the following logical equivalence using a Truth Table:

\\[ p\to q\equiv \neg(p\land\neg q) \\]

(c) Differentiate between Bandwidth and Throughput.

### Question 5 — Programming / Algorithms / Microprocessor

(a) Write a C/C++ program to print the Fibonacci series using recursion.

(b) Explain the computational complexity of cryptographic algorithms.

(c) Explain Bubble Sort and sort the following numbers:

`13, 14, 23, 4, 6`

(d) Define the following:

(i) Propagation Delay

(ii) Transmission Delay

(e) Explain the difference between these two instructions:

```
MOV AX, A534H
MOV AX, [A534H]
```

(f) What is Edge Computing? Explain its importance and applications.

### Question 6 — Internet Technology / Web Development

(a) What is the Internet of Things (IoT)? Explain its applications.

(b) What is Cloud Computing and its relationship with IoT?

(c) Compare Static Website and Dynamic Website.

(d) What is DBMS? Mention its major functions.

(e) Explain HTTP and HTTPS.

(f) What is Authentication?

## Additional Questions — Bangla, English & General Knowledge

The BPSC.pdf also contains the following non-ICT written questions.

<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>

### Exam 2 — Network/Website Manager (ICT), 21 May 2025

Bangla (40 Marks)

1. নিচের বিষয়টির ওপর একটি যুক্তিপূর্ণ প্রবন্ধ লিখুন।
2. সারমর্ম লিখুন।
3. একটি ইংরেজি অনুচ্ছেদ বাংলায় অনুবাদ করুন।
4. ভাবসম্প্রসারণ করুন।
5. নিচের বাংলা ব্যাকরণসংক্রান্ত প্রশ্নগুলোর উত্তর লিখুন।

English (40 Marks)

1. Write an essay on "The Internet" using the hints given below: What internet is, Greatest means of communication, Various uses, Storehouse of information, Impact of information technology, Global financial impact, Internet addiction, Harmful effects, Uses and abuses, Conclusion.
2. Write a letter to the officer-in-charge of your police station to provide regular police patrol in your locality to prevent crimes.
3. Read the passage on climate change and answer questions (a)–(e).
4. Rewrite the sentences using the instructions given in brackets (sentence correction, voice, narration, prepositions and idioms).

### Exam 3 — Assistant Director (ICT), 29 May 2025

Bangla / General Knowledge

1. প্রবন্ধ লিখুন।
2. সারমর্ম লিখুন।
3. একটি অনুচ্ছেদ বাংলায় অনুবাদ করুন।
4. ভাবসম্প্রসারণ করুন।
5. বাংলা ব্যাকরণসংক্রান্ত প্রশ্নগুলোর উত্তর লিখুন।
6. সংক্ষিপ্ত সাধারণ জ্ঞানমূলক প্রশ্নগুলোর উত্তর লিখুন।

English (40 Marks)

1. Read the passage about discipline and answer the questions (a)–(e).
2. Write an essay on "Corruption in the ICT Sector in Bangladesh" using the hints given.
3. Imagine that you have purchased a laptop from a local showroom a week back. The warranty period is on and the laptop is not functioning well. Write a letter of complaint to the manager of the showroom about the problem and what you want.
4. Rewrite the sentences using the instructions given in brackets.

### Exam 4 — Assistant Programmer, 19 July 2026

General Knowledge

The paper contains short questions on Bangladesh affairs, international organizations, FTA/PTA, economic diplomacy, bandwidth, CFC, and other general knowledge topics.

English (40 Marks)

1. Write an essay on "Digital Citizenship on Social Media" using the following hints: Introduction, Concept of Digital Citizenship, Benefits of social media, Challenges and risks, Online ethics and responsible behavior, Combating fake news and misinformation, Role of digital literacy and awareness, Conclusion.
2. Write a letter to the editor of a newspaper drawing public attention against the "Wide spread of corruption" in every sphere of life.
3. Read the passage on nuclear war and answer questions (a)–(e).
4. Answer the following questions on grammar and sentence correction.

Extraction note: The principal ICT/CSE questions are listed above by examination. Some additional Bangla, English, and General Knowledge questions are summarized rather than transcribed verbatim because the scanned text is too small or unclear to reproduce reliably. The original PDF should be consulted for those passages, diagrams, and exact question wording.