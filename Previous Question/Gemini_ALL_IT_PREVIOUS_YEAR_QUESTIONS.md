# Master IT Previous Year Question Bank

## Overview & Organization
This document is a consolidated master question bank containing previous year examination questions extracted across 9 source files from competitive recruitment examinations in Bangladesh (including Bangladesh Bank, Combined Banks, BPSC, BCIC, BBA, BCC, BREB, BUET, Petrobangla, WZPDCL, BTCL, and others).

### Duplicate-Counting & Formatting Rules
1. **Exact Deduplication:** Only questions whose complete question content and technical parameters are identical across or within source files have been consolidated. Questions that are merely similar in concept but differ in wording, values, options, code, or subquestions remain as separate entries.
2. **Occurrence Count:** If an identical question appears multiple times, it is retained as a single entry with its verified total occurrence count, formatted as `**(N times)**` (e.g., `**(2 times)**` or `**(3 times)**`). Questions that occur only once do not display an occurrence count.
3. **Combined Bank Post Short Keys:** For Combined Bank examinations, specific post designations are represented using standardized short keys instead of generic wording: Senior Officer (`SO`), Officer (`O`), Assistant Programmer (`AP`), Assistant Database Administrator (`ADA`), Assistant Network Engineer (`ANE`), and Assistant Engineer (`AE`) (e.g., `[SO-2025]`, `[O-2026]`, `[AP-2026]`, `[ADA-2026]`, `[ANE-2026]`, `[AE-2026]`).
4. **Verified Institute-Year Metadata:** All verified institution and year references corresponding to every occurrence are attached as bracketed bold tags (e.g., `**[SO-2025] [BPSC-2025]**`). When metadata cannot be verified from the source context, it is explicitly marked as `[Institute Unknown-Year Unknown]` without fabrication.
5. **Content Preservation:** Original wording, language, spelling, values, options, code snippets, mathematical expressions, subquestions, and tables are preserved verbatim without paraphrasing or omission.
6. **Sequential Numbering:** Questions are numbered sequentially starting from `01` within each of the 17 Master Subjects, without any topic-wise subsections.

## Source Files Processed
All nine expected source files from `/media/irfan/b368c67d-7629-4f43-9f79-973ca03b3fe75/A Study Metarials/Govt Job/Cloud It Online/notes/Previous Question/` were fully processed:
1. `2026/ADA.md`
2. `2026/combined_office_it-2026.md`
3. `BB-AD/previous_question_BB_AD.md`
4. `Cloud IT All Question/all_questions.md`
5. `Compact IT/Bangladesh Bank, AD - ICT.md`
6. `Compact IT/BPSC.md`
7. `Compact IT/Combined_Bank.md`
8. `Compact IT/OTHER_AP.md`
9. `FB_IT_Previous_Year_Questions.md`

---

# 1. C Programming

* 01. Write a C program or Pseudo code to find the similar elements of two arrays and print the similar elements along with the total number of similar elements. **[10]** **(2 times)** **[Bangladesh Bank-2025]**

* 02. Write a C program or Pseudo code to find the similar elements of two array and print the similar elements and number of similar elements. **[Bangladesh Bank-2025]**

* 03. Write a structured program (in C or Python) that takes an integer input n and prints the sum of all even numbers from 1 to n. **(2 times)** **[SO-2025]**

* 04. Write a C program to find the sum of digits of an integer number using "recursion". **[BPSC-2025]**

* 05. (a) Write a program in any high level language to read an integer and display a pattern like below. For example, if the given integer number is 1234, then the following pattern will be printed.

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
   **[BPSC-2025]**

* 06. What is recursion? **[BBA-2025]**

* 07. Write a C program that accepts 10 elements in an array and finds the maximum elements from the array. **[BBA-2025]**

* 08. Write a C program to check whether a string is a Palindrome. **[BUET-2025]**

* 09. Find biggest elements in an array of 10 components. **[BCC-2025]**

* 10. Draw a Flow chart for print odd number for 1 to N. **[BCC-2025]**

* 11. What is recursion? Explain with suitable example? **[Narayanganj City Corporation-2025]**

* 12. Write a Program any language check age 18 eligible to voter or not voter? **[Narayanganj City Corporation-2025]**

* 13. Write a Program any language check leap year? **[Narayanganj City Corporation-2025]**

* 14. This program finds the sum of even and odd numbers from 1 to N. **[Narayanganj City Corporation-2025]**

* 15. Write a Program to check the Armstrong number. **[BREB-2025]**

* 16. Find the output of the following program:

  (a)

  ```
  char str[20] = "Development";
  str[5] = '\0';
  int len = strlen(str);
  printf("%s", str);
  ```

  (b) Find the output of the second C program shown on PDF page 15. **[BREB-2025]**

* 17. Write a C/C++ Program reverse string without library function. **[Biman Bangladesh Airlines-2026]**

* 18. Draw or describe a Flowchart to determine the largest of three distinct numbers (A, B, C). **(2 times)** **[AP-2026]**

* 19. What is the output of the following C program?

  The source code begins at the bottom of PDF page 18 and continues beyond the visible scan. Only part of the code is visible. **[AP-2026]**

* 20. What is the output of the following C program? (Pointer arithmetic with ledger array.) **[The referenced C program is not present on the source page.]** **[AP-2026]**

* 21. Write a program to print prime numbers from 1 to n. **[AP-2024]**

* 22. Write a C program to find the sum of the series: `1 + 2 + 4 + 7 + 11 + ... + N`. **[AP-2024]**

* 23. Find the output of the following recursion:

     ```c
     #include <stdio.h>
     void fun(int x) {
         if (x < 0) return;
         printf("%d\n", x--);
         fun(--x);
         printf("%d\n", x);
     }
     int main() {
         fun(5);
         return 0;
     }
     ```
   **[AP-2024]**

* 24. Write a function to find the smallest element from an array. **[AP-2023]**

* 25. Write a code in C/C++ that will output the 2nd largest number. (If N ≥ 1.) **[AP-2020]**

* 26. Write a C program or Pseudo code to find the similar elements of two arrays and print the similar elements along with the total number of similar elements. **[Bangladesh Bank-2025]**

* 27. Describe run-time error vs compile-time error. **[RAKUB-2026]**

* 28. Write a structured program (in C or Python) that takes an integer input $n$ and prints the sum of all even numbers from 1 to $n$. **[SO-2025]**

* 29. Write a C program to get the maximum element of an array of size 10. **[BBA-2025]**

* 30. What is recursion? Expain with suitable example? **[Narayanganj City Corporation-2025]**

* 31. Write a program in any language to check age 18 eligible to voter or not voter? **[Narayanganj City Corporation-2025]**

* 32. Write a program in any language to check out a leap year or not. **[Narayanganj City Corporation-2025]**

* 33. Write a program in any language to find out even sum and odd sum? **[Narayanganj City Corporation-2025]**

* 34. পয়েন্টার ব্যবহার করে একটি সংখ্যা ইনপুট নাও এবং সেই সংখ্যাটি উল্টো (Reverse) করে প্রিন্ট করে। **[WZPDCL-2026]**

* 35. Write a function which receives an array of integers as parameter and print the numbers divisible by 3 in the array. **[O-2024]**

* 36. Write a program in any language to find the sum of rows and columns of a $m \times n$ matrix, where $m$ and $n$ is taken input from the user. Give the output in the following format: Sample Input matrix: 1 3 4 2 2 4 5 3 3 2 2 1 Sample Output: 10 14 8 **[SO-2024]**

* 37. Write a program in any language to find the prime numbers between $1$ to $n$, where $n$ is taken as user input. Sample input: Enter value of n: 20 Sample Output: Prime Numbers: 2, 3, 5, 7, 11, 13, 17, 19 **[SO-2024]**

* 38. Write a C program to determine prime number from 1 to n. **[AP-2024]**

* 39. Write a program to determine the sum of this series: $1+2+4+7+11+16+....... n^{\text{th}}$ term. **[AP-2024]**

* 40. Find the output of the provided recursive function code. **[AP-2024]**

* 41. What can be used to terminate `for(;;)`? **[BCC-2023]**

* 42. When a function is called more than one time, that is called? **[BCC-2023]**

* 43. What is the name of the technique where a function uses multiple copies? **[BCC-2023]**

* 44. Write a program to check whether a number is prime or not. **[ICB Asset Management-2024]**

* 45. ৩ সংখ্যার মধ্যে বড় সংখ্যা নির্ণয়ের ফ্লোচার্ট এবং ৩ সংখ্যার মধ্যে ক্ষুদ্র সংখ্যা নির্ণয়ের ফ্লোচার্ট। **[BTCL-2024]**

* 46. Write a c code: Input: 6789 Output: 9876. **[BGDCL-2024]**

* 47. Write a program for following sequence analyze complexity: 1, 2, 2, 3, 3, 3, 4, 4, 4, 4, 5, 5, 5, 5, 5... 100 time. **[O-2023]**

* 48. Write a C code segment of swapping two numbers without using third variable. **[WZPDCL-2023]**

* 49. Write the output of the following C Code segment: `unsigned char a=5, b=9; printf("%d \n%d",a<<1,b<<1);` **[WZPDCL-2023]**

* 50. Write a program to reverse a string without using extra memory, reverse in place. [ADBA-2022] **[ADBA-2022]**

* 51. Algorithm to check a number is prime or not [NSDA-2022] **[NSDA-2022]**

* 52. Output Tracing - [NSDA-2022]


  * A) `char str[20] = "Development"; str[5] = '\0'; int len = strlen(str); printf("%s", str);`

  * B) `int i; for (i=0; i<9; i++) { if(i==5) continue; printf("%d\n", i); }` **[NSDA-2022]**

* 53. Write a program which takes 'n' as input and calculate all the odd number up to n. [NSDA-2022] **[NSDA-2022]**

* 54. Find the output of this program [APSCL-2021] **[APSCL-2021]**

* 55. What do you mean by recursion? Calculate factorial function using recursion with C programming code. [Krishi_Biponon_Ministry-2022] **[Krishi Biponon Ministry-2022]**

* 56. c) Find the largest number in an array of N elements. [Krishi_Biponon_Ministry-2022]
  d) Determine even or odd numbers. [Krishi_Biponon_Ministry-2022] **[Krishi Biponon Ministry-2022]**

* 57. Write a C/C++ code for the following series for n number. [NESCO 2021] **[NESCO-2021]**

# 2. Data Structure & Algorithm

* 01. What is Dynamic Programming? Main Characteristics of Dynamic Programming. **(2 times)** **[ADA-2026]**

* 02. Demonstrate the step-by-step construction of a **Min Heap** using the following set of given values:

  ```

  12, 29, 33, 56, 66, 99, 100, and 344

  ```

  Show the heap structure after each insertion. **[10]** **(2 times)** **[Bangladesh Bank-2025]**

* 03. Given an adjacency list representation for a complete binary tree on 7 vertices, give the equivalent adjacency matrix representation. Assume that vertices are numbered from 1 to 7 as in a binary heap. **(2 times)** **[Bangladesh Bank-2023]**

* 04. Construction of Min Heap: Given Value 12, 29, 33, 56, 66, 99, 100, and 344. **[Bangladesh Bank-2025]**

* 05. বাংলাদেশের ব্যাংকিং খাতে কৃত্রিম বুদ্ধিমত্তার প্রয়োগ কীভাবে কার্যক্রমের দক্ষতা ও নিরাপত্তা বৃদ্ধি করতে পারে? একই সঙ্গে, এর সম্ভাব্য ঝুঁকি ও নৈতিক চ্যালেঞ্জসমূহ বিশ্লেষণ করুন। **[SO-2025]**

* 06. Determine whether the following pair of graphs are isomorphic, and justify your answer in one sentence.

  The original question includes two pairs of graph diagrams on PDF page 2 (printed page 59). **[SO-2025]**

* 07. Explain the Quick Sort algorithm with a suitable example. Under what conditions does Quick Sort exhibit its worst-case time complexity, and why does this situation occur? **(3 times)** **[SO-2025]**

* 08. Explain the concepts of Reinforcement Learning (RL), Deep Learning (DL), and Federated Learning (FL) in the context of Machine Learning. Briefly describe how each approach differs in its learning mechanism, data usage, and real-world applications. **(2 times)** **[SO-2025]**

* 09. Write an Algorithm to detect a cycle in a directed graph. **[BPSC-2025]**

* 10. Write down the Pseudo Code for recursive binary search algorithm. Use the following function's definition:

  `binarySearch(array, target, low, high)` **[BPSC-2025]**

* 11. Briefly explain supervised learning, unsupervised learning & reinforcement learning. **[BPSC-2025]**

* 12. (a) Define the term "Data Mining". Explain supervised and unsupervised classification with suitable example.

  (b) How can we validate and check reliability of a machine learning model? **[BPSC-2025]**

* 13. (a) Why is Merge Sort preferred over Quick Sort in certain applications, despite having higher space complexity?

  (b) Suppose you have a list of items: 41, 25, 87, 57, 80, 79, 19, 36, 42, 7. Using Quick Sort algorithm sort this list. You should explain each step. **[BPSC-2025]**

* 14. (a) Describe the following terms:

  (i) Supervised learning (ii) Unsupervised learning (iii) Reinforcement learning

  (b) Given following values:

  - True Positive (TP) = 560
  - True Negative (TN) = 330
  - False Positive (FP) = 60
  - False Negative (FN) = 50

  Calculate the following:

  (i) Accuracy (ii) Precision (iii) Recall (iv) F1 Score

  (c) What is activation function in Deep Neural Network? What is the usability of this? **[BPSC-2025]**

* 15. (a) What is 2-factor authentication? Describe it with an example.

  (b) What is hash table? What are the advantages of using hash table?

  (c) Explain the role of BIOS (Basic Input Output System) in the booting process of a PC. Describe the steps involved in booting a computer from power on to loading operating system. **[BPSC-2025]**

* 16. (a) Apply the Kruskal's algorithm for the following graph to find out the cost of the minimum spanning Tree (MST).

  The original weighted graph is provided on PDF page 27 (printed page 101).

  (b) What is heap sort? Build a heap tree from the following list of numbers:

  `44, 30, 50, 22, 60, 55, 77, 55` **[BPSC-2025]**

* 17. (a) Write a C/C++ program to print the Fibonacci series using recursion.

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

  (f) What is Edge Computing? Explain its importance and applications. **[BPSC-2026]**

* 18. Implementation of Insertion sort, Selection sort, Bubble sort. **[BCIC-2025]**

* 19. Implementation of Stack using two Queues? **[BCIC-2025]**

* 20. In a quicksort algorithm taking the first element as a pivot element, how Analyze the time complexity of the quicksort algorithm when all services of the quicksort algorithm are already sorted. **[Petrobangla-2024]**

* 21. You are given a binary tree (a, b, c, d, e, f, g, h, i) nodes. The post order of the binary tree is:

  `a, b, f, g, h, i, d, e, c`

  Now draw the binary tree and show the array representation of this binary tree.

  # Other Assistant Programmer & ICT — Written Examination Questions

  Source: Other AP-2.pdf | 33 Pages | Questions Only

  The uploaded PDF contains question sets from Biman Bangladesh Airlines, Combined Bank, ICB Securities Trading Company Limited, and BPSC.

  The questions are arranged by institution, examination date, and original numbering. Answers and solutions are excluded. Each examination section ends with the requested closing separator. **[Petrobangla-2024]**

* 22. Short Note:

  (a) AI

  (b) Trans Shiftnam vs Transit

  The wording of Question 13(b) is unclear in the original scan. **[Biman Bangladesh Airlines-2026]**

* 23. Describe step-by-step how Binary Search locates a target value in a sorted array. Why does it fail if the array is unsorted? **(2 times)** **[AP-2026]**

* 24. You have two stacks. Explain the logic required to implement a Queue (FIFO) using only these two stacks. **(2 times)** **[AP-2026]**

* 25. Explain the logic of "Bubble Sort". Why is it considered inefficient for large datasets compared to Merge Sort? **(2 times)** **[AP-2026]**

* 26. Construct a logical argument explaining why a heuristic (like A\* search) might be faster than a blind search (like BFS), even if it doesn't guarantee the absolute perfect path in all cases. **[AP-2026]**

* 27. Compare and contrast the three fundamental paradigms of Machine Learning: Supervised Learning, Unsupervised Learning, and Reinforcement Learning. **(2 times)** **[AP-2026]**

* 28. In a B+ tree, each node can have a maximum of 4 child pointers (order m = 4). From height 0 to height 2 (where height 0 is the root), what is the maximum number of keys that can be stored across all nodes in the tree? **(2 times)** **[AP-2026]**

* 29. Compare between BFS and DFS with proper examples. **[AP-2026]**

* 30. Explain the time complexity of Merge Sort: Best, Average and Worst case. **[AP-2026]**

* 31. Write a function that takes a string as input and changes each alphabetic character to the next character. Non-alphabetic characters should remain unchanged while maintaining case sensitivity. Also mention the time complexity of your solution. **[ICB Securities-2026]**

* 32. (a) Explain the computational complexity of cryptographic algorithms.

  (b) Sort the following numbers using Bubble Sort:

  `13, 14, 23, 4, 6` **[BPSC-2026]**

* 33. Compare BFS & DFS with examples. **[AP-2026]**

* 34. Explain the time complexity of merge sort. Best, Average, Worst. **[AP-2026]**

* 35. Construct a logical argument explaining why a heuristic (like A* search) can be faster than a blind search (like BFS), even if it doesn't guarantee the absolute shortest path in all cases. **[AP-2026]**

* 36. Difference between Stack and Queue. Write about 2 problems solved by stack and queue. **[AP-2024]**

* 37. Problem solved more efficiently in adjacency list representation than adjacency matrix representation and problem solved more effectively in adjacency matrix than adjacency list. **[AP-2023]**

* 38. Perform Max Heap insertion/deletion operations for the given array elements `[a, b, c, d, e, f, g, h, i, j]` step-by-step and show the final binary heap structure/tree representation. **[AP-2023]**

* 39. Linked list, doubly linked list and circular linked list explain with diagram. **[AP-2020]**

* 40. How to determine the weighted graph has negative cycle? **[AP-2020]**

* 41. X is an integer stream of N numbers. You have to select 2 data P and Q such that `A ≤ (P + Q) ≤ B`. Write an algorithm / pseudocode / C program to find how many ways you can select P & Q. The time complexity must be `O(N log N)`. **[AP-2020]**

* 42. Demonstrate the step-by-step construction of a Min Heap using the following set of given values: `12, 29, 33, 56, 66, 99, 100, 344`. Show the heap structure after each insertion. **[Bangladesh Bank-2025]**

* 43. Explain the role of Link-State Advertisements (LSAs) in OSPF and how the Dijkstra SPF algorithm uses the information contained in LSAs to build the routing table. **[ANE-2026]**

* 44. Why is a **Circular Queue** preferred over a **Linear Queue** in many operating systems? Explain with one example. **[SO-2026]**

* 45. Define the following terms used in tree data structures: (i) Tree, (ii) Leaf Node, (iii) Internal Node, and (iv) Height of a Tree. Provide a suitable example to illustrate each term. **[SO-2026]**

* 46. An array contains one million sorted integers. Which searching algorithm would you choose to find a given element? Justify your answer. **[SO-2026]**

* 47. Consider the grammar:

      ```text
      E -> E + E | E * E | id
      ```

      Show that the grammar is ambiguous for the string: `id + id * id`. **[SO-2026]**

* 48. What is a Linked List? What is searching? Explain Binary Search. **[SO-2026]**

* 49. Determine whether the following pair of graphs are isomorphic, and justify your answer in one sentence. **[The pair of graphs is not included on the source page.]** **[SO-2025]**

* 50. Determine whether the following pair of graphs is isomorphic, and justify your answer in one sentence. **[SO-2025]**

* 51. Explain the concepts of Reinforcement Learning (RL), Deep Learning (DL), and Federated Learning (FL) in machine learning, including their learning mechanisms and real-world applications. **[SO-2025]**

* 52. Convert the infix expression $P=12/(7-3)+2$ to postfix expression and evaluate it. **[O-2024]**

* 53. Explain the difference between a singly link list and a doubly link list data structure. **[O-2024]**

* 54. Describe, and estimate the costs of, a procedure to insert a new item into an existing binary max-heap. **[O-2024]**

* 55. What is the worst-case time and space complexity of quicksort? Briefly explain how this worst-case behavior can occur. **[O-2024]**

* 56. You are given a binary tree (a, b, c, d, e, f, g, h, i) nodes. The post order of the binary tree is: a b f c h d e g i nodes. Now draw the binary tree and show the array representation of this binary tree. **[Petrobangla-2024]**

* 57. What is machine learning? Difference between supervised vs unsupervised vs reinforcement learning. **[SO-2024]**

* 58. Difference between stack and queue? Explain two problems that can be solved using stack and queue. **[AP-2024]**

* 59. What is Topology in the context of communication network? Differentiate between Bus, Ring, Tree and Star Topology. What is the purpose of IEEE 802 committee? **[SO-2023]**

* 60. What does the axon of a neural network do? **[BCC-2023]**

* 61. Prefix conversion of $A+(B-C)*D$ expression? **[BCC-2023]**

* 62. What is the minimum node for a binary tree? **[BCC-2023]**

* 63. Machine learning is a feature of cloud computing? True or False. **[BCC-2023]**

* 64. Which data structure uses recursion? **[BCC-2023]**

* 65. What is a binary search algorithm? Write down the algorithm of binary search. **[ICB Asset Management-2024]**

* 66. ট্রি এর ৩ টি বাস্তব উদাহরণ দেখাও। **[BTCL-2024]**

* 67. Node সংখ্যা N হলে ট্রি এর edge সংখ্যা কত হবে ব্যাখ্যা কর। **[BTCL-2024]**

* 68. How to represent binary tree using array data. Dry Run of Array Representation of Binary Tree with Example. **[BGDCL-2024]**

* 69. What is Network Topology? Distinguish between Bus, Ring, Tree and Star topology. Discuss how the Bus topology works. **[ANE-2023]**

* 70. Find the output of the following program including time and space complexity. [Code segment for Fibonacci series shown] **[ANE-2023]**

* 71. What is binary search tree? Write an example of it. **[WZPDCL-2023]**

* 72. What is the difference between Divide and Conquer and Dynamic Programming? **[WZPDCL-2023]**

* 73. Give an adjacency-list representation for a complete binary tree on 7 vertices. Give an equivalent adjacency-matrix representation. Assume that vertices are numbered from 1 to 7 as in a binary heap. $[BB\text{-}AP\text{-}2023]$ **[BB-AP-2023]**

* 74. The complexity of the merge sort is $T(n) = 2T(n/2)+n$. Explain how the above equation is derived? $[\text{Multiple Ministry } AP\text{-}2023]$ **[Multiple Ministry  AP-2023]**

* 75. How does dynamic programming relate to the divide and conquer approach? $[\text{Multiple Ministry-}2023]$ **[Multiple Ministry-2023]**

* 76. Does greedy algorithm always achieve optimal solution? If not, when does greedy approach achieve optimal solution? $[\text{Multiple Ministry-}2023]$ **[Multiple Ministry-2023]**

* 77. Different protocol are work in different layer of networking protocol stack. There are different types of layer data link layer, physical layer, network layer and transport layer. Fill up the following protocol table by work at which layer? $[BPDB\text{-}2023]$ CSMA, OSPF, TCP, UDP, RIP. **[BPDB-2023]**

* 78. Construct the binary search tree using the following set of data 45, 9, 5, 19, 23, 19, 46, 2, 12, 10. $[BR\text{-}Powergen\text{-}2024]$ **[BR Powergen-2024]**

* 79. How hashing is done for a particular set of numbers with the hashing function $f(x) = x \text{ mod } 10$, show the process in diagrams and the resulting hashing table. [ADBA-2022] **[ADBA-2022]**

* 80. Construct binary tree from: [APSCL-2021]

      * pre-order: 1, 5, 7, 8, 3, 4, 10
      * in-order: 7, 5, 8, 1, 4, 3, 10 **[APSCL-2021]**

* 81. You want to search a specific number x in the array where $2^{20}$ numbers are stored in ascending order. Write down a pseudo code to search x in an optimal search policy. **[APSCL-2021]** **[APSCL-2021]**

* 82. Assume that you are dealing with a new element sup request by an online portal at ASCL where each request has importance associated with it. Which data structure would be helpful to deal with these objects (communication request) when it is necessary to repeatedly remove the connection request with the highest or lowest importance. [APSCL-2021] **[APSCL-2021]**

* 83. Differentiate between array and structure data types. [Krishi_Biponon_Ministry 2022] **[Krishi Biponon Ministry-2022]**

* 84. Explain the differences between depth-first and breadth-first searches. [Krishi_Biponon_Ministry 2022] **[Krishi Biponon Ministry-2022]**

* 85. For which type of data a linked list is better (INSERT/DELETE/UPDATE) than an array? [NESCO 2021] **[NESCO-2021]**

* 86. Find the number of nodes in a binary tree for height 7. Note that the root node has a height of 0. **[Institute Unknown-Year Unknown]**

* 87. What do you mean by machine learning? Name three machine learning applications in our daily life. [Krishi_Biponon_Ministry - 2022] **[Krishi Biponon Ministry-2022]**

* 88. Write the difference between machine learning and deep learning. [Krishi_Biponon_Ministry - 2022] **[Krishi Biponon Ministry-2022]**

# 3. Data Communication & Networking

* 01. What is Responsive Web Design? Client-Side & Server-Side Scripting. **(2 times)** **[ADA-2026]**

* 02. What is DNS? How Does DNS Work? **(2 times)** **[ADA-2026]**

* 03. Given IP address 192.168.1.0/24 and divided into four subnets in equal size:

  * A) Find the new subnet mask (CIDR).
  * B) Find out first usable host address of subnet. **(2 times)** **[ADA-2026]**

* 04. Mention the layers of the OSI Model and the function of each layer **(2 times)** **[O-2026]**

* 05. Compare TCP and UDP protocols with examples. (User Datagram Protocol) and UDP Protocols. The main differences are given below (TCP vs UDP (Comparison Table)) **(2 times)** **[O-2026]**

* 06. What is cloud computing? Mention its service models **(2 times)** **[O-2026]**

* 07. What is the Total Latency for a 3-kbyte message (an e-mail) if the bandwidth of the network is 1Gbps? Assume that the distance between the sender and the receiver is 300 km and light travels at a speed of 2 × 10⁸ m/s. Given that Round Trip Time (RTT) is 50 ms and Queueing Time is 5 ms. **[10]** **(2 times)** **[Bangladesh Bank-2025]**

* 08. Sinthia wants to send an email to her friend Afsana. The communication flows through the Application layer and Transport layer of the OSI/TCP-IP model.

  (a) Mention the primary protocols used in both the Application layer and the Transport layer to support this functionality.

  (b) Write down the detailed step-by-step process of Mail transfer from Sinthia's client environment to Afsana's mailbox. **(2 times)** **[Bangladesh Bank-2025]**

* 09. What is Total Latency for a 3-kbyte message (an e-mail) if the bandwidth of the network is 1Gbps? Assume that the distance between the sender and the receiver is 300 km and that light travels at \\(2\times10^8\\) m/s. Round Trip Time 50ms Queuing Time 5ms? **[Bangladesh Bank-2025]**

* 10. Sinthia wants to send an email to her friend (Afsana). He sends the email through application and transport layer.

  (a) Mention the protocol of application layer and transport layer.

  (b) Write down the steps of Mail transfer from Afsana to Sinthia. **[Bangladesh Bank-2025]**

* 11. Why are data privacy and regulatory compliance (such as AML, KYC, and international data-protection standards) vital for the stability and credibility of the banking sector in Bangladesh? Discuss with examples and practical recommendations. **[SO-2025]**

* 12. Why does the Domain Name System (DNS) primarily use UDP as its transport layer protocol instead of TCP? Describe the sequence of events that take place during the DNS name resolution process when a user enters www\.companybd.com into a web browser and presses Enter. **[SO-2025]**

* 13. Show the pictorial representation of TCP 3-way handshaking protocol for establishing a connection between a server and a client. **[BPSC-2025]**

* 14. Find the network address, subnet mask, broadcast address, and usable host IP range for the following IP address: `192.9.205.31/16`. **[BPSC-2025]**

* 15. The IP address of a device in a network is `172.16.128.123/22`. Answer the following questions:

  (i) What is the network address?

  (ii) What is the subnet mask for the given network?

  (iii) What is the broadcast address?

  (iv) What is the maximum number of devices in this network?

  (v) What is the IP address of the first host device in the network? **[BPSC-2025]**

* 16. (a) Differentiate between MAC Address and IP Address.

  (b) Classify Classful and Classless IP Addresses.

  Determine the classes of the following IP addresses:

  (i) `00000001 00001011 00000011 11101111`

  (ii) `211.10.15.4` **[BPSC-2026]**

* 17. What are the CIDR Prefixes exactly representing the range of IP addresses `10.12.2.0` to `10.12.3.255`? **[BCIC-2025]**

* 18. Which of the following are not needed in software Requirement Specifications (SRS)?

  (a) Functional Requirements

  (b) Non-Functional Requirements

  (c) Testing Requirements

  (d) Interface Requirements




  # Other Assistant Programmer & ICT Examination Questions

  Source: Other AP - 25.pdf | 20 Pages | Questions Only

  The PDF contains several examination sets from different organizations. Below, the questions are arranged by organization and examination date, maintaining the original numbering. All answers and explanations are excluded. **[BCIC-2025]**

* 19. What is the port number used by DNS? **[BBA-2025]**

* 20. What is the port number of DNS? **[BCC-2025]**

* 21. Write down the private IP address range for class B? **[BCC-2025]**

* 22. Check the valid IP address from the following table.

  `1.1.1.1` (1.1.1.1 is a valid IP address) **[BREB-2025]**

* 23. What does DHCP mean? **[BREB-2025]**

* 24. What is the need of edge server? **(2 times)** **[Petrobangla-2024]**

* 25. For the following description of various IP networking protocols write down the protocol name and its full form in the following table.

  The protocol-description table begins on PDF page 1 and continues onto page 2; not all rows are legible. **[Biman Bangladesh Airlines-2026]**

* 26. Given IP address `192.168.72.138/16` find total IP, total usable IP, Network address, Subnet mask, Broadcast address. **[Biman Bangladesh Airlines-2026]**

* 27. What is Cloud computing? Importance of Cloud computing? Describe IaaS, PaaS and SaaS. **[Biman Bangladesh Airlines-2026]**

* 28. Apply the concept of IP addressing and routing to explain how packets are delivered across networks using Open Shortest Path First (OSPF) at the network layer. **(2 times)** **[AP-2026]**

* 29. Explain the logic of a "Checksum". How is it used to verify data integrity during file transfer? **(2 times)** **[AP-2026]**

* 30. Compare between TCP and UDP. **[AP-2026]**

* 31. A `/22` network is to be divided into five subnets for five departments with host requirements of 250, 250, 125, 120, and 60.

  Determine the network address, subnet mask, and usable host range for each subnet. **[ICB Securities-2026]**

* 32. The CPU is fast, but the RAM is slow, causing the CPU to wait for memory access and resulting in slow response time.

  (a) To improve response time, should the CPU or RAM be upgraded? Explain.

  (b) If the RAM speed is doubled, will the memory latency be reduced by half? Explain. **[ICB Securities-2026]**

* 33. (a) Differentiate between MAC Address and IP Address.

  (b) Differentiate between Classful and Classless IP Addressing. Determine the IP address classes for:

  (i) `00000001 00001011 00000101 11101111`

  (ii) `211.10.15.4` **[BPSC-2026]**

* 34. (a) What is Propagation Delay?

  (b) What is Transmission Delay?

  (c) Explain the difference between the following assembly instructions:

  ```
  MOV AX, A534H
  MOV AX, [A534H]
  ```

  (d) What is Edge Computing? Explain its importance. **[BPSC-2026]**

* 35. Compare between TCP and UDP: their connection, reliability, speed. One real-life use case of UDP. **[AP-2026]**

* 36. CRC is a redundancy error technique used to determine the error. Suppose the original data is `11100` and the divisor is `1001`. **[AP-2023]**

* 37. Attacker steals private key of website that uses transport layer security and remains undetected. What can be done with a private key? **[AP-2023]**

* 38. Write down the functionality of OSI model. **[AP-2020]**

* 39. What is the Total Latency for a 3-kbyte message (an e-mail) if the bandwidth of the network is 1 Gbps? Assume that the distance between the sender and the receiver is 300 km and light travels at a speed of `2 × 10⁸ m/s`. Given that Round Trip Time (RTT) is 50 ms and Queuing Time is 5 ms. **[Bangladesh Bank-2025]**

* 40. Sinthia wants to send an email to her friend Afsana. The communication flows through the Application layer and Transport layer of the OSI/TCP-IP model. [10]
     - (a) Mention the primary protocols used in both the Application layer and the Transport layer to support this functionality.
     - (b) Write down the detailed step-by-step process of Mail transfer from Sinthia's client environment to Afsana's mailbox. **[Bangladesh Bank-2025]**

* 41. Explain the main differences between IPv4 and IPv6 addressing. Include at least three key differences and state the IPv6 equivalent of ARP. **[ANE-2026]**

* 42. Using VLSM, subnet the block `10.100.0.0/22` to allocate address space for the following departments. Write the Subnet Address and CIDR mask for each. Allocate efficiently and show the order of allocation.
     - Dept A: 250 hosts
     - Dept B: 120 hosts
     - Dept C: 50 hosts
     - **[The fourth bullet in the source is blank.]** **[ANE-2026]**

* 43. List the top five steps of the BGP path-selection decision process in priority order (highest priority first). Briefly describe how each criterion influences the selection of the best route when multiple routes to the same destination are available. **[ANE-2026]**

* 44. Explain how Port Address Translation (PAT) works and why it is more commonly used than Static or Dynamic NAT in most enterprise and home networks. **[ANE-2026]**

* 45. What is network topology? Explain the different network topologies. **[ANE-2026]**

* 46. Draw and explain the seven layers of the OSI model. **[ANE-2026]**

* 47. Divide the network `192.168.10.0/24` into four equal-sized subnets and determine the following for each subnet:
      - Network address
      - Subnet mask
      - Usable host range
      - Broadcast address **[ANE-2026]**

* 48. What is Cross Site Scripting? Reflected XSS & stored XSS in terms of how the payload is delivered to the victim. **[RAKUB-2026]**

* 49. Excessive broadcast traffic in LAN. What is the cause and solution? **[RAKUB-2026]**

* 50. IPv6 headers enable faster processing and resulting throughput across intermediate transit routers than the legacy IPv4. Explain the key reasons. **[RAKUB-2026]**

* 51. A core router receives a packet with destination IP address `192.168.20.45`. The router's forwarding table contains the following overlapping routes: `192.168.0.0/16`, `192.168.16.0/20`, `192.168.20.0/22`, `192.168.20.32/27`. Identify the exact routing interface the router will use to forward this packet. **[RAKUB-2026]**

* 52. A corporate network pool experiences exhaustion due to a high volume of transient guest devices. What lease duration parameters adjustment resolves this? **[RAKUB-2026]**

* 53. A satellite link has a one-way propagation delay of 250 ms and a transmission rate 1 Mbps. Frame size 1000 bytes; calculate utilization efficiency if stop-and-wait protocol is used. What is the minimum window size required to achieve 100% efficiency? **[RAKUB-2026]**

* 54. An organization has been assigned the IPv4 network address `192.168.1.0/24`. As part of the network deployment, the network administrator is required to divide the address space into four equal-sized subnets to support different departments. Determine the Network Address, Subnet Mask (both CIDR and dotted-decimal notation). **[O-2026]**

* 55. Describe the functions of a Switch and a Router and explain two key differences between these networking devices. **[O-2026]**

* 56. What is a communication system? Describe the different types of transmission modes with examples. **[O-2026]**

* 57. What is cloud computing? Why is it used? State the difference between cloud storage and traditional storage. **[O-2026]**

* 58. Network Address Translation (NAT) maps internal networks to the public internet.
      - (a) Explain the historical IP addressing limitation that made NAT a necessity globally.
      - (b) Explain the step-by-step logical translation process that occurs at a branch router when an internal employee (IP `192.168.1.5`) sends a web request to an external server, and how the router correctly handles the returning response packet. **[O-2026]**

* 59. Subnetting logic requires precise binary calculation. A network engineer is tasked with dividing the internal network `192.168.10.0/24` into exactly 4 equal subnets for four different bank branches. Show the mathematical calculation to determine how many bits must be borrowed to create 4 subnets, and state the new Subnet Mask in both CIDR notation and decimal format. **[O-2026]**

* 60. Mention the layers of the OSI Model and the function of each layer. **[O-2026]**

* 61. Compare TCP and UDP protocols with examples. **[O-2026]**

* 62. What is cloud computing? Mention its service models. **[O-2026]**

* 63. An organization is granted the IPv4 network block `14.24.74.0/24` and needs to segment it into two subnets: Subnet A (requires 120 addresses) and Subnet B (requires 60 addresses). Allocating sequentially from the requirement first to maximize remaining address space, state only the Network Address (with its CIDR mask) and the Broadcast Address for both subnets. **[SO-2026]**

* 64. What is the OSI model? Explain the functions of each layer with examples. **[SO-2026]**

* 65. Define Computer Network. Describe different types of Computer Networks. **[SO-2026]**

* 66. What is Cloud Computing? What are its characteristics? Briefly describe the types of cloud computing and its applications. **[SO-2026]**

* 67. A bank has the network block `192.168.10.0/24`. The IT manager wants to divide this into 4 equal subnets.
     - (a) How many bits do you need to borrow to make 4 subnets?
     - (b) What is the new Subnet Mask in dotted-decimal format?
     - (c) Write down the Network Address, the First Usable IP, and the Broadcast Address for the second subnet created. Show your calculation. **[SO-2026]**

* 68. Why does the Domain Name System (DNS) primarily use UDP as its transport layer protocol instead of TCP? Describe the sequence of events that take place during the DNS name resolution process when a user enters into a web browser and presses enter. **[SO-2025]**

* 69. At which layer of the OSI model does a standard Router primarily operate, and what is the specific name of the Protocol Data Unit (PDU) at this layer? A router has four contiguous /24 routing table entries: `10.1.0.0/24`, `10.1.1.0/24`, `10.1.2.0/24`, and `10.1.3.0/24`. If you summarize (supernet) these into a single route, what will be the new CIDR notation? **[AE-2026]**

* 70. (i) For securing a bank's sensitive customer data, what is the fundamental difference in the specific technologies used to protect "Data in Transit" versus "Data at Rest"?

      (ii) What defines a "Zero-Day" vulnerability, and why do traditional signature-based antivirus solutions fail to protect a bank's servers against them? **[AE-2026]**

* 71. Why does the Domain Name System (DNS) primarily use UDP as its transport layer protocol instead of TCP? Describe the sequence of events during a DNS lookup. **[SO-2025]**

* 72. Given network `245.248.128.0/20`, divide the address space among three departments (Manager, HR, Admin) with specific proportions and determine network blocks, IP ranges, and valid hosts. **[Dhaka WASA-2025]**

* 73. Calculate the network address, broadcast address, minimum host address, and maximum host address for the IP address `192.168.111.168/28`. **[BBA-2025]**

* 74. Find the IPv4 Private IP ranges for Class A, Class B, and Class C. **[BBA-2025]**

* 75. Two computers on the same LAN cannot communicate with each other, but both can access the internet. What possible causes would you examine? **[Ministry of Land-2025]**

* 76. DNS কী? DNS-এর কাজ বা উদ্দেশ্য লেখো। **[WZPDCL-2026]**

* 77. রাউটার (Router) কেন টেবিল (Routing Table) সংরক্ষণ করে? **[WZPDCL-2026]**

* 78. Consider the following buy a product description. System presents full pricing information and customer fills in credit card information. System authorizes purchase confirms sale and sends confirming email to customer. Draw a use case diagram for the above system. **[O-2024]**

* 79. Using an explanation of the difference between flow-control and congestion control, discuss the impact of a stable end-to-end latency **[O-2024]**

* 80. Mention the day and month of celebration of International Mother's Day. **[SO-2024]**

* 81. Briefly describe the following network devices: Repeater, hub, Bridge, Switch and Router. **[SO-2024]**

* 82. What are the different types of transmission media used for data communication? Explain their advantages and disadvantages. **[SO-2024]**

* 83. How many types of modes are used in data transferring through networks? Briefly explain those modes. Differentiate between TCP vs UDP. **[SO-2024]**

* 84. Differentiate between OSI Model and TCP/IP Model. What is the relation between Data, Segment, Packet, Frame and Bit in OSI Model? **[SO-2023]**

* 85. IPv6 is how many bits? **[BCC-2023]**

* 86. What is the popular way of linking many documents? **[BCC-2023]**

* 87. What is propagation time? What are the propagation time and the transmission time for a 5 Mbyte message (an image) if the bandwidth of the network is 1 Mbps? Assume that the distance between the sender and the receiver is 12000 km and that light travels at $2.4\times 10^8\text{ m/s}$. **[ICB Asset Management-2024]**

* 88. Function of switch, Bridge Router. Difference between TCP, UDP used transport layer TCP/IP protocol architecture. **[O-2023]**

* 89. Differentiate between OSI Model and TCP/IP Model. Draw the diagram of 4 Layers of TCP/IP Model including the main function of each layer and related protocols. List some basic functions performed at the MAC layer. **[ANE-2023]**

* 90. Write down the basic differences of the following: a) Public vs. Private IP address **[ANE-2023]**

* 91. Differentiate between Collision Domain and Broadcast Domain in computer network. What is the function of DNS and DHCP? **[ANE-2023]**

* 92. What do you mean by Subnet and Subnet Mask? The network address of 172.16.0.0/19 provides how many subnets and hosts? What is the function of OSPF? **[ANE-2023]**

* 93. Convert the decimal IP address 192.168.101.5 into binary IP address. Fill-up the following in tabular form: **[ANE-2023]**

* 94. Differentiate between IPv4 and IPv6. **[WZPDCL-2023]**

* 95. MAC flooding, Piggy Backing? $[\text{Teletalk-}2023]$ **[Teletalk-2023]**

* 96. Write a JavaScript code to validate mobile number input, which should be 11 digits, and the number must include + before it. [NESCO 2021] **[NESCO-2021]**

* 97. In IPv4, show the network address and host of classes A, B, and C. [NSDA-2022] **[NSDA-2022]**

* 98. Given IP: 192.168.5.154/26, Calculate network and subnet mask. [NSDA-2022] **[NSDA-2022]**

* 99. Given IP address is: 172.16.128.120/25 **[APSCL-2021]**
      * a. What is the network address?
      * b. What is subnet mask?
      * c. This network can cover how many host networks?
      * d. What is the Broadcast address? **[APSCL-2021]**

* 100. Describe the data communication system with the necessary diagram. [Krishi_Biponon_ministry 2022] **[Krishi Biponon Ministry-2022]**

* 101. Write short notes on i) Web server ii) ISP iii) Router iv) Search engine. **[Institute Unknown-Year Unknown]**

* 102. Why packet switching is suitable for digital data transmission. [Krishi_Biponon_Ministry 2022] **[Krishi Biponon Ministry-2022]**

* 103. How can you define IoT? What are the essential components of IoT? [Krishi_Biponon_Ministry - 2022] **[Krishi Biponon Ministry-2022]**

# 4. Security & Cryptography

* 01. Cyber risk management in financial institutions. **(2 times)** **[ADA-2026]**

* 02. Suppose your workstation affect ransomware attack so what five steps you take to mitigate this problem? **(2 times)** **[ADA-2026]**

* 03. What is Phishing? What are the types of phishing and prevention measures? **(2 times)** **[ADA-2026]**

* 04. What is firewall? Difference between stateful inspection and new technology firewall (NGFW). **(2 times)** **[ADA-2026]**

* 05. Firewall rules:

  * Rule 1: A source destination B port is 89.
  * Rule 2: A source destination B less than 443.
  * Rule 3: A source destination B port is 443.
  When a packet comes from 443, is it accepted or rejected? Explain the procedure (First inspection rules). **(2 times)** **[ADA-2026]**

* 06. What is authentication and authorization? What is the CIA triad in cybersecurity? **(2 times)** **[O-2026]**

* 07. What is social engineering? What is vulnerability assessment? How is it different from encryption? What is hashing? **(2 times)** **[O-2026]**

* 08. A new employee joins the bank. Describe the process of creating a new user account for them, focusing on security best practices (e.g., password policies) **(2 times)** **[O-2026]**

* 09. Based on the information given below, Can User X write to Folder 1? Explain the precedence logic (Explicit Deny vs Explicit Allow). Access Logic:

  * User X belongs to Group A and Group B.
  * Folder 1 grants "Read" to Group A.
  * Folder 2 has an "Explicit Deny Write" for Group B.
  * Folder 1 grants "Write" to User X individually.
  Can User X Write to Folder 1? **(2 times)** **[O-2026]**

* 10. Bangladesh Bank operates an internal client-server architecture communicating with a Mail Server, a DNS Server, and a Web Server. The bank network administration intends to maximize security by enforcing Firewall protection on these servers. Draw a clean network architecture diagram reflecting this secure infrastructure scenario. **(3 times)** **[Bangladesh Bank-2025]**

* 11. Consider a hash table of size 13 strong entries with integer keys. Suppose the hash function is h(k)=kmod 13h(k). Insert in the given order entries with keys 10,3,6,16,17,1910,3,6,16,17,19 into the hash table using linear probing to resolve collisions. Show all the work. **[Bangladesh Bank-2023]**

* 12. Describe a man-in-the-middle attack on the Diffie-Hellman key exchange protocol in which the adversary generates two public key pairs for the attack. **(2 times)** **[Bangladesh Bank-2023]**

* 13. Preserving confidentiality, integrity, and availability of data is a restatement of the concern over falsification, masquerade, and denial of service. Explain how the first three concepts relate to the last four. **[Bangladesh Bank-2023]**

* 14. In order to prevent that, the company decided to add end-to-end encryption techniques. Which layer of the OSI model is suitable to work in, considering parameters like development time, software maintainability, and development cost? Give reasons for your concepts. **(2 times)** **[Bangladesh Bank-2023]**

* 15. Bangladesh Bank have client server and the communication with Mail Server, DNS server, Web server. Bangladesh Bank want to ensure the security using firewall on those server. Draw a diagram with the scenario. **[Bangladesh Bank-2025]**

* 16. Describe how the principles of Confidentiality, Integrity, and Availability work together to protect organizational data, and provide one real-world example of a security breach where one or more of these principles were compromised. **(2 times)** **[SO-2025]**

* 17. A banking application requires users to enter a 4-digit PIN for login.

  - Explain how you would test this input field to ensure that it accepts only valid 4-digit numbers and rejects invalid inputs.
  - Mention a few test cases you would include and explain why such testing is important for system security and reliability. **[SO-2025]**

* 18. What is a Man-in-The Middle (MitM) attack? How can it be prevented? **[BPSC-2025]**

* 19. Briefly explain phishing attack and denial-of-service (DoS) attack. **[BPSC-2025]**

* 20. Why NAND is universal gate? **[BCC-2025]**

* 21. What is difference between Encryption and hashing? Comparison between Cybersecurity & Cyber Crime. **[Biman Bangladesh Airlines-2026]**

* 22. What is a Universal Gate? Prove that the NAND gate is a Universal Gate. **[AP-2026]**

* 23. Why is a Zero-Day Attack dangerous for IT? Mention two reasons. **[ICB Securities-2026]**

* 24. What is a Universal Gate? Prove that the NAND Gate is a Universal Gate. **[AP-2026]**

* 25. A & B two frames in a browser loaded from different origins. Why is it a reasonable security policy to allow A to navigate B to another origin based only on whether the display area of A contains display space of B and A has the control over the area? **[AP-2023]**

* 26. Consider a hash table of size 13 storing entries with integer keys. Suppose the hash function is `h(k) = k mod 13`. Insert in the given order entries with keys `10, 3, 6, 16, 17, 19, 10, 3, 6, 16, 17, 19` into the hash table using linear probing to resolve collisions. Show all the work. **[Bangladesh Bank-2023]**

* 27. Preserving confidentiality, integrity, and availability of data is a restatement of the concern over falsification, masquerade, and denial of service. Explain how the first three concepts relate to the last four. **[The source says "last four," although it lists three latter concerns.]** **[Bangladesh Bank-2023]**

* 28. Difference between spoofing and sniffing. **[AP-2020]**

* 29. What is Two-Factor Authentication (2FA)? Define the CIA Triad. **[Bangladesh Bank-2026]**

* 30. Explain three fundamental principles of information security. **[Bangladesh Bank-2026]**

* 31. Differentiate between a firewall, an Intrusion Detection System (IDS), and an Intrusion Prevention System (IPS), and explain how each contributes to network security. **[ANE-2026]**

* 32. Several computers in a bank branch become encrypted by ransomware. Describe the immediate actions the IT team should take in chronological order. **[ANE-2026]**

* 33. Differentiate between a Computer Virus and a Computer Worm based on how they spread and replicate across host networks. **[O-2026]**

* 34. Draw the circuit schematic diagrams to build an Exclusive-OR (XOR) logic function using only universal NAND gates. **[O-2026]**

* 35. Explain the concepts of encryption and decryption with an example. **[O-2026]**

* 36. Explain how any Boolean function can be implemented using only universal gates. **[O-2026]**

* 37. What is a phishing attack? Explain its types and discuss methods to prevent it. **[O-2026]**

* 38. What does CIA stand for in information security? Explain each component briefly. **[O-2026]**

* 39. Multi-Factor Authentication (MFA) is mandatory in modern banking infrastructure. (a) Define the concept of MFA and explicitly list the three globally recognized categories of authentication factors. **[O-2026]**

* 40. What is authentication and authorization? What is the CIA triad in cyber security? How does it work? **[O-2026]**

* 41. What is social engineering? What is hashing? How is it different from encryption? **[O-2026]**

* 42. A new employee joins the bank. Describe the process of creating a new user account for them, focusing on security best practices (e.g., password policies). **[O-2026]**

* 43. Based on the information given below, can User X write to Folder 1? Explain the precedence logic (Explicit Deny vs Explicit Allow) Access Logic.
      - User X belongs to Group A and Group B.
      - (i) Folder 1 grants "Read" to Group A.
      - (ii) Folder 1 has an "Explicit Deny Write" for Group B.
      - (iii) Folder 1 grants "Write" to User X individually. **[O-2026]**

* 44. Explain the operational difference between Hashing and Encryption. **[SO-2026]**

* 45. Why is cyber security important? What are the common types of cyber threat? Explain cyber security measures. **[SO-2026]**

* 46. What is Encryption? What are the types? Explain the role of Encryption in security. **[SO-2026]**

* 47. What is Cryptocurrency? What is Bitcoin? What are the advantages of Blockchain Technology? **[SO-2026]**

* 48. A banking application requires users to enter a 4-digit PIN for login. Explain how you would test this input field to ensure that it accepts only valid 4-digit numbers and rejects invalid inputs. Mention a few test cases you would include and explain why such testing is important for system security and reliability. **[SO-2025]**

* 49. A server suddenly starts sending abnormal traffic to external systems. Analyze the possible cause and suggest immediate actions. **[AE-2026]**

* 50. Describe how the principles of Confidentiality, Integrity, and Availability (CIA Triad) work together to protect organizational data, and provide one real-world example of a security breach where one or more principles were compromised. **[SO-2025]**

* 51. What preventive measures should be taken to ensure cyber security of the IT equipments and systems of an office? **[Ministry of Land-2025]**

* 52. An Intrusion Prevention System (IPS) frequently blocks large print jobs sent to a high-capacity departmental printer, flagging them as potential data exfiltration attempts. Smaller jobs print successfully.


  * (a) How would you analyze IPS alerts and traffic patterns to confirm whether these are false positives?


  * (b) What tuning strategies would you apply to balance security monitoring and operational efficiency? **[Ministry of Land-2025]**

* 53. Let you procure a microfinance application and host it in your office's data center. What kind of cyber-security threats should you be aware of and what steps would you take to mitigate the threats? **[SO-2024]**

* 54. What do you understand about the IT disaster recovery plan? Describe your approach to disaster recovery and business continuity planning for the data center of your office. **[SO-2024]**

* 55. What do you mean by the CIA Triad of Information/Cyber security? What are the 10 most common types of Cyber-attacks today? Discuss how do the Ransomware attack and DDOS attack work? **[SO-2023]**

* 56. What is Blockchain? How does Blockchain Work? Mention top 5 benefits of blockchain technology in business. What is the key difference between Traditional (Online) banking and Digital banking? **[SO-2023]**

* 57. In which layer does IPsec work? **[BCC-2023]**

* 58. Software downloaded from the internet and installed that is malicious is called what? **[BCC-2023]**

* 59. In which way can blockchain data be modified? **[BCC-2023]**

* 60. What is a distributed ledger on a peer-to-peer network called? **[BCC-2023]**

* 61. What are hackers who find bugs and vulnerabilities called? **[BCC-2023]**

* 62. What is the function of a firewall? **[BCC-2023]**

* 63. How to create private and public key using RSA algorithm. **[ICB Asset Management-2024]**

* 64. How to provide system Security. **[ICB Asset Management-2024]**

* 65. What is the difference between Web application firewall and Network Firewall. **[BR Powergen-2024]**

* 66. Difference between digital signature and certificate. Write down the definition of White hat, Black hat and gray hat hackers. **[O-2023]**

* 67. benefits of network firewall. Types of firewall. Difference of Traditional firewall and next generation firewall. **[O-2023]**

* 68. Draw a diagram of LAN including network Firewall. Why is firewall important in network

  Based on the provided images, here are the red-circled questions retrieved text-by-text in their proper sequential order: **[ANE-2023]**

* 69. Distinguish between Symmetric Encryption and Asymmetric Encryption. Give some examples of encryption algorithms. What are the different types of ciphers in cryptography? What are the factors to be considered for cryptographic strength? **[ANE-2023]**

* 70. Write down about blockchain. **[WZPDCL-2023]**

* 71. What is asymmetric cryptosystems? Write an example of it. **[WZPDCL-2023]**

* 72. Preserving confidentiality, integrity and availability of data is a restatement of the concern over falsification, interception, masquerade and denial-of-service. Explain how do the first three concepts relate to the last four. $[BB\text{-}AP\text{-}2023]$ **[BB-AP-2023]**

* 73. Draw a binary tree of 15 elements and list out the elements in (i) Preorder (ii) In order (iii) post order traversals. $[\text{Multiple Ministry-}2023]$ **[Multiple Ministry-2023]**

* 74. What is a digital signature. Describe its role in digital security? [Krishi_Biponon_ministry 2022] **[Krishi Biponon Ministry-2022]**

* 75. What does mean by DDoS attack? [NESCO 2021] **[NESCO-2021]**

# 5. Database

* 01. What is Normalization? Briefly describe the types of normalization. **(2 times)** **[ADA-2026]**

* 02. You have tables EMPLOYEES (ID, Name, DeptID) and DEPARTMENTS (DeptID, DeptName). Write the logical steps (or pseudo-SQL logic) to get a list of Employee Names who work in "IT". **(2 times)** **[O-2026]**

* 03. relational database schema for a Bank is given below:

  ```

  Bank(Br_Name, Br_City, Assets, Acc_name, Acc_Num, Balance)

  ```

  (a). Identify the Functional Dependencies, decompose/normalize the schema up to **3NF**, and explicitly point out the **Primary Keys** and **Foreign Keys** for each normalized table.

  (b). Show the final structured design and clearly state the technical reasons why your decomposed schema is in a good form. **(2 times)** **[Bangladesh Bank-2025]**

* 04. Suppose that we have a relational database with the following tables. Underlined attributes represent primary keys:
  * Movies (mid,title,year)
  * People (pid,name)
  * Genres (gid,genre)
  * HasRole (pid,mid,role)
  * HasGenre (gid,mid)
  Write an SQL query to return the number of movies that are romantic comedies. **[Bangladesh Bank-2023]**

* 05. A Bank schema is given below:

  `Bank(Br_Name, Br_City, Assets, Acc_name, Acc_Num, Balance)`

  (a) Provided and Normalize and point out Primary and Foreign Key?

  (b) Show that is the schema and state that why your schema is in good form. **[Bangladesh Bank-2025]**

* 06. Consider the following relation:

  `Sales(sales_id, salesman, region, sale_amount, sale_date)`

  Write an SQL query to display the region, average sale amount, and total number of sales for each region where: The average sale amount exceeds BDT 50,000 and the total number of sales in that region is at least 5. **[SO-2025]**

* 07. Explain the concept of ACID properties in a database transaction. Describe how each property—Atomicity, Consistency, Isolation, and Durability—ensures the reliability and integrity of a database system. **(2 times)** **[SO-2025]**

* 08. Explain the differences between Second Normal Form (2NF) and Third Normal Form (3NF) with examples. **[BPSC-2025]**

* 09. Given a Patient table in a hospital database below.

  | Patient_ID | Disease_Name |
  | ---------- | ------------ |
  | 1          | Covid-19     |
  | 2          | Dialysis     |
  | 3          | Covid-19     |
  | 4          | Dengue       |

  Write down an SQL query to display the total number of patients under each disease category. **[BPSC-2025]**

* 10. Given the following two tables (Students and Marks) in a database, write down the output of the given SQL queries and write down the SQL queries for the outputs.

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

  (v) List all the subject names. **[BPSC-2025]**

* 11. (a) Design an ER diagram for a library management system where:

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

  (c) Why normalization is required in Database? Write shortly about 3NF. **[BPSC-2025]**

* 12. (a) What is the Internet of Things (IoT)? Explain its applications.

  (b) What is Cloud Computing and its relationship with IoT?

  (c) Compare Static Website and Dynamic Website.

  (d) What is DBMS? Mention its major functions.

  (e) Explain HTTP and HTTPS.

  (f) What is Authentication? **[BPSC-2026]**

* 13. SQL OUTPUT Problem: Find Employee salary from a table where salary more than 5000. **[BCIC-2025]**

* 14. Who know how they are built internally?

  What is SQL?

  The scan shows the SQL question as Question 4; the preceding wording belongs to Question 3's printed answer. **[BBA-2025]**

* 15. Write an SQL query to find duplicate names in the employee table. **[BBA-2025]**

* 16. Given two tables:

  `Students(studentid, name, ...)`

  `Enrollment(studentid, course, grade)`

  (a) Write an SQL query to retrieve all student names, their courses, and grades.

  (b) Write an SQL query to retrieve names of students who obtained grade 'A'. **[BUET-2025]**

* 17. Write SQL code to get duplicate names from employee table. **[BCC-2025]**

* 18. Define Normalization? Explain 1NF and 2NF. **(2 times)** **[Narayanganj City Corporation-2025]**

* 19. Draw an Entity-Relationship (ER) diagram for NCC showing its four departments (Admin, Finance, Service, and English). Clearly mention entities, attributes, and relationships. **[Narayanganj City Corporation-2025]**

* 20. SQL Query:

  Write SQL queries demonstrating the following JOIN operations:

  (a) INNER JOIN

  (b) LEFT JOIN

  (c) RIGHT JOIN

  (d) FULL JOIN **[BREB-2025]**

* 21. How many processes of Transaction complete? **[BREB-2025]**

* 22. Given Four tables:

  ```
  Employee (empno(PK), empname, monthlysalary,
            deptno, mgrno(FK))

  Department (deptno, deptname, deptlocation)

  Course (crscode(PK), crsdesc,
          crscategory, crsduration)

  Offering (offbegdate, crscode fk,
            offeringlocation, empno fk)
  ```

  Write query for:

  (a) Find Departments with Average Monthly Salary Greater than 1000.

  (b) Find Courses with More Than 2 Offerings. **[Petrobangla-2024]**

* 23. Why need ER Diagram? Define Normalization also describe its types. **[Biman Bangladesh Airlines-2026]**

* 24. You are designing a database for a Library. Explain the relationship between a "Book" table and a "Borrower" table. Is it 1-to-1, 1-to-Many, or Many-to-Many? Justify your answer. **(2 times)** **[AP-2026]**

* 25. Two separate threads are initialized with the exact same instance of Counter Subsystem and run concurrently to completion.

  State definitively whether the final value of `transactionCounter` is guaranteed to be exactly 2000.

  Name the specific multithreading hazard that occurs here and explain the low-level mechanical steps that cause this behavior.

  The associated `CounterSubsystem` program begins on PDF page 15; part of the code is cut off. **[AP-2026]**

* 26. Consider the following two concurrent transactions operating on two data items, X and Y:

  Transaction T₁: Read(X), Write(X), Read(Y), Write(Y)

  Transaction T₂: Read(Y), Write(Y), Read(X), Write(X)

  Where the operations are executed:

  | Step | Operation |
  | ---- | --------- |
  | 1    | R₁(X)     |
  | 2    | W₁(X)     |
  | 3    | R₂(Y)     |
  | 4    | W₂(Y)     |
  | 5    | R₁(Y)     |
  | 6    | W₁(Y)     |
  | 7    | R₂(X)     |
  | 8    | W₂(X)     |

  (i) Draw the precedence (serialization) graph for the above schedule.

  (ii) Determine whether the schedule is conflict serializable. Justify your answer.

  (iii) If it is serializable, specify the equivalent serial schedule.

  (iv) If Two-Phase Locking (2PL) is used, discuss whether a deadlock can occur. **[AP-2026]**

* 27. Given the Student and Course tables:

  ```
  Student(StudentID, StudentName, CourseID, ...)
  Course(CourseID, CourseName, Enrolment, ...)
  ```

  (a) Find Student information.

  (b) Find the courses and the number of students where enrolment is less than or equal to 30. **[ICB Securities-2026]**

* 28. (a) What is the Internet of Things (IoT)? Mention its applications.

  (b) Compare Static Website and Dynamic Website.

  (c) What is DBMS? Explain its major functions.

  (d) Differentiate between HTTP and HTTPS. **[BPSC-2026]**

* 29. Two separate threads are initialized with the exact same instance of Counter Subsystem and run concurrently to completion. State definitively whether the final value of `transactionCounter` is guaranteed to be exactly 2000. Name the specific multithreading hazard that occurs here and explain the low-level mechanical steps that cause this behavior. **[AP-2026]**

* 30. Consider a concurrent transaction schedule involving two data items, X and Y:
     - **T1:** Read(X), Write(X), Read(Y), Write(Y)
     - **T2:** Read(Y), Write(Y), Read(X), Write(X)

     Describe how the standard 2PL protocol treats these transactions. Contrast with Strict 2PL. **[AP-2026]**

* 31. Discuss different types of relations in DBMS. **[AP-2024]**

* 32. Assuming an Employees table with structure `employee_id`, `employee_name`, `department_id`, and `salary`, write queries:
      - To find the total number of employees in each department.
      - To calculate the average salary across all employees in the organization. **[AP-2024]**

* 33. Suppose we have a relational database with five tables:

     ```text
     S(sid, A, ...)
     T(tid, B)
     Tid(U_id, C)
     U(id, R(sid, tid, D))
     Q(tid, uid, E)
     ```

     Here, R implements a many-to-many relationship between the entities implemented with tables S and T, and Q implements a many-to-many relationship between the entities implemented with tables T and U.
     - (A) Write an SQL query that returns all records of the form `sid, uid`, where `sid` is the key of an S-record and `uid` is the key of a U-record, and these two records are related through the relations R and Q. Use `SELECT` and not `SELECT DISTINCT` in your query.
     - (B) Write an SQL query that returns records of the form `A, C`, where the A-value is from an S-record and the C-value is from a U-record, and these two records are related through the relations R and Q. Use `SELECT` and not `SELECT DISTINCT` in your query.

     **[The table notation is reproduced as printed; see original PDF page 6 if interpreting it as a schema.]** **[AP-2023]**

* 34. Suppose that we have a relational database with the following tables. Underlined attributes represent primary keys:
     - Movies (mid, title, year)
     - People (pid, name)
     - Genres (gid, genre)
     - HasRole (pid, mid, role)
     - HasGenre (gid, mid)

     Write an SQL query to return the number of movies that are romantic comedies. **[Bangladesh Bank-2023]**

* 35. What is the full meaning of SQL? List the aggregate functions. Write SQL query of a table and its output. **[AP-2020]**

* 36. A relational database schema for a Bank is given below: `Bank(Br_Name, Br_City, Assets, Acc_Name, Acc_Num, Balance)`.
     - (a) Identify the Functional Dependencies, decompose/normalize the schema up to 3NF, and explicitly point out the Primary Keys and Foreign Keys for each normalized table.
     - (b) Show the final structured design and clearly state the technical reasons why your decomposed schema is in a good form. **[Bangladesh Bank-2025]**

* 37. What is Dynamic ARP Inspection (DAI)? How does it detect and prevent ARP spoofing attacks? Explain how Dynamic ARP Inspection (DAI) uses the DHCP snooping binding database to prevent ARP spoofing attacks in a switched enterprise network. **[ANE-2026]**

* 38. Consider `Employees (EmpID, Name, Department, Salary)`. Write an SQL query to retrieve employees whose salaries are greater than the average salary of their respective departments. **[ANE-2026]**

* 39. A high traffic web application suddenly begins failing with database connection timeouts under peak load. At the same time, the underlying Linux OS kernel hosting the database reports "too many open files" error and network socket exhaustion. Explain the root cause of this failure at the Linux OS kernel level. **[RAKUB-2026]**

* 40. Explain the distinct filtering behaviors of a WHERE clause versus a HAVING clause within a SQL statement containing an aggregate execution layout. **[RAKUB-2026]**

* 41. What is JDBC? Explain the steps required to connect a Java application to a MySQL database. **[O-2026]**

* 42. Describe the SQL Injection and Cross-Site Scripting (XSS) web security threats and suggest preventive measures for each. **[O-2026]**

* 43. An institute wants to create a database table named `STUDENT` to store student information. The table should include the columns Roll Number, Name, Department, Email, and Admission Date. Specify the most appropriate SQL data type for each column and identify which column should be defined as the Primary Key, giving a brief justification for your choice. **[O-2026]**

* 44. Consider a STUDENTS table with the following attributes: `StudentID, Name, Department, Marks (10 Marks)`:
      - (I) Write an SQL query to display only `StudentID, Name, and Marks` for students scoring more than 80 marks.
      - (II) Write an SQL query to count how many students scored more than 80 marks in each Department. **[O-2026]**

* 45. What are the different types of relationships in a relational database? Explain each with examples. **[O-2026]**

* 46. Storage technology selection directly impacts banking operations. Server A will host the Core Banking Database. Server B will host 10 years of immutable archive data. Compare Hard Disk Drives (HDD) and Solid State Drives (SSD). **[O-2026]**

* 47. You have table `EMPLOYEES (ID, Name, DeptID)` and table `DEPARTMENTS (DeptID, DeptName)`. Write the logical steps for pseudo-SQL logic to get a list of Employee Names who work in "IT". **[O-2026]**

* 48. Consider the following relation: `Employee(EmpID, Name, Department, Salary)`. Write an SQL query to retrieve the Department, the total number of employees, and the average salary for each department. The output should display one record for each department. **[SO-2026]**

* 49. Draw and clearly describe a step-by-step flowchart for a User Login system. Your login must include:
     - Taking a Username and Password as input.
     - Checking the database.
     - If correct: Granting access.
     - If wrong: Adding 1 to a "failed attempts counter."
     - Access denied blocks the account if the counter reaches 3. **[SO-2026]**

* 50. What is Normalization? How 1NF and 2NF works in database? Give examples. **[SO-2026]**

* 51. A database has a Managers table and an Employees table. The Employees table references the Managers table using a Foreign Key. The database is set to `ON DELETE CASCADE`.
      - (a) Explain what `ON DELETE CASCADE` means in simple English.
      - (b) If you delete one Manager from the database, what will automatically happen to all Employees under that manager?
      - (c) Explain why this is very dangerous in a real banking system. What is the best practice and how does it fix this danger? **[SO-2026]**

* 52. Consider the following relation: `Sales(sales_id, salesman, region, sale_amount, sale_date)`. Write an SQL query to display the region, average sale amount, and total number of sales for each region where the average sale amount exceeds BDT 50,000 and the total number of sales in that region is at least 5. **[SO-2025]**

* 53. What does the Consistency property in ACID guarantee during a bank fund transfer transaction? You are designing the schema for a Savings_Accounts table. Write the specific SQL constraint clause to ensure that the `current_balance` column can never drop below zero. **[AE-2026]**

* 54. নারী উদ্যোক্তা উন্নয়নে সামাজিক যোগাযোগ মাধ্যমের ভূমিকা। **[ADA-2026]**

* 55. Earthquake Risk management and mitigation. **[ADA-2026]**

* 56. Consider the relation `Sales(sales_id, salesman, region, sale_amount, sale_date)`. Write an SQL query to display the region, average sale amount, and total number of sales for each region where the average sale amount exceeds BDT 50,000 and the total number of sales is at least 5. **[SO-2025]**

* 57. Explain the concept of ACID properties in a database transaction and describe how each property ensures reliability and integrity. **[SO-2025]**

* 58. Technical Section:

  * **(ক)** Write a program to find the largest element from an array containing 10 elements.


  * **(খ)** SQL query to find duplicate names from an employee table.


  * **(গ)** What is an API? Protocol for sending email? DNS port number? Private IP range for Class B? Write a program to print even numbers from 1 to $n$? Why is NAND a universal gate? Draw a flowchart to display odd numbers between 1 and $n$. **[BCC-2025]**

* 59. Write an SQL query to find duplicate names from an employee table. **[BBA-2025]**

* 60. Short questions on SQL, API, recursion, and DNS port number.


  Here are questions 1, 2, and 3 from the Bridge Authority (AME) subjective section on page 13: **[BBA-2025]**

* 61. NCC has 4 dept (Admin, Finance, Service, Eng) Draw ER diagram with relationship? **[Narayanganj City Corporation-2025]**

* 62. Consider that you are given a database of a "Pet Society" with the following relations, Animals(ID: integer, Name: string, PrevOwner: string, DateAdmitted: date, Type: string) Adopter(PSIN: integer, Name: string, Address: string, Other Animals: integer) Adoption(AnimalID: integer, PSIN: integer, AdoptDate: date, chipNo: integer) Give a sql query that list total number of adoptions on June 30, 2024 for each animal type **[O-2024]**

* 63. Given Four table: Department(deptno, deptname, deptlocation), Employee(empno(PK), empname, monthlysalary, deptno, mgrno(FK)), Course(crscode(pk), crsdesc, crscategory, crsduration), Offering(offeringno(pk), begindate, crscode(fk), offeringlocation, empno(fk)) Write query for:
  * (a) Find Departments with Average Monthly Salary Greater than 1000.
  * (b) Find Courses with More Than 2 Offerings. **[Petrobangla-2024]**

* 64. What is SaaS and multi-tenant architecture? How are they related? What are the advantages and disadvantages of multi-tenancy? For a multi-vendor e-commerce application, you can choose a database architecture where you can put all the vendors in a single database or each vendor in a separate database. Which architecture will you follow and why? **[SO-2024]**

* 65. Let a database has two tables, Customers and Orders. The following figure shows the partial data of these two tables. Based on this partial data, explain Inner, Left, Right and Full join. Show the result set of each join operation. **[SO-2024]**

* 66. Briefly describe primary key, foreign key and index in relational database and their relationship. Do you think database indexing always makes applications faster? Explain your answer. **[SO-2024]**

* 67. Various types of relationship in database? Define them. **[AP-2024]**

* 68. Given two tables `DEPARTMENT` and `EMPLOYEE`, write SQL queries for:

  ```sql
  CREATE TABLE DEPARTMENT (
      DEPTCODE INT(10),
      DeptName CHAR(30),
      LOCATION VARCHAR(33)
  );

  CREATE TABLE EMPLOYEE (
      EmpCode INT(4),
      EmpFName VARCHAR(15),
      EmpLName VARCHAR(15),
      Job VARCHAR(45),
      Manager CHAR(4),
      HireDate DATE,
      Salary INT(6),
      Commission INT(6),
      DEPTCODE INT(2)
  );
  ```
  * a) Display EMPFNAME and "Total Salary" for each employee.


  * b) Display EMPLNAME, EMPFNAME, DEPTNAME, LOCATION from EMPLOYEE and DEPARTMENT tables. Make sure the result are in ascending order on the EMPFNAME and LOCATION of the department.


  * c) Find the average salary of each employee in each department.


  * d) Return a list of all employees who are paid above the average salary.


  * e) List of all departments, ordered by the number of employees in each department. **[AP-2024]**

* 69. What is Cryptography? Distinguish between Symmetric Encryption and Asymmetric Encryption with example. Draw a diagram and discuss how Public Key (Asymmetric) Encryption using Hash function ensures Data Confidentiality, Data Integrity, Authenticity of sender and receiver in e-commerce or online transactions. **[SO-2023]**

* 70. What are the key differences among Database, Data Warehouse, and Data Mining? Can you provide examples that illustrate how each of these concepts is applied in real-world scenarios? **[SO-2023]**

* 71. To achieve a '0-bit data loss' for its $24\times7\times365$ banking operation, what steps or technology should an online bank employ to safeguard its data against any potential threats of data loss? **[SO-2023]**

* 72. What is the degree of relation? **[BCC-2023]**

* 73. Functional dependency is used in which normalizations? **[BCC-2023]**

* 74. Which join is used for including non-matching records in the output? **[BCC-2023]**

* 75. What does the "D" stand for in the ACID property in databases? **[BCC-2023]**

* 76. What is the trigger? Why do we use triggers in databases? Write with an example? **[ICB Asset Management-2024]**

* 77. Given 2 Tables: Department (`dept_id`, `Salary`, `dept_name`) and Employee (`dept_id`, `emp_name`). Write SQL query for: যাদের salary গড় 50000 থেকে বেশী তাদের নাম, আইডি দেখাও। **[BTCL-2024]**

* 78. Mysql database এর data backup করাও data restore করার command লিখ। **[BTCL-2024]**

* 79. Analyze the output of the following SQL `SELECT department_name, AVG(salary) AS average_salary FROM employees e` **[ANE-2023]**

* 80. What is database normalization? Write down the types of database normalization. **[WZPDCL-2023]**

* 81. Differentiate between primary key and foreign key. What is trigger and how it works? **[WZPDCL-2023]**

* 82. Draw an ER diagram of BPL (Team, Player, Game, Captain) [ADBA-2022] **[ADBA-2022]**

* 83. What is the trigger, when it's used, and advantages [ADBA-2022] **[ADBA-2022]**

* 84. Write short notes on ACID properties [ADBA-2022] **[ADBA-2022]**

* 85. Weak entity type VS strong entity type, show example in an ER diagram. [ADBA-2022] **[ADBA-2022]**

* 86. Why do we need database normalization? [Krishi_Biponon_Ministry-2022] **[Krishi Biponon Ministry-2022]**

* 87. How can you define the E-R model in DBMS? [Krishi_Biponon_Ministry-2022] **[Krishi Biponon Ministry-2022]**

* 88. Explain the difference between data administrator and database administrator. [Krishi_Biponon_Ministry-2022] **[Krishi Biponon Ministry-2022]**

* 89. Describe the advantages and disadvantages of DBMS-provided and Application-provided security. [Krishi_Biponon_Ministry-2022] **[Krishi Biponon Ministry-2022]**

* 90. What do you mean by roll back and roll forward? [Krishi_Biponon_Ministry-2022] **[Krishi Biponon Ministry-2022]**

* 91. SQL query to insert into a table. [NSDA-2022] **[NSDA-2022]**

* 92. `Employee(empno(PK), empname, empsal, deptno(FK))`


  `Department(deptno(PK), deptname, deptdate, empno(FK))`


  A SQL query to find the deptname whose employee average salary is greater than the company average salary. [NESCO 2021] **[NESCO-2021]**

* 93. a) Describe the cloud-based database briefly. [Krishi_Biponon_ministry 2022]
  b) What do you mean by national data center? Define its purpose. [Krishi_Biponon_ministry 2022] **[Krishi Biponon Ministry-2022]**

# 6. Computer Architecture & Microprocessor

* 01. Explain the difference between compiler and interpreter **(2 times)** **[O-2026]**

* 02. Arrange the following in the correct chronological order of a computer's boot process: (OS Kernel Load, BIOS/UEFI POST, MBR/GPT Lookup, User Login, Driver Initialization). **[O-2026]**

* 03. Explain the difference between direct, immediate, and register addressing modes in the 8086 microprocessor. **(2 times)** **[SO-2025]**

* 04. Write down the names of different stages of instruction pipelining in a multi-cycle datapath architecture. What is a data-hazard in a pipelined datapath? **[BPSC-2025]**

* 05. (a) Define the term "SSD". Briefly describe the working principle of "SSD".

  (b) Compare CPU and GPU. **[BPSC-2025]**

* 06. (a) Differentiate between Vector Graphics and Raster Graphics.

  (b) Solve the following Knapsack problem.

  | Item   | 1  | 2  | 3  | 4  | 5  |
  | ------ | -- | -- | -- | -- | -- |
  | Value  | 20 | 15 | 12 | 14 | 20 |
  | Weight | 4  | 3  | 2  | 2  | 5  |

  Knapsack Capacity = 25.

  (i) Using the Fractional Knapsack method, find the maximum value.

  (ii) Determine the selected items and their order. **[BPSC-2026]**

* 07. Write advantage and disadvantage of direct mapping and associative mapping between cache memory and main memory. **[BCIC-2025]**

* 08. Difference between SRAM & DRAM also write Differences Cache Memory vs Flash Memory. **[BUET-2025]**

* 09. Given a code with a variable value `a = 85` and find its output.

  ```
  if a >= 90 print A;
  if a >= 80 print B;
  if a >= 70 print C;
  if a >= 60 print D;
  else print F;
  ```
   **[Petrobangla-2024]**

* 10. Write down the difference between Microprocessor & Microcontroller. **[Biman Bangladesh Airlines-2026]**

* 11. Suppose your dataset has missing values and noise. How would you preprocess it? **(2 times)** **[AP-2026]**

* 12. (a) Differentiate between Vector Graphics and Raster Graphics.

  (b) Consider the following Knapsack problem:

  | Item   | 1  | 2  | 3  | 4  | 5  |
  | ------ | -- | -- | -- | -- | -- |
  | Value  | 20 | 15 | 12 | 14 | 20 |
  | Weight | 4  | 3  | 2  | 2  | 5  |

  Knapsack Capacity = 25.

  (i) Using the Fractional Knapsack method, determine which items should be selected.

  (ii) Find the maximum value and explain the selection order. **[BPSC-2026]**

* 13. (a) Differentiate between Microprocessor and Microcontroller.

  (b) Write a program to generate the Fibonacci series using recursion. **[BPSC-2026]**

* 14. Given the following values, compute function point when all complexity adjustment factor (CAF) and weighting factors are average:
     - User Input = 50
     - User Output = 40
     - User Inquiries = 35
     - User Files = 6
     - External Interface = 4 **[AP-2023]**

* 15. If x is an integer and `x + 1/x = 17/4`, then the value of `x − 1/x` = ? **[Bangladesh Bank-2023]**

* 16. A computer's RAM has been upgraded from 8 GB to 16 GB, and its SSD capacity has been increased from 256 GB to 512 GB. Which upgrade allows the computer to run more applications simultaneously, and which upgrade allows it to store more data? **[Bangladesh Bank-2026]**

* 17. An engineering model is deployed to identify critical network hardware failures. Explain why an administrator must optimize for recall instead of precision if the business penalty for a missed failure is catastrophic. **[RAKUB-2026]**

* 18. Define Amdahl's law. How does it mathematically dictate the absolute maximum performance speedup a system can achieve when adding more CPU cores? **[RAKUB-2026]**

* 19. Compare RAM, ROM, cache memory, and secondary storage in terms of speed and usage. **[O-2026]**

* 20. Explain the difference between compiler and interpreter. **[O-2026]**

* 21. Arrange the following in the correct chronological order of a computer's boot process: (OS Kernel Load, BIOS/UEFI POST, MBR/GPT Lookup, User Login, Driver initialization). **[O-2026]**

* 22. Why do modern processor designs favor a multi-stage pipelined approach over a single-cycle implementation? **[SO-2026]**

* 23. Explain the difference between a "Compulsory Miss" (Cold Miss) and a "Capacity Miss" in cache memory. **[SO-2026]**

* 24. Consider the following Java program and determine the integer value printed by the execution of the `main()` method.

      ```java
      class Test {
          static int x = 5;

          public static int fun(int n) {
              if (n <= 1) {
                  return 1;
              }
              x = x + 2;
              return fun(n - 1) + x;
          }

          public static void main(String[] args) {
              System.out.println(fun(3));
          }
      }
      ```
   **[SO-2026]**

* 25. What are Compilers and Interpreters? Briefly describe their role and difference. Write some key points of advantages and disadvantages of Open Source Software. **[SO-2026]**

* 26. Distinguish between Preventive and Corrective maintenance with a real-world example for each in a data center environment. A critical system consists of three components (Power Supply, Motherboard, and Storage) connected in a series configuration. If each component has a reliability of 0.95, what is the total reliability of the system? **[AE-2026]**

* 27. Let M be a 3 × 3 real matrix with eigenvalues 1, 2, and 3. What is the determinant of the matrix `M² − M + I`, where I is the 3 × 3 identity matrix? **[AE-2026]**

* 28. :

  Arrange the following in the correct chronological order of a computer's boot process: (OS Kernel Load, BIOS/UEFI POST, MBR/GPT Lookup, User Login, Driver Initialization). **[O-2026]**

* 29. Explain the difference between direct, immediate, and register addressing modes in a microprocessor. **[SO-2025]**

* 30. Give abbreviations for the following: HTTP, SMTP, BIOS, ASCII, and DHCP. **[BBA-2025]**

* 31. A computer frequently restarts without warning during normal operation. What hardware-related issues might cause this, and how would you test them? **[Ministry of Land-2025]**

* 32. অ্যাড্রেসিং মোড (Addressing Mode) কী? এটি কেন ব্যবহার করা হয়? ৩ প্রকার Addressing mode এর উদাহরণ দাও। **[WZPDCL-2026]**

* 33. মেমরি হায়ারার্কি (Memory Hierarchy)-এর একটি চিত্র আঁকো এবং এর প্রতিটি স্তরের কাজ ব্যাখ্যা করো। **[WZPDCL-2026]**

* 34. How many total bits are required for a directly mapped cache with 16 KB of data and 4-word blocks assuming a 32 bit address? **[O-2024]**

* 35. Given as code with a variable value $a=85$ and finds its output **[Petrobangla-2024]**

* 36. What exactly is a microcontroller? What distinguishes a microprocessor from a microcontroller? Mention the differences between RISC and CISC microprocessors. **[SO-2024]**

* 37. Differentiate between 32-bit & 64-bit Microprocessor with example. What are the differences among Intel's i3, i5 & i7 Processors? Write down the specifications of a high-performance Laptop Computer. Why do you prefer SSD instead of HD? **[SO-2023]**

* 38. Difference among CPU Register, Cache Memory, Main Memory and Auxiliary/Secondary memory. What is the meaning of 2.40 GHz of a microprocessor? **[SO-2023]**

* 39. Write a program in any language that takes two matrices A and B as inputs. Ensure your code handles matrices of different dimensions.
  * a) Find a matrix C that is a multiplication of A and B.
  * b) Calculate the average of the elements of the both matrix.
  * c) Find the highest value of the elements in C matrix. **[SO-2023]**

* 40. Difference between compiler and interpreter. **[ICB Asset Management-2024]**

* 41. মাইক্রোকম্পিউটার উপাদান গুলো নামসহ আর্কিটেকচার অংকন। **[BTCL-2024]**

* 42. কোন memory processor এর কাছাকাছি থাকে? **[BTCL-2024]**

* 43. Write the concept of cache memory in the computer and how it changes the performance of the computer. **[BITAC-2023]**

* 44. What is dual channel RAM? Difference between Single channel and Dual channel RAM. **[BITAC-2023]**

* 45. You have given two $16 \times 16$ matrix but your processor support $8 \times 8$ matrices how you can multiply: Write algorithm. **[BGDCL-2024]**

* 46. In the context of data management, what are the primary differences between data replication and data backup? Provide real-world examples of when each is employed effectively. **[ANE-2023]**

* 47. What are the key hardware components that make up a typical server, and how do they contribute to its overall performance and functionality? **[ANE-2023]**

* 48. Discuss the factors that affect the Speed of a CPU. **[ANE-2023]**

* 49. A Software projects unadjusted function point = 180, <br>  value added fact = 0.87, <br>  Performance fact = 4. <br>  Calculate required effort in days? $[\text{Com } AP\text{-}2023]$ **[AP-2023]**

* 50. What is the use of cache memory? [Krishi_Biponon_ministry 2022] **[Krishi Biponon Ministry-2022]**

* 51. How can you define SSD? [Krishi_Biponon_ministry 2022] **[Krishi Biponon Ministry-2022]**

* 52. What is the function of GPU? [Krishi_Biponon_ministry 2022] **[Krishi Biponon Ministry-2022]**

* 53. What do you understand by the resolution of a computer screen? [Krishi_Biponon_ministry 2022] **[Krishi Biponon Ministry-2022]**

# 7. OOP

* 01. What is programming language? Give 4 examples. Difference between structured and OOP language. **(2 times)** **[ADA-2026]**

* 02. Consider the following Java code:
  ```java
  public class Class A {
      public void m1() {}
      public void m2(int i) {}
      public void m3(int i) {}
      public static void m4(int i) {}
  }
  public class Class B extends Class A {
      public static void m1(int i) {}
      public void m2(int i) {}
      public void m3(String s) {}
      public static void m4(int i) {}
  }

  ```


  Mention which of the methods overload, override, and hide superclass methods. What about the remaining method? **[Bangladesh Bank-2023]**

* 03. Draw a class diagram. A token-ring based local area network (LAN) is a network consisting of nodes in which network packets are sent around. Every node has a unique name within the network and refers to its next node. Different kinds of nodes exist: Workstations are originators of messages; servers and printers are network nodes that can receive messages. Packets contain an originator, a destination, and content, and are sent around on a network. A LAN is a circular configuration of nodes. **(2 times)** **[Bangladesh Bank-2023]**

* 04. Evaluate the challenges and prospects of managing the Rohingya refugee crisis in Bangladesh. How important is international cooperation, and what reforms or support mechanisms should be prioritized?

  ## Section 2 — Subject-Related Questions (ICT)

  Questions 6.1–6.15 | 10 Marks Each **[SO-2025]**

* 05. Write a program using any object-oriented language (e.g., C++ / Java / Python) to represent a Bank Account. Your program should include:

  - A class BankAccount with data members for account holder's name, account number, and balance.
  - Member functions to deposit() money, withdraw() money (ensuring sufficient balance), and display() account details.

  Demonstrate the concept of encapsulation by keeping data member’s private and providing appropriate public methods for accessing and modifying them. **[SO-2025]**

* 06. Explain the concept of polymorphism in Object-oriented Programming with example. **[BPSC-2025]**

* 07. (a) Suppose you are working with an array of size 10. It contains all the numbers from 1 to 10 exactly once in a random order. But accidentally, one of the numbers in the array got replaced by a zero (0). Write a C/C++ programme using functions, to restore the lost number.

  (b) What is polymorphism in the context of an object-oriented paradigm? Explain the method of overloading and method of overriding with suitable examples. **[BPSC-2025]**

* 08. Write down the difference between Structure and Class. **[BCIC-2025]**

* 09. Class/Interface implementation of code? **[BCIC-2025]**

* 10. What is OOP? Explain two feature with example? **(2 times)** **[Narayanganj City Corporation-2025]**

* 11. You have three access specifiers in Java object-oriented language. You have to find which access specifiers are worked with Public, Private and Protected Mode. If yes you have to write Y and if No you have to write N. **[Petrobangla-2024]**

* 12. Program: Write a C/C++ Program Swap two integer using call by value. **[Biman Bangladesh Airlines-2026]**

* 13. Explain the concept of Inheritance in Object-Oriented Programming. Name and briefly describe three common types of inheritance used in OOP. **(2 times)** **[AP-2026]**

* 14. What is Polymorphism? Discuss different types of Polymorphism with example. **[AP-2024]**

* 15. Consider the following Java code. Mention which of the methods overload, override, and hide superclass methods. What about the remaining method?

     ```java
     public class ClassA {
         public void m1() {}
         public void m2(int i) {}
         public void m3(int i) {}
         public static void m4(int i) {}
     }

     public class ClassB extends ClassA {
         public static void m1(int i) {}
         public void m2(int i) {}
         public void m3(String s) {}
         public static void m4(int i) {}
     }
     ```
   **[Bangladesh Bank-2023]**

* 16. What will be the output in C and Java code?
     - (i) C program code snippet.
     - (ii) Java program code snippet.

     **[The source lists snippets as prompts but does not supply their code.]** **[AP-2020]**

* 17. State the main purpose of Spanning Tree Protocol (STP) in Ethernet networks. Explain how switching loops occur in a network. Briefly explain how STP prevents switching loops. **[ANE-2026]**

* 18. Difference between compile-time polymorphism & run-time polymorphism. **[RAKUB-2026]**

* 19. Explain the concepts of Inheritance and Polymorphism in Java. Write a Java program to demonstrate method overriding. **[O-2026]**

* 20. Simplify the following Boolean expression using a 4-variable K-map: `F(A,B,C,D) = Σ m(0,3,5,7,8,10,11,12,13,14,15)`. Draw the K-map grid, clearly show your groupings (loops), and write the final simplified Sum-of-Products (SOP) expression. **[SO-2026]**

* 21. What is Object-Oriented Programming (OOP)? What are the main principles of OOP? What is the difference between Method Overloading and Method Overriding? **[SO-2026]**

* 22. Write a program using any object-oriented language (e.g., C++ / Java / Python) to represent a Bank Account. Your program should include:
     - (i) A class BankAccount with data members for account holder's name, account number, and balance.
     - (ii) Member functions to deposit money, withdraw money (ensuring sufficient balance), and display account details.
     - (iii) Demonstrate the concept of encapsulation by keeping data members private and providing appropriate public methods for accessing and modifying them. **[SO-2025]**

* 23. Simplify the following Boolean expression using a 4-variable K-map: `F(A,B,C,D) = Σ m(0,3,5,7,8,10,11,12,13,14,15)`. Draw the K-map grid, clearly show your groupings (loops), and write the final simplified Sum-of-Products (SOP) expression. `[Combined Bank SO IT — 25.07.2026]` **[AE-2026]**

* 24. Design a scalable big data analytics pipeline for an e-commerce platform that ingests real-time logs, stores petabyte-scale data, supports batch and stream processing, delivers near real-time recommendations, and runs large-scale machine learning models; from the following Hadoop ecosystem components — *MapReduce, HDFS, YARN, HBase, ZooKeeper, Pig, Hive, Mahout, Chukwa, Cassandra, Avro, Oozie, Flume, Sqoop* — select any five and explain the role of each component in this system. **[AE-2026]**

* 25. Write a program using any object-oriented language (e.g., C++ / Java / Python) to represent a Bank Account with encapsulation, deposit, withdraw, and display methods. **[SO-2025]**

* 26. Explain how encapsulation and inheritance are advantageous in object oriented programming. **[O-2024]**

* 27. Suppose we want to develop software for a graphic package and we are given the task to implement circle class. The circle class has to be translatable from its origin. And it should also be able to give perimeter and area of the circle. Identify the data and method requirements for the class and give the data flow of translation method. **[O-2024]**

* 28. You have three access specifiers in java object oriented language. You have to find which access specifiers are worked with Public, Private and Protected Mode. If yes you have to right Y and If No you have to write N. **(2 times)** **[Petrobangla-2024]**

* 29. What is polymorphism? Explain different types of polymorphism with example. **[AP-2024]**

* 30. What do you mean by platform-independent software? Discuss Platform-independent software: Java with example. **[SO-2023]**

* 31. The statement that allows you to define a block of code to be tested for exceptions while it is being executed. **[BCC-2023]**

* 32. What are the inbuilt classes? **[BCC-2023]**

* 33. A feature of object-oriented programming languages that allows a specific routine to use variables of different types at different times, is called in OOP? **[BCC-2023]**

* 34. Which variable violates the principle of encapsulation? **[BCC-2023]**

* 35. Which type of members can't be accessed in derived classes of a base class? **[BCC-2023]**

* 36. What is the syntax for calling a static method in a class? **[BCC-2023]**

* 37. Which level of abstraction specifies the data and relationships between data? **[BCC-2023]**

* 38. Difference between while and do while loop. **[ICB Asset Management-2024]**

* 39. Local Loopback address কি? কোন command ব্যবহার করে connectivity test করা হয়। **[BTCL-2024]**

* 40. Advantage of OOP over traditional programming with example. **[O-2023]**

* 41. What is constructor in object oriented programming? Write the properties of it. **[WZPDCL-2023]**

* 42. a) Determine whether a given number is prime or not. [Krishi_Biponon_Ministry-2022]
  b) Print the following matrix using for loop. [Krishi_Biponon_Ministry-2022] **[Krishi Biponon Ministry-2022]**

* 43. What is the difference between "call by value" and "call by reference"? [Krishi_Biponon_Ministry-2022] **[Krishi Biponon Ministry-2022]**

* 44. When is a constructor invoked in OOP? [Krishi_Biponon_Ministry-2022] **[Krishi Biponon Ministry-2022]**

* 45. Differentiate between interpreter and compiler. [Krishi_Biponon_Ministry-2022] **[Krishi Biponon Ministry-2022]**

# 8. Software Engineering

* 01. Flowchart of ATM PIN Success/Failure Process. **(2 times)** **[ADA-2026]**

* 02. Software Testing Levels and How They Complement Each Other. **(2 times)** **[ADA-2026]**

* 03. What is the difference between functional and non-functional requirements? What is requirement validation? **(3 times)** **[O-2026]**

* 04. Critically analyze the limitations of the Waterfall model and explain how Agile methodologies address those limitations **(2 times)** **[O-2026]**

* 05. Write down the differences between Agile model and Waterfall model in Software development. What is white box testing? **[BPSC-2025]**

* 06. (a) What are the advantages and disadvantages of the Agile Model compared to the Waterfall Model in software development?

  (b) Distinguish between Generative AI and Large Language Models (LLMs). **[BPSC-2025]**

* 07. Difference between Black box testing and white box testing? Why suitable for Integration testing? **[Narayanganj City Corporation-2025]**

* 08. Given scenario of software engineering (Unit test, Regression Test, Smoke Test, Integration testing, Load Testing). Write the name of the testing and whether it is functional? Non-functional or both. **[Petrobangla-2024]**

* 09. What is the difference between Whitebox and Blackbox testing? **[Biman Bangladesh Airlines-2026]**

* 10. What is software requirement specification? **[Biman Bangladesh Airlines-2026]**

* 11. Write a C/C++ program sum of 7 digit from given number also draw flow chart. **[Biman Bangladesh Airlines-2026]**

* 12. Explain the concept of the Software Development Life Cycle (SDLC) and describe its main phases. **(2 times)** **[AP-2026]**

* 13. What is Version Control (e.g., Git)? Explain the specific difference between "Committing" code and "Pushing" code. **(2 times)** **[AP-2026]**

* 14. Assume a banking application wants to add a fingerprint system for their App. Write one functional requirement and one security requirement. **(2 times)** **[AP-2026]**

* 15. Which system did you build for a real-life software project? What problems did you face during that time and how did you solve this? **[AP-2024]**

* 16. Write a comprehensive essay on **"Digital Financial Literacy"**. **[AP-2023]**

* 17. What is Agile Methodology? Difference between Agile Model and Waterfall Model. **[AP-2020]**

* 18. A software company has been hired to develop an Online Library Management System for a university. The librarian wants the system to be delivered in phases so that feedback from users can be incorporated after each release. As a software developer, identify the most suitable Software Development Life Cycle (SDLC) model for this project. Justify your choice by mentioning two advantages of the selected model. **[O-2026]**

* 19. What are the main phases of the Software Development Life Cycle (SDLC)? Explain each phase briefly. **[O-2026]**

* 20. Critically analyze the limitations of the Waterfall model and explain how Agile methodologies address those limitations. **[O-2026]**

* 21. Explain the difference between Unit Testing and Integration Testing. **[SO-2026]**

* 22. Describe the phases of the Software Development Life Cycle (SDLC). **[SO-2026]**

* 23. In each of the following questions, a related pair of words is given in capital letters. Select the option that best expresses a relationship similar to that expressed in the original pair.

      **(i) FAMISHED : HUNGRY :: ______ : ______**
      - A) wealthy : poor
      - B) meticulous : careful
      - C) treacherous : reliable
      - D) agile : clumsy

      **(ii) CACOPHONY : SOUND :: ______ : ______**
      - A) chorus : melody
      - B) aroma : smell
      - C) glare : light
      - D) flavor : taste **[AE-2026]**

* 24. A banking application requires users to enter a 4-digit PIN for login. Explain how you would test it. **[SO-2025]**

* 25. What are the difference between black box testing and white box testing? Why black box testing suitable for intration testing? **[Narayanganj City Corporation-2025]**

* 26. You are required to convert a 12-bit digital number to an analog voltage over the voltage range of 0 to 3.3V with a Digital-to-Analogue Converter (DAC), What is the resolution of the analog output? **[O-2024]**

* 27. Given scenario of software engineering (Unit test, Regression Test, Smoke Test, Integration testing, Load Testing). Write the name of the testing and whether it is functional/Non-functional or both. **[Petrobangla-2024]**

* 28. What do you understand about software quality assurance (SQA)? While purchasing a software system for your company, as a SQA team leader what aspects will you look into for a quality software. **[SO-2024]**

* 29. You are asked to lead a team of software engineers to develop an application software system for your company and deploy it as fast as possible. You need to gather user requirements, design, develop, test and then deploy the system. Between Waterfall Approach and Incremental Approach, which software development approach will you take for your software project? Explain your answer. **[SO-2024]**

* 30. Write briefly on a real life software project that you have done by self. What are the challenges you faced and how did you solve those? **[AP-2024]**

* 31. What is SDLC? Explain every phase of SDLC. **[ICB Asset Management-2024]**

* 32. Which SDLC is better between Agile model and waterfall model. **[O-2023]**

* 33. What is MVC? Draw MVC pattern. **[WZPDCL-2023]**

* 34. Write the names of a few architectures design pattern of software development. **[WZPDCL-2023]**

* 35. Explain the software development life cycle (SDLC). [Krishi_Biponon_Ministry -2022] **[Krishi Biponon Ministry-2022]**

* 36. Which factors are to be considered as software pricing? [Krishi_Biponon_Ministry 2022] **[Krishi Biponon Ministry-2022]**

* 37. What is API? Explain with example. [Krishi_Biponon_Ministry 2022] **[Krishi Biponon Ministry-2022]**

# 9. Web Technologies

* 01. What are SOAP and RESTful APIs in web services? State one main difference between SOAP and REST in terms of how they exchange data. **(3 times)** **[SO-2025]**

* 02. Imagine a government agency is developing an AI-based citizen service chatbot that can automatically generate responses, summarize documents, and provide policy information to citizens. Explain how Generative AI can be used to power such a system, and how Explainable AI (XAI) techniques can ensure that its responses are transparent, reliable, and accountable. **(2 times)** **[SO-2025]**

* 03. What is an API? **[BBA-2025]**

* 04. What is API? **[BCC-2025]**

* 05. Identify and explain the three main components of the following URL: `https://www.bb.org.bd/index.php`. **[Bangladesh Bank-2026]**

* 06. A computer can ping `8.8.8.8` but cannot access websites using domain names. Explain the likely cause and describe how you would diagnose and resolve the problem using standard network utilities. **[ANE-2026]**

* 07. Describe any two key differences between the HTTP GET and HTTP POST methods used for communication between a web browser and a web server. **[O-2026]**

* 08. What do the following specific HTTP status codes mean? Write down the exact standard text phrase for each:
      - (a) 200
      - (b) 403
      - (c) 503 **[SO-2026]**

* 09. Read the three real-world web development scenarios below. For each scenario, identify the single most appropriate HTTP Status Code from the provided list that the server should return.

     **Codes to choose from:** 204, 301, 400, 403, 503.
     - **(i) Scenario A:** A client sends a POST request to create a new user, but the JSON payload is malformed and missing a required bracket, making it impossible for the server to parse the data.
     - **(ii) Scenario B:** A user is successfully logged in, but they attempt to access a `/admin/settings` endpoint. They only have standard user privileges, not administrator rights.
     - **(iii) Scenario C:** A client successfully sends a DELETE request to remove a photo. The photo is deleted, and the server needs to acknowledge the success but has no actual data or message to send back in the response body. **[AE-2026]**

* 10. Two machines, A and B, manufacture 60% and 40% of the total daily production of a factory, respectively. It is known that 2% of the items produced by machine A are defective, and 5% of the items produced by machine B are defective. If a randomly chosen item from the daily production is found to be defective, what is the probability (expressed as a decimal) that it was produced by machine B? **[AE-2026]**

* 11. Imagine a government agency developing an AI-based citizen service chatbot. Explain how Generative AI can power such a system, and how Explainable AI (XAI) techniques can ensure transparency, reliability, and accountability. **[SO-2025]**

* 12. Why is CSS used in a website? [NESCO 2021] **[NESCO-2021]**

* 13. Automatic IP assigning protocol without internet -- URL to IP conversion -- Server to Client mail fetch -- MAC to IP conversion -- **[Institute Unknown-Year Unknown]**

# 10. Operating System

* 01. Your friend device is slow performing so what should you take step in your task manager? **(2 times)** **[ADA-2026]**

* 02. Define Virtualization. Explain the role of the Hypervisor and the difference between a Virtual Machine (VM) and a Container **(2 times)** **[O-2026]**

* 03. Consider the following snapshot of a system running the Banker's Algorithm with 5 processes (P₀ through P₄) and 3 resource types: A (10 instances), B (5 instances), and C (7 instances) at time T₀:

  **Allocation Matrix**

  | Process | A | B | C |
  |---|---|---|---|
  | P₀ | 0 | 1 | 0 |
  | P₁ | 2 | 0 | 0 |
  | P₂ | 3 | 0 | 2 |
  | P₃ | 2 | 1 | 1 |
  | P₄ | 0 | 0 | 2 |

  **Max Matrix**

  | Process | A | B | C |
  |---|---|---|---|
  | P₀ | 7 | 5 | 3 |
  | P₁ | 3 | 2 | 2 |
  | P₂ | 9 | 0 | 2 |
  | P₃ | 2 | 2 | 2 |
  | P₄ | 4 | 3 | 3 |

  **Available**

  | A | B | C |
  |---|---|---|
  | 3 | 3 | 2 |

  (a) Find and state the content of the **Need Matrix**.

  (b) Determine whether the system is in a **Safe State** or **Unsafe State**. If safe, provide the safe execution sequence.

  **[10]** **(2 times)** **[Bangladesh Bank-2025]**

* 04. Banker’s Algorithm: 5 processes P₀ through P₄; 3 resource types A (10 instances), B (5 instances), and C (7 instances).

  (a) Need matrix

  (b) Safe state or Unsafe

  Snapshot at time T₀:

  | Process | Allocation (A B C) | Max (A B C) |
  | ------- | ------------------ | ----------- |
  | P₀      | 0 1 0              | 7 5 3       |
  | P₁      | 2 0 0              | 3 2 2       |
  | P₂      | 3 0 2              | 9 0 2       |
  | P₃      | 2 1 1              | 2 2 2       |
  | P₄      | 0 0 2              | 4 3 3       |

  Available (A B C): 3 3 2 **[Bangladesh Bank-2025]**

* 05. Consider a logical address space of 512 pages, each of 2-KB page size, mapped onto a physical memory containing 128 frames.

  (a) How many bits are required in the logical address?

  (b) How many bits are required in the physical address? **[SO-2025]**

* 06. Explain the concept of thrashing in an operating system, describing how it occurs in a demand-paged virtual memory system and how it impacts CPU utilization and overall system performance. **(3 times)** **[SO-2025]**

* 07. Compare "Paging" and "Segmentation" memory management technique? **[BPSC-2025]**

* 08. There are 3 tasks P1, P2, and P3. The arrival time and duration of each task is given below. Apply the round-robin scheduling algorithm with quantum size = 20 to schedule the tasks in a single-core machine. Calculate the turnaround time for each task. (All tasks have the same priority.)

  | Task | Arrival Time (ms) | Duration (ms) |
  | ---- | ----------------- | ------------- |
  | P1   | 0                 | 40            |
  | P2   | 5                 | 40            |
  | P3   | 10                | 20            |
   **[BPSC-2025]**

* 09. (a) Write about notes on:

  (i) Virtual memory (ii) Cache memory

  (b) Use the Karnaugh Map to simplify the following function.

  \\[ F(A,B,C)=\bar A\bar B\bar C+A\bar B\bar C+A\bar BC+ABC \\] **[BPSC-2025]**

* 10. (a) Consider a computer system with the following specifications:

  - Physical memory (RAM): 4 GB
  - Page size: 4 KB
  - Virtual address space: 32 bits
  - Page table entry size: 8 bytes

  (i) How many pages are there in the virtual address space? Explain your answer.

  (ii) What is the size of the page table? Explain your answer.

  (b) What is process? Describe different states of a process.

  (c) Define context switch with proper example.

  (d) What is cache memory? Explain the concepts of:

  (i) Cache hit (ii) Cache miss **[BPSC-2025]**

* 11. (a) What is a Distributed Computing System? Explain its advantages and disadvantages.

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

  (ii) Find the turnaround time using these scheduling algorithms. **[BPSC-2026]**

* 12. Calculate the average waiting time.

  | Process | Burst Time |
  | ------- | ---------- |
  | P1      | 21         |
  | P2      | 3          |
  | P3      | 6          |
  | P4      | 2          |
   **[BCIC-2025]**

* 13. What is Deadlock? Write Conditions for Deadlock and also write Deadlock. **[BUET-2025]**

* 14. Write the difference between shell and kernel? **[Petrobangla-2024]**

* 15. How to solve drive failure in RAID? **(2 times)** **[Petrobangla-2024]**

* 16. Explain the fundamental difference between a Process and a Thread. Provide two distinct advantages of using threads over processes. **(2 times)** **[AP-2026]**

* 17. Explain the "Producer-Consumer" problem in operating systems. What specific synchronization issue must be solved? **(2 times)** **[AP-2026]**

* 18. A system utilizes a 32-bit logical address space and a page size of \\(2^{20}\\) bytes. If each entry (block) in the Translation Lookaside Buffer (TLB) requires 6 bytes, calculate the total memory required for the TLB to map the entire logical address space. **[AP-2026]**

* 19. (a) What is Distributed Computing? Differentiate between Distributed Computing and Centralized Computing.

  (b) Explain Clock Cycle and Clock Frequency. What is the clock cycle time of a processor operating at 3.5 GHz?

  (c) Consider the following processes:

  | Process | Burst Time (ms) | Priority |
  | ------- | --------------- | -------- |
  | P₁      | 15              | 3        |
  | P₂      | 2               | 1        |
  | P₃      | 4               | 3        |
  | P₄      | 2               | 4        |
  | P₅      | 8               | 2        |

  All processes arrive at time 0.

  (i) Draw Gantt Charts using FCFS and SJF scheduling algorithms.

  (ii) Determine the average turnaround time. **[BPSC-2026]**

* 20. A system utilizes a 32-bit logical address space and a page size of 2²⁰ bytes. If each entry (block) in the Translation Lookaside Buffer (TLB) requires 6 bytes, calculate the total memory required for the TLB to map the entire logical address space. **[AP-2026]**

* 21. What is Multithreading programming? Why is multithreading used in programming? **[AP-2024]**

* 22. Consider page reference string `1, 3, 0, 3, 5, 6, 3` with 3 page frames. Find the number of page faults. **[Page-replacement algorithm is not specified.]** **[AP-2023]**

* 23. A computer has an Operating System (OS) installed on its SSD, and the SSD is detected in the BIOS. However, the computer boots from the network instead of the SSD. Which BIOS/UEFI setting should be changed to resolve this issue? **[Bangladesh Bank-2026]**

* 24. Consider the following snapshot of a system running the Banker's Algorithm with 5 processes and three resource types: A (10 Instances), B (5 Instances), C (3 Instances).

     | Process | Allocation A | B | C | Max Need A | B | C |
     |---|---:|---:|---:|---:|---:|---:|
     | P0 | 0 | 1 | 0 | 7 | 5 | 3 |
     | P1 | 2 | 0 | 0 | 3 | 2 | 2 |
     | P2 | 3 | 0 | 2 | 9 | 0 | 2 |
     | P3 | 2 | 1 | 1 | 2 | 2 | 2 |
     | P4 | 0 | 0 | 2 | 4 | 3 | 3 |

     - (i) Find and state the content of the Need Matrix.
     - (ii) Demonstrate whether the system is in a safe state or unsafe state. If safe, prove the safe execution sequence. `[BB AD ICT: 07.02.2025]` **[Bangladesh Bank-2025]**

* 25. Differentiate process from a thread regarding memory space allocation. **[RAKUB-2026]**

* 26. A physical server has 32 CPU cores, 96 GB RAM, and 4 TB storage. Each virtual machine (VM) requires 4 CPU cores, 16 GB RAM, and 500 GB storage. Calculate the maximum number of VMs that can be hosted on the server without overcommitting resources. Identify which hardware resource limits the number of VMs. **[O-2026]**

* 27. A system has three processes with the following arrival times and CPU burst times:

      | Process | Arrival Time | Burst Time |
      |---|---:|---:|
      | P1 | 0 | 5 |
      | P2 | 1 | 3 |
      | P3 | 2 | 2 |

      Using the First-Come, First-Served (FCFS) CPU scheduling algorithm, calculate the average waiting time and the average turnaround time. **[O-2026]**

* 28. Differentiate between system software and application software. **[O-2026]**

* 29. Define Virtualization. Explain the role of the Hypervisor and the difference between a Virtual Machine (VM) and a Container. **[O-2026]**

* 30. You have 4 Hard Drives of 2 TB each. Calculate usable storage for RAID 0, RAID 5, and RAID 10. **[O-2026]**

* 31. A startup company wants to launch a new web application. They do not want to manage any underlying hardware, operating systems, or even the runtime environment; they only want to focus on writing and deploying their code. Based on your understanding of Cloud Service Models, which model (IaaS, PaaS, or SaaS) is most appropriate for them? Provide two real-world examples of platforms that provide this specific type of service. **[SO-2026]**

* 32. Explain the basic idea of RAID. Why do servers use multiple hard drives instead of one big drive? If you have six drives of 2 TB each in a RAID 6 setup, calculate the total usable storage space. **[SO-2026]**

* 33. Consider a logical address space of 512 pages, each of 2-KB page size, mapped onto a physical memory containing 128 frames.
     - (a) How many bits are required in the logical address?
     - (b) How many bits are required in the physical address? **[SO-2025]**

* 34. A maintenance engineer is setting up a RAID 5 array with five hard drives, each having a capacity of 4 TB. What is the total usable storage capacity, and why is it not 20 TB? **[AE-2026]**

* 35. Briefly explain "Circular Wait." In a Resource Allocation Graph, if a cycle exists, does it absolutely guarantee that a Deadlock has occurred? Explain briefly. **[AE-2026]**

* 36. Consider a logical address space of 512 pages, each of 2-KB Page size, mapped onto a physical memory containing 128 frames:

  * **a)** How many bits are required in the logical address?


  * **b)** How many bits are required in the physical address? **[SO-2025]**

* 37. A system uses a 16-bit logical address and a 1 KB page size. Find the number of pages and the bits used for page number and offset. **[Dhaka WASA-2025]**

* 38. An application works correctly for one user account but fails for another on the same machine. What could be the possible causes and troubleshooting steps? **[Ministry of Land-2025]**

* 39. Give the necessary conditions for deadlock to occur. Is it possible to have deadlock involving only a single process? Explain your answer. **[O-2024]**

* 40. Write the difference between shell and karnels? **[Petrobangla-2024]**

* 41. Assume that an office has three departments and each department has 50 to 70 employees who are using computers with Windows operating systems. The office space is designed in such a way that an employee can use any computer within a department. Once an employee logs in from a computer, he/she will get access to his files from the server. Let you are planning for network and server setup for this company.
  * a. What is Active Directory? Do you need an Active Directory for such an office? If yes, briefly explain its use under this circumstance.


  * b. What is a subnet? What benefits will you get using subnets for this office? **[SO-2024]**

* 42. When do we use multi thread programming? Describe one problem that you have solved by multi-thread programming. Also write necessary code to solve the problem. **[AP-2024]**

* 43. Scenario: Batch Processing and Multithreading related problem analysis. **[SO-2023]**

* 44. Lists of CPU Scheduling algorithm? Which one is best in performance? Write with explanation. **[ICB Asset Management-2024]**

* 45. Difference between paging and segmentation. **[BTCL-2024]**

* 46. Deadlock এর চারটি শর্ত কি কি? **[BTCL-2024]**

* 47. How can multiprogramming be achieved on a uniprocessor system? Explain. **[BGDCL-2024]**

* 48. Difference between primary and Extended partition of Hard Disk, FAT, FAT32, NTFS. Can FAT 32 drive be converted to NTFS without losing data? **[O-2023]**

* 49. What is Virtualization? Why Virtualization is important. Type discus top 5 popular software / platforms. **[O-2023]**

* 50. Discuss server maintenance best practices, including routine tasks like cleaning, monitoring, and applying security patches. How do these practices contribute to server longevity and performance? **[ANE-2023]**

* 51. What is semaphore? Write a real-life example of it. **[WZPDCL-2023]**

* 52. Define a virtual machine with a neat diagram, explain the working of VM. What are the benefits of Virtual machine? $[BB\text{-}AME\text{-}2023]$ **[BB-AME-2023]**

* 53. LRU replacement algorithm three frames 1234 234 1211 314. Find the Page fault occur? $[\text{Com } AP\text{-}2023]$ **[AP-2023]**

* 54. Job scheduling algorithm $[\text{Teletalk-}2023]$ **[Teletalk-2023]**

* 55. Name and define characteristics properties of the Deadlock situation in a computer system. [Krishi_Biponon_ministry 2022] **[Krishi Biponon Ministry-2022]**

# 11. Linux

* 01. Write Linux command:

  (a) Displays real-time system statistics, including CPU usage, memory usage, running processes, and system load.

  (b) Searches for a specified pattern in a file or output.

  (c) Shows disk usage for all mounted file systems.

  (d) Displays information about system memory (RAM and swap). **[BCIC-2025]**

* 02. Explain the meaning of `chmod 750 backup.sh` and `chown root:admin backup.sh`. Write a command to grant the owner read/write/execute permissions, the group read/execute permissions, and no permissions to others. **[ANE-2026]**

* 03. State the exact administrative activity performed by running the command `chmod 755 script.sh` on a Linux target file. **[RAKUB-2026]**

* 04. Write a Linux command to count the total number of characters and words from the first 10 lines of a file named `wasacustomers.txt`. **[Dhaka WASA-2025]**

* 05. Write Linux command:

      * a) To change permission of a file
      * b) Show the active processes
      * c) To link up process
      * d) To trace the connection
      * e) To download from internet **[BR Powergen-2024]**

* 06. How to show hidden files in a directory (Linux command) [ADBA-2022] **[ADBA-2022]**

* 07. Write down the Linux command for the following instruction: [APSCL-2021]

      * I) Show the files in a folder of the current directory
      * II) Create a directory named 'APSCL' in the current directory.
      * III) You have named "myFile" in the current directory; now, change the permission of the file search where anyone can read, write and execute the file. **[APSCL-2021]**

* 08. Linux Command [NESCO 2021]

      * I. To show only the file names along with size on logged in user directory:
      * II. To show the disk usage report in human-readable format: **[NESCO-2021]**

# 12. Telecommunication & Circuit Part

* 01. Construct a Truth Table for a system that triggers an Alarm (output 1) if: (Motion is Detected AND it is Night Time) OR (Panic Button is Pressed) **(2 times)** **[O-2026]**

* 02. For the Boolean expression:

  ```

  X = AB + (A + B) · C

  ```

  construct and write the complete Truth Table. **[10]** **(2 times)** **[Bangladesh Bank-2025]**

* 03. \\[ \overline{A}\overline{B}\cdot\overline{(A+B)}\cdot C \\]

  Write Truth Table. **[Bangladesh Bank-2025]**

* 04. Design a full adder using XOR and AND or gate? **[BPSC-2025]**

* 05. (a) Consider the following logic circuit.

  (i) Derive the Boolean expression algebraically for T1 through T4. Derive F1 and F2 as a function of the three inputs A, B and C.

  (ii) Use K-map to simplify these expressions F1 and F2, and show that they are equivalent to the ones obtained in (i).

  The original logic circuit is provided on PDF page 18 (printed page 92).

  (b) Represent −25 in 8-bit binary using 2's complement.

  (c) Compare TTL and CMOS logic family in terms of:

  (i) Speed (ii) Noise (iii) Power consumption **[BPSC-2025]**

* 06. (a) A network has been assigned the IP address `200.1.2.0/24`. It has 3 subnets. Determine the following for each subnet:

  (i) Total number of IP addresses (ii) Range of usable IP addresses (iii) Network address (iv) Direct broadcast address (v) Limited broadcast address (vi) Direct broadcast address

  (b) Draw the diagram of TCP/IP protocol suite and mention the name of protocols used in different layers of TCP/IP.

  (c) Compare circuit switching and packet switching. **[BPSC-2025]**

* 07. (a) What is Color Model? Explain RGB, CMY and CMYK color models.

  (b) Prove the following logical equivalence using a Truth Table:

  \\[ p\to q\equiv \neg(p\land\neg q) \\]

  (c) Differentiate between Bandwidth and Throughput. **[BPSC-2026]**

* 08. What is Multiplexer? Difference between D latch and D flip-flop? **[BCIC-2025]**

* 09. Difference between circuit switching and packet switching. Identify which of the two is predominantly used in Internet communication and justify why? **[BUET-2025]**

* 10. Find the Norton equivalent circuit for a DC power supply that has a 30 V terminal voltage.

  The remainder of the question and its circuit are cut off in the supplied scan (PDF page 7). **[Dhaka WASA-2025]**

* 11. What is the use of mmWave in IoT? **(2 times)** **[Petrobangla-2024]**

* 12. A traffic signal cycles from RED to YELLOW, YELLOW to GREEN and GREEN to RED. In each cycle RED is turned for 100 seconds, YELLOW is turned for 40 seconds and GREEN is turned for 80 seconds. The traffic has to be implemented using FSM. The only input to this FSM is a clock of 10 seconds period. The minimum number of flip-flops required to implement this FSM is? **[Petrobangla-2024]**

* 13. Number System Conversion:

  - Binary to Decimal
  - Octal to Hexadecimal **[Biman Bangladesh Airlines-2026]**

* 14. A voice signal is band-limited to 4 kHz. Each sample is quantized using 256 discrete levels. Find the resulting bit rate in a Pulse Code Modulation (PCM) system. **(2 times)** **[AP-2026]**

* 15. Given a propositional logic expression

  \\[ (P\to Q)\leftrightarrow(\neg P\to\neg Q) \\]

  determine whether it is a tautology, contradiction, or contingency. Show the result using a truth table. **[ICB Securities-2026]**

* 16. (a) What is Color Model? Explain RGB, CMY and CMYK Color Models.

  (b) Prove the following logical equivalence using a Truth Table:

  \\[ p\to q \equiv \neg(p\land\neg q) \\]

  (c) Differentiate between Bandwidth and Throughput. **[BPSC-2026]**

* 17. A telephone line normally has a bandwidth of 3000 Hz (300 to 3300 Hz) assigned for data communication. The SNR is usually 3162. What will be the capacity for this channel? **[AP-2023]**

* 18. For the Boolean expression `X =` **[expression missing in the source]**, construct and write the complete Truth Table. **[Bangladesh Bank-2025]**

* 19. A net link utilizes 16QAM. If the underlying signal system operates at baud rate 2400 Baud, calculate exact corresponding data in bps. **[RAKUB-2026]**

* 20. Differentiate between a Fuse and a Miniature Circuit Breaker (MCB). Which one is more suitable for modern office electrical installations and why? **[O-2026]**

* 21. Explain the working principle of a PN junction diode. Draw its symbol and describe the difference between forward bias and reverse bias. **[O-2026]**

* 22. What is the difference between a Multiplexer and a Demultiplexer? Explain one practical application of each in digital systems. **[O-2026]**

* 23. Construct a Truth Table for a system that triggers an Alarm (Output 1) if: (Motion is Detected AND it is Night Time) OR (Panic Button is Pressed). **[O-2026]**

* 24. Five channels, each with a 100-kHz bandwidth, are to be multiplexed together. What is the minimum bandwidth of the link if there is a need for a guard band of 10 kHz between the channels to prevent interference? **[SO-2026]**

* 25. Find the Norton equivalent circuit for a DC power supply delivering specific terminal voltages. **[Dhaka WASA-2025]**

* 26. A two-element series circuit analysis with power factor and applied voltage. **[Dhaka WASA-2025]**

* 27. Calculate channel current for an N-Channel MOS operating in the linear region. **[Dhaka WASA-2025]**

* 28. Design a three-input X-OR gate with the output function $f = w1 \oplus w2 \oplus w3$ using 2-to-1 multiplexers. **[Dhaka WASA-2025]**

* 29. Determine current passing through a resistor in a diode circuit. **[Dhaka WASA-2025]**

* 30. Differentiate between TDM, FDM and WDM in communication. Explain how synchronous TDM work? **[SO-2023]**

* 31. An optical fiber has a single solid dielectric cylinder known as the core, which is surrounded by a solid dielectric... what is called? **[BCC-2023]**

* 32. 55 থেকে 27 বিয়োগ করে দেখাও 2's Complement এর মাধ্যমে। **[BTCL-2024]**

* 33. Sum of min term given $F(A, B, C, D) = \sum(0,2,5,7,8,9,10,13,15)$. Now find simplest form using Karnaugh Map. **[BR Powergen-2024]**

* 34. Difference between Guided and unguided media with example. Cat 5 and cat 6 cable benefit UTP cable compared to STP. **[O-2023]**

* 35. What is the main benefit of a broadband transmission system compared to baseband? What is the attenuation of transmission media? Distinguish between twisted pair, coaxial cable and fiber optics in tabular form. **[ANE-2023]**

* 36. Do you prefer packet switching compared to circuit switching in a communication network? If Yes, why? How does packet switching work step by step? What applications use packet switching? **[ANE-2023]**

* 37. Simplify the following Boolean function using K-map. $[MM\text{-}AP\text{-}2023]$ **[MM-AP-2023]**

* 38. Difference between Optical Communication vs. Satellite Communication $[ANE\text{-}RAKAB\text{-}2023]$ **[ANE-RAKAB-2023]**

* 39. Simplify the Boolean Function: $ABC'D + A'BD + ABCD$ [APSCL-2021] **[APSCL-2021]**

* 40. Design a logic circuit that counts the number of 1s in 3 inputs (A, B, C) and outputs a two-bit binary number representing that count of 1s? [Krishi_Biponon_Ministry 2022] **[Krishi Biponon Ministry-2022]**

* 41. Define the principle of data transmission through the fiber optic cable. [Krishi_Biponon_ministry 2022] **[Krishi Biponon Ministry-2022]**

# 13. Bangla

* 01. **Bangla Focus:** নারী উদ্যোক্তা উন্নয়নে সামাজিক যোগাযোগ মাধ্যমের ভূমিকা। **[ADA-2026]**

* 02. Write an Essay in Bangla:

  দুর্নীতিমুক্ত দেশ গঠনে যুবসমাজের ভূমিকা। **(2 times)** **[O-2026]**

* 03. Translate into Bangla:

  From the Aman paddy season to the current winter vegetable cultivation, farmers in many districts have been unable to purchase fertilizers at government-fixed prices. Farmers and government officials allege that dishonest traders are exploiting an "artificial crisis," particularly for non-urea fertilizers, making extra. Potato farmers in northern districts are among the worst affected. In many districts, farmers reported paying Tk 200-Tk 600 more per 50kg sack than the government rates for non-urea fertilizers. In response, local administration seized around 12,000 sacks of illegally stockpiled fertilizer. **(2 times)** **[O-2026]**

* 04. The Bangla passage for translation is printed at the top of PDF page 2. The text is too small to transcribe reliably from the supplied scan. **[SO-2025]**

* 05. নিচের বিষয়টির ওপর একটি যুক্তিপূর্ণ প্রবন্ধ লিখুন। **[BPSC-2025]**

* 06. সারমর্ম লিখুন। **(2 times)** **[BPSC-2025]**

* 07. একটি ইংরেজি অনুচ্ছেদ বাংলায় অনুবাদ করুন। **[BPSC-2025]**

* 08. ভাবসম্প্রসারণ করুন। **(2 times)** **[BPSC-2025]**

* 09. নিচের বাংলা ব্যাকরণসংক্রান্ত প্রশ্নগুলোর উত্তর লিখুন।

  English (40 Marks) **[BPSC-2025]**

* 10. প্রবন্ধ লিখুন। **[BPSC-2025]**

* 11. একটি অনুচ্ছেদ বাংলায় অনুবাদ করুন। **[BPSC-2025]**

* 12. বাংলা ব্যাকরণসংক্রান্ত প্রশ্নগুলোর উত্তর লিখুন। **[BPSC-2025]**

* 13. শূন্যস্থানে সঠিক শব্দ বসাও। **[BUET-2025]**

* 14. কোনটি কবি জীবনানন্দ দাশের কাব্যগ্রন্থ? **[BUET-2025]**

* 15. উপসর্গ কি? কত প্রকার ও কি কি? **[BCC-2025]**

* 16. ৩৬ জুলাই নিয়ে অনুচ্ছেদ লিখ। **[BCC-2025]**

* 17. বাক্য শুদ্ধি: গর্বিত সূর্য টুটিয়া হয়। **[BCC-2025]**

* 18. আমি কাজটি অবশ্যই করার নিব। **[BCC-2025]**

* 19. Translation English to Bangla. **[BREB-2025]**

* 20. এক কথায় প্রকাশ। **[BREB-2025]**

* 21. বাক্য সংশোধন। **[BREB-2025]**

* 22. **Bangla Focus Writing:** তথ্য প্রযুক্তির যথাযথ ব্যবহার ও সচেতনতা বৃদ্ধিতে করণীয়। **[ANE-2026]**

* 23. **Focus Writing in Bangla:** বাংলাদেশের অর্থনৈতিক খাতে খেলাপি ঋণ: কারণ, প্রভাব ও উত্তরণের উপায়। **[O-2026]**

* 24. **Translate the following passage into Bangla:**

     > The boy found a lost wallet on his way to school. Instead of keeping it, he looked for the owner and returned it. The owner, impressed by his honesty, offered him a reward. The boy politely refused, saying that honesty is its own reward. **[O-2026]**

* 25. **Focus Writing in Bangla:** বাংলাদেশের ব্যাংকিং খাতে চতুর্থ শিল্পবিপ্লবের (4th Industrial Revolution) প্রভাব: ডিজিটাল ব্যাংকিংয়ের সম্ভাবনা, আধুনিক প্রযুক্তির ব্যবহার, গ্রাহকসেবার পরিবর্তন এবং সংশ্লিষ্ট প্রযুক্তিগত চ্যালেঞ্জসমূহ বিশ্লেষণ করুন। **[SO-2026]**

* 26. **Translate the following passage into Bangla:**

     > He decided to pull out of the agreement at the eleventh hour. This sudden move took everyone by surprise and put the entire project at stake. He had informed the team beforehand, we could have easily made alternative arrangements. Now, we are left with no other choice but to start everything from scratch. It just goes to show that you cannot always take people at their word. **[SO-2026]**

* 27. Bangla Section:

  * **ক)** উপসর্গ কাকে বলে? কত প্রকার ও কি কি?


  * **খ)** বাক্য শুদ্ধ করুন: (১) ইহার আবশ্যক নাই (২) অন্নাভাবে ঘরে ঘরে হাহাকার (৩) পূর্বদিকে সূর্য উদয় হয়।


  * **গ)** ৩৬ জুলাই সম্পর্কে অনুচ্ছেদ।


  * **ঘ)** অনুবাদ ও ইংরেজি রূপান্তর (যেমন: আজকের যুগ কৃত্রিম বুদ্ধিমত্তার যুগ...)। **[BCC-2025]**

* 28. Translation [English to Bangla] **[O-2024]**

* 29. Focus Writing in Bangla **[O-2024]**

* 30. [Focus Writing in Bangla] :

  তীব্র তাপপ্রবাহ হ্রাসে পরিবেশ সুরক্ষার গুরুত্ব'-এর উপর একটি রচনা লিখন ১৫০ (+/-১০%) শব্দের মধ্যে। **[SO-2024]**

* 31. [Translate English to Bangla] :

  Earth Day inspires green innovation through participatory and collective action and encourages the adoption of sustainable practices across the financial system. It, therefore, serves as an opportunity for financial institutions to engage with their stakeholders and demonstrates their commitment to sustainable practices. Thus, Earth Day carries a deep significance in promoting sustainable and responsible financing which is an example of environmentally conscious investment practices. Positive environmental outcomes will be easily achieved if all financial sectors, stakeholders and investors alike are part of a long-term plan to improve the environmental health of this planet, along with the financial and human health. We celebrate Earth Day around the world, let us reaffirm our commitment towards building a greener, more tolerant, liveable and sustainable future for our next generations. *(Translation: English to Bangla)*

  #### General Knowledge **[SO-2024]**

* 32. সমৃদ্ধির অগ্রযাত্রায় বাংলাদেশ" এর উপর বাংলায় একটি রচনা লিখুন ২০০ (+/- ১০%) শব্দের মধ্যে। **[ANE-2023]**

* 33. * i) Correct the sentence: We had gone to the movies yesterday.


      * ii) Make a sentence using 'keep on'


      * iii) Change the narration: He said, "I shall play football".


      * iv) সঠিক রূপ লিখঃ সব ছাত্র আজ উপস্থিত।


      * v) Translate the following sentence: পথিকের পথ চলা আর শেষ হলো না। **[WZPDCL-2023]**

# 14. English

* 01. **English Focus:** Earthquake Risk management and mitigation. **[ADA-2026]**

* 02. Write an Essay in English:

  Online Banking **(2 times)** **[O-2026]**

* 03. Translate into English:

  বর্তমান ডিজিটাল যুগে গুগল ড্রাইভ এখন শুধু একটি ফাইল সংরক্ষণের জায়গা নয়, বরং এটি পড়াশোনা, অফিসের কাজ ও ব্যক্তিগত নথি ব্যবস্থাপনার একটি গুরুত্বপূর্ণ ডিজিটাল মাধ্যম। প্রতিদিনেই কোটি কোটি মানুষ এ ক্লাউড স্টোরেজ সেবার ওপর নির্ভর করছে। তবে নিয়মিত ব্যবহার করলেও অনেকেই জানেন না, গুগল ড্রাইভে এমন কিছু লুকানো ফিচার রয়েছে, যা ব্যবহারকারীর কাজকে আরো সহজ, দ্রুততর ও কার্যকর করে। ই-মেইলে বড় ফাইল পাঠানোর ক্ষেত্রে এটাচমেন্ট সাইজ একটি বড় সমস্যা। তবে জিমেইল ব্যবহারকারীরা গুগল ড্রাইভ থেকে সরাসরি ফাইল যুক্ত করে সহজেই বড় ফাইল পাঠাতে পারেন. **(2 times)** **[O-2026]**

* 04. Language Proficiency and Analytical Technical Writing:

  (a). Translate the following sentences from Bengali to English:

  1. নিরাপত্তা হতে জল অপচয় করা যায় না।  
  2. আপনার ব্যাংক অ্যাকাউন্টের স্থিতি জানার জন্য মোবাইল ব্যাংকিং অ্যাপ্লিকেশন এ লগইন করুন।

  ### (b) Focus Writing (Short Note)

  Write a comprehensive short note on:

  **"The role of Artificial Intelligence (AI) and Machine Learning in mitigating the challenges of cyber attacks on the banking system."**

  **Target word count: 100 to 150 words.** **(2 times)** **[Bangladesh Bank-2025]**

* 05. Essay: "Growing use of technology in the Financial Service Industry." **[Bangladesh Bank-2023]**

* 06. Bengali to English:

  (a) শনিবার হতে সে অফিসে আসছে না।

  (b) আপনার ব্যাংক একাউন্ট এর স্থিতি জানার জন্য মোবাইল ব্যাংকিং এপ্লিকেশন এ লগইন করুন।

  (c) Write short note on: "The role of AI and machine language mitigate challenges of cyber attack on banking system" 100 to 150 Words. **[Bangladesh Bank-2025]**

* 07. The ongoing war in Gaza has created a serious humanitarian crisis. Continuous bombing and fighting have destroyed thousands of houses, hospitals, and schools. Many innocent people have lost their homes and are living without enough food, clean water, or medicine. Children and women are suffering the most because they have no protection and very little help. Aid workers say that the situation in Gaza is getting worse every day and people may soon face starvation and disease. The Gaza war has become a tragedy that affects the whole world. It shows how war destroys not only buildings but also hope and humanity. **[SO-2025]**

* 08. Write an essay on "The Internet" using the hints given below: What internet is, Greatest means of communication, Various uses, Storehouse of information, Impact of information technology, Global financial impact, Internet addiction, Harmful effects, Uses and abuses, Conclusion. **[BPSC-2025]**

* 09. Write a letter to the officer-in-charge of your police station to provide regular police patrol in your locality to prevent crimes. **[BPSC-2025]**

* 10. Read the passage on climate change and answer questions (a)–(e). **[BPSC-2025]**

* 11. Rewrite the sentences using the instructions given in brackets (sentence correction, voice, narration, prepositions and idioms). **[BPSC-2025]**

* 12. Read the passage about discipline and answer the questions (a)–(e). **[BPSC-2025]**

* 13. Write an essay on "Corruption in the ICT Sector in Bangladesh" using the hints given. **[BPSC-2025]**

* 14. Imagine that you have purchased a laptop from a local showroom a week back. The warranty period is on and the laptop is not functioning well. Write a letter of complaint to the manager of the showroom about the problem and what you want. **[BPSC-2025]**

* 15. Rewrite the sentences using the instructions given in brackets. **[BPSC-2025]**

* 16. Write an essay on "Digital Citizenship on Social Media" using the following hints: Introduction, Concept of Digital Citizenship, Benefits of social media, Challenges and risks, Online ethics and responsible behavior, Combating fake news and misinformation, Role of digital literacy and awareness, Conclusion. **[BPSC-2026]**

* 17. Write a letter to the editor of a newspaper drawing public attention against the "Wide spread of corruption" in every sphere of life. **[BPSC-2026]**

* 18. Read the passage on nuclear war and answer questions (a)–(e). **[BPSC-2026]**

* 19. Answer the following questions on grammar and sentence correction. **[BPSC-2026]**

* 20. Convert into a question:

  "You have some way?" **[BUET-2025]**

* 21. Correct the sentence:

  "Do you have any inflammable materials with you?" **[BUET-2025]**

* 22. Our success was better than expected. **[BUET-2025]**

* 23. She has a strong \_\_\_\_\_\_ in justice and equality.

  (a) belief (b) believe (c) beliefs (d) believing **[BUET-2025]**

* 24. A sentence is "stringent". What is the meaning of "stringent"?

  (a) relaxed (b) inflexible (c) lenient (d) expensive **[BUET-2025]**

* 25. More than a boy \_\_\_\_\_\_ were has found guilty.

  (a) were (b) has (c) was (d) have **[BUET-2025]**

* 26. The committee \_\_\_\_\_\_ divided in their opinion.

  (a) was (b) has (c) is (d) were **[BUET-2025]**

* 27. Correct the spelling — neumonia. **[BCC-2025]**

* 28. Do not close the door — make it passive. **[BCC-2025]**

* 29. Preposition. **[BCC-2025]**

* 30. Type of sentence: Though he is poor, he is honest. **[BCC-2025]**

* 31. Translate Bangla to English: 3 sentence. **[BCC-2025]**

* 32. Everybody hates a liar. (Make negative) **[BCC-2025]**

* 33. Man is mortal. (Make negative but no meaning change) **[BCC-2025]**

* 34. Paragraph on: Three Zero Theory. **[BREB-2025]**

* 35. From the parentheses in each sentence, write only the correct answer.

  (A) If the department had allocated more funds, the project (would succeed / would have succeeded).

  (B) By next month, the university (will have completed / will ... ) ...

  The remaining options and subsequent parts of Question 20 are cut off in the scan. **[AP-2026]**

* 36. Discuss the effects of transitioning to a renewable energy-based economy on the economy and the environment. Also discuss the challenges of this transition. **[ICB Securities-2026]**

* 37. Discuss the opportunities, employment prospects, and side effects of social media. **[ICB Securities-2026]**

* 38. (a) Translate the passage on 21st February from Bengali to English.

  (b) Suppose ICB's server traffic increases from 10,000 to 50,000 hits, but ICB does not migrate to the cloud. Discuss the possible consequences from both the business and technical perspectives. **[ICB Securities-2026]**

* 39. Write an essay on "Digital Citizenship on Social Media" using the following hints:

  Introduction – Concept of Digital citizenship – Benefits of social media – Challenges and risks – Online ethics and responsible behavior – Combating fake news and misinformation – Role of digital literacy and awareness – Conclusion. **[BPSC-2026]**

* 40. Write a letter to the editor of a Newspaper drawing public attention against the "Wide spread of corruption" in every sphere of life. **[BPSC-2026]**

* 41. Read the passage about nuclear war and answer the questions that follow:

  (a) What is the result of a nuclear war?

  (b) How will the survivors of nuclear war survive?

  (c) What is the best way to avoid nuclear war?

  (d) What would be the appropriate title of the above passage? Justify the title in two sentences.

  (e) What is the consequence of radiation? **[BPSC-2026]**

* 42. Answer the following questions.

  (a) Rangu Mia saw Alta Begum and Bedena Begum (discuss) \_\_\_\_\_\_ a funny thing. (Use the right form of each other. Use the right form of verb in bracket.)

  (b) It was long gap since they (meet) \_\_\_\_\_\_ each other.

  (c) He uttered something in his speech and it was disappointing. (Make it complex.)

  (d) Why do you prefer bus journey to train journey? (Use positive degree.)

  (e) He is going to cuts his hair. (Correct the sentence.)

  (f) There is a girl's high school at my Village. (Correct the sentence.)

  (g) Make a meaningful sentence with "Give vent to".

  (h) Make a meaningful sentence with "By leaps and bounds".

  (i) I am sorry \_\_\_\_\_\_ disturbing you. (Use a preposition.)

  (j) The baby is crying. (Make it passive.) **[BPSC-2026]**

* 43. **English Proficiency Related Questions.** From the parentheses in each sentence, write only the correct answer:
      - A. If the department had allocated more funds, the project (would succeed / would have succeeded).
      - B. By next month, the university (will have completed / will complete) the accreditation process.
      - C. Hardly (did the presentation begin / had the presentation begun) when the technical problems occurred.
      - D. The committee, as well as its sub-groups, (meets / meet) regularly to discuss policy matters.
      - E. He had better (leave / left) the station before it's too late.
      - F. The methodology section is comprehensive; (for example / however), the discussion lacks critical depth.
      - G. The research team arrived at (a / an) unanimous conclusion after extensive discussion.
      - H. The students were warned that any breach of conduct could result (in / to) suspension.
      - I. She is one of the scholars who (advocates / advocate) a critical pedagogy approach.
      - J. The researcher insisted that the data (be / is) analyzed before publication. **[AP-2026]**

* 44. Write a paragraph on: **Street food culture in Dhaka**. **[AP-2026]**

* 45. Make meaningful sentences with the following words. Do not change the grammatical category of the word: **Judicious; Condone; Fabricate; Accentuate; Multifaceted.** **[AP-2026]**

* 46. Write a short composition: **"The Role of Computers in the Education System in Bangladesh"**. **[AP-2024]**

* 47. Write a letter to your younger brother about the importance of professional vocational training. **[AP-2024]**

* 48. Essay: **"Growing use of technology in the Financial Service Industry."** **[Bangladesh Bank-2023]**

* 49. Discuss five advantages and five challenges of mobile banking. **[Bangladesh Bank-2026]**

* 50. **Language Proficiency and Analytical Technical Writing:**
      - (a) Translate the following sentences from Bengali to English:
         - (i) শনিবার হতে সে অফিসে আসছে না।
         - (ii) আপনার ব্যাংক অ্যাকাউন্ট এর স্থিতি জানার জন্য মোবাইল ব্যাংকিং অ্যাপ্লিকেশন এ লগইন করুন।
      - (b) Focus Writing (Short Note): Write a comprehensive short note on: **"The role of Artificial Intelligence (AI) and Machine Learning in mitigating the challenges of cyber attacks on the banking system."** **[Bangladesh Bank-2025]**

* 51. **English Focus Writing:** Data security challenges in banks and protection guidelines. **[ANE-2026]**

* 52. Explain how a Man-in-the-Middle (MitM) attack can compromise a customer's online banking session and describe technologies to mitigate the threat. **[ANE-2026]**

* 53. **Focus Writing in English:** The Role of Sustainable Banking in Achieving the UN Sustainable Development Goals (SDGs) in Bangladesh. **[O-2026]**

* 54. **Translate the following passage into English:**

     > এক ক্ষুধার্ত শিয়াল একটি আঙুর ক্ষেতের পাশ দিয়ে যাচ্ছিল। উঁচুতে ঝুলে থাকা আঙুর দেখে সে তা খাওয়ার চেষ্টা করল, কিন্তু বারবার লাফিয়েও ব্যর্থ হলো। অবশেষে সে হতাশ হয়ে চলে গেল। যাওয়ার সময় বলল, আঙুরগুলো আসলে টক। **[O-2026]**

* 55. **Focus Writing in English:** The Importance of Digital Literacy in Expanding Cashless Transactions in Bangladesh: Discuss how digital skills influence financial inclusion, the adoption of digital payment systems, and the challenges of building a cashless economy. **[SO-2026]**

* 56. **Translate the following passage into English:**

     > “কথায় আছে, সময়ের এক ফোঁড় অসময়ের দশ ফোঁড়। অথচ আমরা আজ করব কাল করব বলে কাজ ফেলে রেখে ভাগ্যের দোহাই দিতে পছন্দ করি। আকাশকুসুম কল্পনা করে জীবনে রাতারাতি সফল হওয়া যায় না। যে জাতি যত বেশি পরিশ্রমী, সে জাতি তত বেশি উন্নত। তাই কথায় কথায় অজুহাত না দেখিয়ে আমাদের এখনই কাজে নেমে পড়া উচিত।” **[SO-2026]**

* 57. English Section:

  * Verb form of 'milk', correct spelling of 'nuemonia', antonym of 'artificial', passive form of "Do not close the door", transformations of sentences (negative/types), etc. **[BCC-2025]**

* 58. Translation [Bangla to English] **[O-2024]**

* 59. Focus Writing in English **[O-2024]**

* 60. [Focus Writing in English] :

  Write an essay on Modern Technology and Its Effect on Student Academic Achievements within 150 (+/-10%) words. **[SO-2024]**

* 61. [Translate Bangla to English] :

  বাংলাদেশে ব্যবসা প্রতিষ্ঠান বাসাবাড়ি ও বিভিন্ন প্রকল্পে সৌরবিদ্যুৎ তথা সোলার প্যানেলের ব্যবহার দিন দিন বাড়ছে। সূর্য থেকে সোলার প্যানেল আলো শোষণ করে বৈদ্যুতিক প্রবাহ তৈরি করে, যা দিয়ে পরবর্তী সময়ে লাইট, ফ্যান প্রভৃতি চালানো যায়। সরকারের টেকসই উন্নয়ন লক্ষ্যমাত্রায় ২০৩০ সালের মধ্যে ৪ হাজার ১০০ মেগাওয়াট বিদ্যুৎ নবায়নযোগ্য উৎস থেকে উৎপাদনের পরিকল্পনা নেয়া হয়েছে। ফলে নীতিগত ও ব্যবহারিক উভয় দিক দিয়ে দেশে সৌরবিদ্যুৎ খাতের বেশ সম্ভাবনা রয়েছে। সোলার প্যানেলের মাধ্যমে বিদ্যুৎ উৎপাদন মূলত একটি পরিবেশবান্ধব প্রক্রিয়া এবং এ প্রক্রিয়ায় বিদ্যুৎ উৎপাদন করে তা জাতীয় গ্রিডে যুক্ত করা গেলে বিদ্যুৎ খরচ ২০ শতাংশ কমবে। *(Translation: Bangla to English)* **[SO-2024]**

* 62. The role of computer in education system of Bangladesh. **[AP-2024]**

* 63. Write a letter to your younger brother by mentioning the importance of vocational training for employment generation in Bangladesh. **[AP-2024]**

* 64. Write an essay on Women's Empowerment and Gender Equality in Bangladesh within 200 (+/-10%) words. **[ANE-2023]**

# 15. General Math

* 01. Solve the following mathematical and analytical problems:

  (a) Evaluate the definite integral:

  \[
  \int_0^2 (2x^2 + 3x)\,dx
  \]

  (b) In Bangladesh Bank, there are 6 Assistant Directors (ADs) and 4 Deputy Directors (DDs). Each AD always brings a bag to the workplace, whereas only half of the DDs bring a bag. If a bag is selected completely at random from all the bags brought to the office, what is the probability that the chosen bag belongs to a Deputy Director (DD)? **(2 times)** **[Bangladesh Bank-2025]**

* 02. Given two integers A and B as input, write a program to compute the least common multiple (LCM) of A and B. **(2 times)** **[Bangladesh Bank-2023]**

* 03. If x is an integer and x + 1/x = 17/4 , then the value of x - 1/x = ? **[Bangladesh Bank-2023]**

* 04. A basketball team has won 15 games and lost 9. If these games represent 16 2/3% of the games to be played, then how many more games must the team win to average 75% for the season? **[Bangladesh Bank-2023]**

* 05. Students of a class are made to stand in rows. If 4 students are extra in each row, then there would be 2 rows less. If 4 students are less in each row, then there would be 4 more rows. What is the number of students in the class? **(2 times)** **[Bangladesh Bank-2023]**

* 06. (a)

  \\[ \int_0^2 (2x^2+3x)\\,dx \\]

  (b) In Bangladesh Bank, there are 6 Assistant Directors (ADs) and 4 Deputy Directors (DDs). Each AD brings a bag, while only half of the DDs bring a bag. If a bag is selected at random from all the bags, what is the probability that the chosen bag belongs to a Deputy Director (DD)? **[Bangladesh Bank-2025]**

* 07. CARBON word permutations that vowel must occupy odd positions? **[BCIC-2025]**

* 08. −3, −6, −9, −12 ... এর ১২তম পদের যোগফল কত? **[BUET-2025]**

* 09. মৌলিক সংখ্যা দ্বারা গঠিত সেট কোনটি?

  (a) 13 (b) 13 (c) 8 (d) 12 **[BUET-2025]**

* 10. 4x + 3y = 22 রেখার মূলবিন্দু (0, 0) থেকে দূরত্ব কত?

  (a) 5 (b) 4.4 (c) 3.6 (d) 6 **[BUET-2025]**

* 11. qx + py + r = 0 রেখার ঢাল কত? **[BUET-2025]**

* 12. x² + y² + 6x − 8y + 1 = 0 বৃত্তটির সমীকরণ-সংক্রান্ত প্রশ্ন। **[BUET-2025]**

* 13. একটি নির্দিষ্ট শর্তে ক্রয়মূল্য ও বিক্রয়মূল্য-সংক্রান্ত শতকরা হিসাব নির্ণয় কর। **[BUET-2025]**

* 14. ১০% চক্রবৃদ্ধি সুদে কোন আসলের সুদ ২৬৮ টাকা হয়? **[BUET-2025]**

* 15. ১২০ MCQ মধ্যে ৬৫ পেলে, ভুল আর সঠিক কয়টি? সঠিক উত্তরে ১ মার্ক এবং ভুল উত্তরে ০.২৫ মার্ক কাটা যায়। **[BCC-2025]**

* 16. ৮.৬% করে সুদে ঋণ নিয়েছে। ঋণ এবং সুদের সমন্বয় ৮.৬% হারে কত বছর?

  Some Bengali questions on PDF pages 9–10 are partially legible; those lines may require checking against the original scan. **[BCC-2025]**

* 17. A rectangle and a square have the same area. The square has a perimeter of 32 meter and the width of the rectangle is 4 meter. Find the length of the rectangle (in meter). **[AP-2026]**

* 18. If \\(2 < x < 5\\) and \\(3 < y < 5\\), find the value of \\(x-y\\) in terms of inequality? **[AP-2026]**

* 19. In a class, the number of boys is 35% more than that of the girls. The total number of students of the class is 94. If 6 more boys are admitted to the class, calculate the ratio of the number of boys to that of the girls. **[AP-2026]**

* 20. A man can row 12 kmph in still water. It takes him thrice as long to row up as to row down the river. Find the rate of the stream. **(2 times)** **[AP-2026]**

* 21. Server X handles 60% of the traffic and has a 2% failure rate. Server Y handles 40% of the traffic and has a 5% failure rate.

  (a) Find the probability of total failure.

  (b) Find the probability that a failed request belongs to Server Y. **[ICB Securities-2026]**

* 22. A rectangle and a square have the same area. The square has a perimeter of 32 meters. The width of the rectangle is 4 meters. Find the length of the rectangle (in meters). **[AP-2026]**

* 23. If 2 < x < 5 and 3 < y < 5, find the value of x − y in terms of inequality? **[AP-2026]**

* 24. In a class, the number of boys is 35% more than that of the girls. The total number of students in the class is 94. If 6 more boys are admitted to the class, calculate the ratio of the number of boys to that of the girls. **[AP-2026]**

* 25. Write a program for Floyd's triangle, n = 5:

     ```text
     1
     0 1
     1 0 1
     0 1 0 1
     1 0 1 0 1
     ```
   **[AP-2024]**

* 26. A basketball team has won 15 games and lost 9. If these games represent 16⅔% of the games to be played, then how many more games must the team win to average 75% for the season? **[Bangladesh Bank-2023]**

* 27. An email mailbox has a storage quota of 2 GB. The following storage is occupied:
     - Sent Items: 350 MB
     - Inbox: 1.25 GB
     - Trash: 900 KB
     - Drafts: 120 MB

     Given that 1 GB = 1,000 MB and 1 MB = 1,000 KB:
     - (a) How much mailbox storage is remaining?
     - (b) What should the email recipient do to receive a 300 MB file? **[Bangladesh Bank-2026]**

* 28. Solve the following mathematical and analytical problems:
     - (a) Evaluate the definite integral: `∫₀² (2x² + 3x) dx`.
     - (b) In Bangladesh Bank, there are 6 Assistant Directors (ADs) and 4 Deputy Directors (DDs). Each AD always brings a bag to the workplace, whereas only half of the DDs bring a bag. If a bag is selected completely at random from all the bags brought to the office, what is the probability that the chosen bag belongs to a Deputy Director (DD)? **[Bangladesh Bank-2025]**

* 29. Math Section:

  * Percentage investment problems, profit/loss calculations with negative marking parameters, and algebraic expression simplification involving square roots ($x$ and $y$). **[BCC-2025]**

* 30. Find the sets X and Y if $X\cup Y=\{1,2,3,5,6,8,9,10\}$, $X\cap Y=\{1,5\}$ and $Y-X=\{2,6,9,10\}$ **[O-2024]**

* 31. If you throw two unbiased dice (each with six sides) together, what is the probability that the sum of the two upward faces will be 7? **[O-2024]**

* 32. Write a c/c++/java program of Floyd's Triangle **[AP-2024]**

* 33. Simple interest on a certain sum of money at the rate 5% p.a for 8 years is tk 840. At what rate interest the same amount of inclusions can be received on the same sum after 5 years. **[AP-2024]**

* 34. In an office 72% of workers prefer tea, 44% prefer coffee, 40 prefer tea or coffee and 40 like both, what is the total number of workers in the office. **[AP-2024]**

* 35. Cost of a diamond varies directly as the square of its weight. A diamond is broken into four pieces with their weights in the ratio of 1:2:3:4. If the loss in the total value of the diamond was tk 70000, find the price of the original diamond. **[AP-2024]**

* 36. If the CE bisects $\angle ACB$, then find the value of $x = ?$ **[AP-2024]**

# 16. General Knowledge (GK)

* 01. General Knowledge (Write only the correct answer. Do not write the whole sentence):

  * **i.** Where was the first earthquake observation centre established in Bangladesh?


  * **ii.** What is the full form of "WIPO"?


  * **iii.** In which year 'Value Added Tax' was introduced in Bangladesh?


  * **iv.** What is the name of the first bank owned by Bengali Entrepreneurs?


  * **v.** Where is the CIRBDAP situated?


  * **vi.** Who invented dynamite?


  * **vii.** Which country's national won the Men's singles in ITTF world championship 2025?


  * **viii.** How many layers are available in OSI network model?


  * **ix.** What is the meaning of "Terracotta"?


  * **x.** Which international organization offered GSP+? **(2 times)** **[O-2026]**

* 02. সংক্ষিপ্ত সাধারণ জ্ঞানমূলক প্রশ্নগুলোর উত্তর লিখুন।

  English (40 Marks) **[BPSC-2025]**

* 03. উত্তরা গণভবন কোথায় অবস্থিত?

  (a) গাজীপুর (b) রাজশাহী (c) রংপুর (d) চট্টগ্রাম **[BUET-2025]**

* 04. চ্যাটজিপিটি কোন কোম্পানি তৈরি করেছে?

  (a) Microsoft (b) OpenAI (c) Google (d) Meta **[BUET-2025]**

* 05. Write the full meaning:

  (a) HTTP

  (b) DVD

  (c) SMTP **[BREB-2025]**

* 06. Full meaning:

  (a) ASEAN

  (b) SPARRSO

  (c) BERC **[BREB-2025]**

* 07. গ্রামীণ ব্যাংক সম্পর্কিত প্রশ্ন। **[BREB-2025]**

* 08. **General Knowledge:**
     - (A) How many basic pillars does the Constitution of Bangladesh have?
     - (B) Which agreement led to an end of the First World War?
     - (C) Roscosmos is the aerospace agency of which country?
     - (D) The Durand Line is the border between which two countries?
     - (E) COP30 was held in which continent?
     - (F) Which is the first paperless city in the world?
     - (G) What is the name of China's commercial aircraft manufacturer?
     - (H) Where is the Shat Gombuj Mosque located?
     - (I) How many foreign banks currently operate in Bangladesh?
     - (J) In relation to product export, what does DDP stand for? **[ANE-2026]**

* 09. **General Knowledge (10 Marks):**
     - Which river is known as the "Lifeline of Bangladesh"?
     - What is the name of the international organization that monitors global health standards and coordinates the response to pandemics?
     - What is the name of Bangladesh's first deep-sea port?
     - Where is the headquarters of the International Monetary Fund (IMF) located?
     - Which country has the world's longest coastline? **[O-2026]**

* 10. **General Knowledge (10 Marks):**
     - What is the full form of NPSB in the banking sector of Bangladesh?
     - Who is the architect of the National Martyrs' Memorial in Savar?
     - What is the name of the central bank of the United Kingdom?
     - Which international organization publishes the "World Economic Outlook" report?
     - What is the name of the first submarine communications cable system that Bangladesh is connected to? **[SO-2026]**

* 11. General Knowledge:

  * Questions regarding Bangladesh Computer Council, UN headquarters, 5th Five-Year Plan, SDG goals, longest river, BIMSTEC, Web3, and ICT Ministry establishment. **[BCC-2025]**

* 12. Answer the following questions (i-x):


  * i. Which organization was created as a result of the language movement?


  * ii. UNDP works in different countries and territories to eradicate poverty while protecting the planet. The headquarters of UNDP is located in which country?


  * iii. On 17 November 2015, UNESCO declared International Day for Universal Access to Information. Which day is observed as International Information Day?


  * iv. In which year did the first coal-fired Ultra Super Critical Thermal Power Plant start the commercial power supply to the national grid of Bangladesh?


  * v. What is the name of the first Bangladeshi film at the Oscars?


  * vi. Which campaign works toward building an international consensus and a sustained global movement of leaders and citizens to eliminate nuclear weapons?


  * vii. American poet and activist Allen Ginsberg wrote a poem, inspired by the plight of the East Bengali refugees from the 1971 Bangladesh Liberation War. What is the name of the poem?


  * viii. How many priority sector(s) fall under the Blue Economy for Bangladesh?


  * ix. What is the hardest substance available on earth?


  * x. As per the declaration of the government, Bangladesh will turn into 'Smart Bangladesh' by which year? **[O-2024]**

* 13. What is Padma Shri Award? Mention the name of Renowned Bangladeshi singer who has recently got the Padma Shri Award. **[SO-2024]**

* 14. What is BIMSTEC? **[SO-2024]**

* 15. Who will host the T20 World Cup 2024? **[SO-2024]**

* 16. Mention the name of the First Governor of Bangladesh Bank.

  #### Subjective Question: **[SO-2024]**

* 17. The first ODI Cricket was played on January 5, 1971 between which countries? **[ANE-2023]**

* 18. Write down the longest and shortest day on the planet. **[ANE-2023]**

* 19. Mention the name of the largest, biggest and heaviest planet. **[ANE-2023]**

* 20. Who wrote the books titled Ekattorer Diary and Ekatturer Dinguli? **[ANE-2023]**

* 21. Who was awarded the Meril-Prothom Alo Lifetime Award 2022? **[ANE-2023]**

* 22. Non-departmental Questions:


      * i) What is the actual length of the padma bridge?


      * ii) Where and when was WZPDCL constituted?


      * iii) Which vitamin helps the blood clot?


      * iv) Why March month is so valuable for our nation?


      * v) In liberation war Khulna's sector was? **[WZPDCL-2023]**

# 17. Others

* 01. Excel এর Vlookup ফর্মুলা ব্যাখ্যা কর। **[BTCL-2024]**

---

# Processing Summary

- **Total Source Files Expected:** 9
- **Successfully Processed Files:** 9
- **Missing / Unreadable Files:** None (0)
- **Total Question Occurrences Extracted Before Deduplication:** 912
- **Total Unique Question Entries After Deduplication:** 824
- **Duplicate Occurrences Consolidated:** 88
- **Number of Questions Appearing More Than Once:** 83
- **Number of Questions with Missing Institute/Year Metadata:** 3
- **Unresolved Classification or Duplicate-Detection Issues:** None

### Question Counts by Master Subject:

| No. | Master Subject Heading | Unique Questions Count |
| :--- | :--- | :--- |
| 01 | 1. C Programming | 57 |
| 02 | 2. Data Structure & Algorithm | 88 |
| 03 | 3. Data Communication & Networking | 103 |
| 04 | 4. Security & Cryptography | 75 |
| 05 | 5. Database | 93 |
| 06 | 6. Computer Architecture & Microprocessor | 53 |
| 07 | 7. OOP | 45 |
| 08 | 8. Software Engineering | 37 |
| 09 | 9. Web Technologies | 13 |
| 10 | 10. Operating System | 55 |
| 11 | 11. Linux | 8 |
| 12 | 12. Telecommunication & Circuit Part | 41 |
| 13 | 13. Bangla | 33 |
| 14 | 14. English | 64 |
| 15 | 15. General Math | 36 |
| 16 | 16. General Knowledge (GK) | 22 |
| 17 | 17. Others | 1 |
| -- | **Total Unique Questions** | **824** |
