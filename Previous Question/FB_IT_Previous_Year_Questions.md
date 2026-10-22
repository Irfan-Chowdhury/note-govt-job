# IT Previous Year Questions — Extracted from PDF

**Source:** `IT Previous Year Question.pdf` (28 PDF pages; the source itself labels them Pages 3–30).  
**Scope:** Questions only, grouped by examination, preserving the printed question numbering. Technical subquestions, formulas, data, and code snippets are retained wherever legible. Exam-preparation topic checklists and duplicated copies of the same paper are excluded.  
**Note:** The source is image-only, and a few tiny or blurred symbols/passage words should be checked against the original pages. Any visibly absent information is marked rather than invented.

---

## 1. Combined Bank — Assistant Programmer
**Exam date:** 22.05.2026 · **Exam taker:** E-Zone · **23-year based** · **Source:** PDF page 1 (printed page 3)

1. Compare BFS & DFS with examples.
2. Explain the time complexity of merge sort. Best, Average, Worst.
3. Suppose your dataset has missing values and noise. How would you preprocess it?
4. A voice signal is band-limited to 4 kHz. Each sample is quantized using 256 discrete levels. Find the resulting bit rate in a Pulse Code Modulation (PCM) system.
5. Two separate threads are initialized with the exact same instance of Counter Subsystem and run concurrently to completion. State definitively whether the final value of `transactionCounter` is guaranteed to be exactly 2000. Name the specific multithreading hazard that occurs here and explain the low-level mechanical steps that cause this behavior.
6. In a B+ tree, each node can have a maximum of 4 child pointers (order m = 4). From height 0 to height 2 (where height 0 is the root), what is the maximum number of keys that can be stored across all nodes in the tree?
7. What is the output of the following C program? (Pointer arithmetic with ledger array.) **[The referenced C program is not present on the source page.]**
8. A system utilizes a 32-bit logical address space and a page size of 2²⁰ bytes. If each entry (block) in the Translation Lookaside Buffer (TLB) requires 6 bytes, calculate the total memory required for the TLB to map the entire logical address space.
9. Consider a concurrent transaction schedule involving two data items, X and Y:
   - **T1:** Read(X), Write(X), Read(Y), Write(Y)
   - **T2:** Read(Y), Write(Y), Read(X), Write(X)

   Describe how the standard 2PL protocol treats these transactions. Contrast with Strict 2PL.
10. Compare between TCP and UDP: their connection, reliability, speed. One real-life use case of UDP.
11. Assume a banking application wants to add a fingerprint system for their App. Write one functional requirement and one security requirement.

---

## 2. Combined Bank — Assistant Programmer
**Exam date:** 17.01.2026 · **Exam taker:** DU · **22-year based** · **Source:** PDF pages 2–4 (printed pages 4–6)

1. Explain the concept of Inheritance in Object-Oriented Programming. Name and briefly describe three common types of inheritance used in OOP.
2. Explain the concept of the Software Development Life Cycle (SDLC) and describe its main phases.
3. Apply the concept of IP addressing and routing to explain how packets are delivered across networks using Open Shortest Path First (OSPF) at the network layer.
4. What is a Universal Gate? Prove that the NAND Gate is a Universal Gate.
5. Explain the fundamental difference between a Process and a Thread. Provide two distinct advantages of using threads over processes.
6. What is Version Control (e.g., Git)? Explain the specific difference between "Committing" code and "Pushing" code.
7. Describe step-by-step how Binary Search locates a target value in a sorted array. Why does it fail if the array is unsorted?
8. You have two stacks. Explain the logic required to implement a Queue (FIFO) using only these two stacks.
9. Explain the logic of "Bubble Sort". Why is it considered inefficient for large datasets compared to Merge Sort?
10. Explain the "Producer-Consumer" problem in operating systems. What specific synchronization issue must be solved?
11. Draw or describe a Flowchart to determine the largest of three distinct numbers (A, B, C).
12. Construct a logical argument explaining why a heuristic (like A* search) can be faster than a blind search (like BFS), even if it doesn't guarantee the absolute shortest path in all cases.
13. You are designing a database for a Library. Explain the relationship between a "Book" table and a "Borrower" table. Is it 1-to-1, 1-to-Many, or Many-to-Many? Justify your answer.
14. Explain the logic of a "Checksum". How is it used to verify data integrity during file transfer?
15. Compare and contrast the three fundamental paradigms of Machine Learning: Supervised Learning, Unsupervised Learning, and Reinforcement Learning.
16. A rectangle and a square have the same area. The square has a perimeter of 32 meters. The width of the rectangle is 4 meters. Find the length of the rectangle (in meters).
17. If 2 < x < 5 and 3 < y < 5, find the value of x − y in terms of inequality?
18. In a class, the number of boys is 35% more than that of the girls. The total number of students in the class is 94. If 6 more boys are admitted to the class, calculate the ratio of the number of boys to that of the girls.
19. A man can row 12 kmph in still water. It takes him thrice as long to row up as to row down the river. Find the rate of the stream.
20. **English Proficiency Related Questions.** From the parentheses in each sentence, write only the correct answer:
    - A. If the department had allocated more funds, the project (would succeed / would have succeeded).
    - B. By next month, the university (will have completed / will complete) the accreditation process.
    - C. Hardly (did the presentation begin / had the presentation begun) when the technical problems occurred.
    - D. The committee, as well as its sub-groups, (meets / meet) regularly to discuss policy matters.
    - E. He had better (leave / left) the station before it's too late.
    - F. The methodology section is comprehensive; (for example / however), the discussion lacks critical depth.
    - G. The research team arrived at (a / an) unanimous conclusion after extensive discussion.
    - H. The students were warned that any breach of conduct could result (in / to) suspension.
    - I. She is one of the scholars who (advocates / advocate) a critical pedagogy approach.
    - J. The researcher insisted that the data (be / is) analyzed before publication.
21. Write a paragraph on: **Street food culture in Dhaka**.
22. Make meaningful sentences with the following words. Do not change the grammatical category of the word: **Judicious; Condone; Fabricate; Accentuate; Multifaceted.**

---

## 3. Combined Bank — Assistant Programmer
**Exam date:** 09.02.2024 · **Exam taker:** BIBM · **21-year based** · **Source:** PDF pages 4–5 (printed pages 6–7)

1. Write a program to print prime numbers from 1 to n.
2. Write a program for Floyd's triangle, n = 5:

   ```text
   1
   0 1
   1 0 1
   0 1 0 1
   1 0 1 0 1
   ```
3. Write a C program to find the sum of the series: `1 + 2 + 4 + 7 + 11 + ... + N`.
4. What is Polymorphism? Discuss different types of Polymorphism with example.
5. What is Multithreading programming? Why is multithreading used in programming?
6. Discuss different types of relations in DBMS.
7. Difference between Stack and Queue. Write about 2 problems solved by stack and queue.
8. Find the output of the following recursion:

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
9. Which system did you build for a real-life software project? What problems did you face during that time and how did you solve this?
10. Assuming an Employees table with structure `employee_id`, `employee_name`, `department_id`, and `salary`, write queries:
    - To find the total number of employees in each department.
    - To calculate the average salary across all employees in the organization.
11. Write a short composition: **"The Role of Computers in the Education System in Bangladesh"**.
12. Write a letter to your younger brother about the importance of professional vocational training.

---

## 4. Combined Bank — Assistant Programmer
**Exam date:** 09.06.2023 · **Exam taker:** 20-year based · **Source:** PDF pages 5–6 (printed pages 7–8)

1. Given the following values, compute function point when all complexity adjustment factor (CAF) and weighting factors are average:
   - User Input = 50
   - User Output = 40
   - User Inquiries = 35
   - User Files = 6
   - External Interface = 4
2. Consider page reference string `1, 3, 0, 3, 5, 6, 3` with 3 page frames. Find the number of page faults. **[Page-replacement algorithm is not specified.]**
3. CRC is a redundancy error technique used to determine the error. Suppose the original data is `11100` and the divisor is `1001`.
4. Write a function to find the smallest element from an array.
5. Attacker steals private key of website that uses transport layer security and remains undetected. What can be done with a private key?
6. A & B two frames in a browser loaded from different origins. Why is it a reasonable security policy to allow A to navigate B to another origin based only on whether the display area of A contains display space of B and A has the control over the area?
7. Problem solved more efficiently in adjacency list representation than adjacency matrix representation and problem solved more effectively in adjacency matrix than adjacency list.
8. Suppose we have a relational database with five tables:

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

   **[The table notation is reproduced as printed; see original PDF page 6 if interpreting it as a schema.]**
9. A telephone line normally has a bandwidth of 3000 Hz (300 to 3300 Hz) assigned for data communication. The SNR is usually 3162. What will be the capacity for this channel?
10. Perform Max Heap insertion/deletion operations for the given array elements `[a, b, c, d, e, f, g, h, i, j]` step-by-step and show the final binary heap structure/tree representation.
11. Write a comprehensive essay on **"Digital Financial Literacy"**.

---

## 5. Bangladesh Bank — Assistant Programmer
**Exam date:** 03.02.2023 · **Exam taker:** BIBM · **Source:** PDF pages 6–8 (printed pages 8–10)

1. Consider a hash table of size 13 storing entries with integer keys. Suppose the hash function is `h(k) = k mod 13`. Insert in the given order entries with keys `10, 3, 6, 16, 17, 19, 10, 3, 6, 16, 17, 19` into the hash table using linear probing to resolve collisions. Show all the work.
2. Describe a man-in-the-middle attack on the Diffie-Hellman key exchange protocol in which the adversary generates two public key pairs for the attack.
3. Preserving confidentiality, integrity, and availability of data is a restatement of the concern over falsification, masquerade, and denial of service. Explain how the first three concepts relate to the last four. **[The source says "last four," although it lists three latter concerns.]**
4. Given two integers A and B as input, write a program to compute the least common multiple (LCM) of A and B.
5. Suppose that we have a relational database with the following tables. Underlined attributes represent primary keys:
   - Movies (mid, title, year)
   - People (pid, name)
   - Genres (gid, genre)
   - HasRole (pid, mid, role)
   - HasGenre (gid, mid)

   Write an SQL query to return the number of movies that are romantic comedies.
6. Consider the following Java code. Mention which of the methods overload, override, and hide superclass methods. What about the remaining method?

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
7. Given an adjacency list representation for a complete binary tree on 7 vertices, give the equivalent adjacency matrix representation. Assume that vertices are numbered from 1 to 7 as in a binary heap.
8. Draw a class diagram. A token-ring based local area network (LAN) is a network consisting of nodes in which network packets are sent around. Every node has a unique name within the network and refers to its next node. Different kinds of nodes exist: Workstations are originators of messages; servers and printers are network nodes that can receive messages. Packets contain an originator, a destination, and content, and are sent around on a network. A LAN is a circular configuration of nodes.
9. In order to prevent that, the company decided to add end-to-end encryption techniques. Which layer of the OSI model is suitable to work in, considering parameters like development time, software maintainability, and development cost? Give reasons for your concepts.
10. Essay: **"Growing use of technology in the Financial Service Industry."**
11. If x is an integer and `x + 1/x = 17/4`, then the value of `x − 1/x` = ?
12. A basketball team has won 15 games and lost 9. If these games represent 16⅔% of the games to be played, then how many more games must the team win to average 75% for the season?
13. Students of a class are made to stand in rows. If 4 students are extra in each row, then there would be 2 rows less. If 4 students are less in each row, then there would be 4 more rows. What is the number of students in the class?

---

## 6. Combined 4 Bank — Assistant Programmer
**Exam date:** 2020 · **Exam taker:** DU · **Source:** PDF page 8 (printed page 10)

1. Difference between spoofing and sniffing.
2. What is the full meaning of SQL? List the aggregate functions. Write SQL query of a table and its output.
3. What will be the output in C and Java code?
   - (i) C program code snippet.
   - (ii) Java program code snippet.

   **[The source lists snippets as prompts but does not supply their code.]**
4. What is Agile Methodology? Difference between Agile Model and Waterfall Model.
5. Linked list, doubly linked list and circular linked list explain with diagram.
6. Write down the functionality of OSI model.
7. How to determine the weighted graph has negative cycle?
8. Write a code in C/C++ that will output the 2nd largest number. (If N ≥ 1.)
9. X is an integer stream of N numbers. You have to select 2 data P and Q such that `A ≤ (P + Q) ≤ B`. Write an algorithm / pseudocode / C program to find how many ways you can select P & Q. The time complexity must be `O(N log N)`.

---

## 7. Bangladesh Bank — Data Entry Control Operator
**Exam date:** 16.10.2026 · **Source:** PDF page 9 (repeated on PDF pages 10–11; printed pages 11–13)

1. A computer has an Operating System (OS) installed on its SSD, and the SSD is detected in the BIOS. However, the computer boots from the network instead of the SSD. Which BIOS/UEFI setting should be changed to resolve this issue?
2. What is Two-Factor Authentication (2FA)? Define the CIA Triad.
3. Identify and explain the three main components of the following URL: `https://www.bb.org.bd/index.php`.
4. A computer's RAM has been upgraded from 8 GB to 16 GB, and its SSD capacity has been increased from 256 GB to 512 GB. Which upgrade allows the computer to run more applications simultaneously, and which upgrade allows it to store more data?
5. An email mailbox has a storage quota of 2 GB. The following storage is occupied:
   - Sent Items: 350 MB
   - Inbox: 1.25 GB
   - Trash: 900 KB
   - Drafts: 120 MB

   Given that 1 GB = 1,000 MB and 1 MB = 1,000 KB:
   - (a) How much mailbox storage is remaining?
   - (b) What should the email recipient do to receive a 300 MB file?
6. Discuss five advantages and five challenges of mobile banking.
7. Explain three fundamental principles of information security.

---

## 8. Bangladesh Bank — Assistant Director (ICT)
**Exam date:** 22.05.2025 · **Exam taker:** DU (CSE) · **Source:** PDF pages 11–13 (printed pages 13–15)

1. Write a C program or Pseudo code to find the similar elements of two arrays and print the similar elements along with the total number of similar elements.
2. For the Boolean expression `X =` **[expression missing in the source]**, construct and write the complete Truth Table.
3. What is the Total Latency for a 3-kbyte message (an e-mail) if the bandwidth of the network is 1 Gbps? Assume that the distance between the sender and the receiver is 300 km and light travels at a speed of `2 × 10⁸ m/s`. Given that Round Trip Time (RTT) is 50 ms and Queuing Time is 5 ms.
4. Consider the following snapshot of a system running the Banker's Algorithm with 5 processes and three resource types: A (10 Instances), B (5 Instances), C (3 Instances).

   | Process | Allocation A | B | C | Max Need A | B | C |
   |---|---:|---:|---:|---:|---:|---:|
   | P0 | 0 | 1 | 0 | 7 | 5 | 3 |
   | P1 | 2 | 0 | 0 | 3 | 2 | 2 |
   | P2 | 3 | 0 | 2 | 9 | 0 | 2 |
   | P3 | 2 | 1 | 1 | 2 | 2 | 2 |
   | P4 | 0 | 0 | 2 | 4 | 3 | 3 |

   - (i) Find and state the content of the Need Matrix.
   - (ii) Demonstrate whether the system is in a safe state or unsafe state. If safe, prove the safe execution sequence. `[BB AD ICT: 07.02.2025]`
5. Demonstrate the step-by-step construction of a Min Heap using the following set of given values: `12, 29, 33, 56, 66, 99, 100, 344`. Show the heap structure after each insertion.
6. A relational database schema for a Bank is given below: `Bank(Br_Name, Br_City, Assets, Acc_Name, Acc_Num, Balance)`.
   - (a) Identify the Functional Dependencies, decompose/normalize the schema up to 3NF, and explicitly point out the Primary Keys and Foreign Keys for each normalized table.
   - (b) Show the final structured design and clearly state the technical reasons why your decomposed schema is in a good form.
7. Sinthia wants to send an email to her friend Afsana. The communication flows through the Application layer and Transport layer of the OSI/TCP-IP model. [10]
   - (a) Mention the primary protocols used in both the Application layer and the Transport layer to support this functionality.
   - (b) Write down the detailed step-by-step process of Mail transfer from Sinthia's client environment to Afsana's mailbox.
8. Bangladesh Bank operates an internal client-server architecture communicating with a Mail Server, a DNS Server, and a Web Server. The bank network administration intends to maximize security by enforcing Firewall protection on these servers. Draw a clean network architecture diagram reflecting this secure infrastructure scenario.
9. Solve the following mathematical and analytical problems:
   - (a) Evaluate the definite integral: `∫₀² (2x² + 3x) dx`.
   - (b) In Bangladesh Bank, there are 6 Assistant Directors (ADs) and 4 Deputy Directors (DDs). Each AD always brings a bag to the workplace, whereas only half of the DDs bring a bag. If a bag is selected completely at random from all the bags brought to the office, what is the probability that the chosen bag belongs to a Deputy Director (DD)?
10. **Language Proficiency and Analytical Technical Writing:**
    - (a) Translate the following sentences from Bengali to English:
       - (i) শনিবার হতে সে অফিসে আসছে না।
       - (ii) আপনার ব্যাংক অ্যাকাউন্ট এর স্থিতি জানার জন্য মোবাইল ব্যাংকিং অ্যাপ্লিকেশন এ লগইন করুন।
    - (b) Focus Writing (Short Note): Write a comprehensive short note on: **"The role of Artificial Intelligence (AI) and Machine Learning in mitigating the challenges of cyber attacks on the banking system."**

---

## 9. Combined 2 Banks — Assistant Network System Engineer (ANSE)
**Exam date:** 16.10.2026 · **Job ID:** 25109 · **25-year based** · **Source:** PDF pages 13–15 (printed pages 15–17)

1. **Bangla Focus Writing:** তথ্য প্রযুক্তির যথাযথ ব্যবহার ও সচেতনতা বৃদ্ধিতে করণীয়।
2. **English Focus Writing:** Data security challenges in banks and protection guidelines.
3. **General Knowledge:**
   - (A) How many basic pillars does the Constitution of Bangladesh have?
   - (B) Which agreement led to an end of the First World War?
   - (C) Roscosmos is the aerospace agency of which country?
   - (D) The Durand Line is the border between which two countries?
   - (E) COP30 was held in which continent?
   - (F) Which is the first paperless city in the world?
   - (G) What is the name of China's commercial aircraft manufacturer?
   - (H) Where is the Shat Gombuj Mosque located?
   - (I) How many foreign banks currently operate in Bangladesh?
   - (J) In relation to product export, what does DDP stand for?
4. State the main purpose of Spanning Tree Protocol (STP) in Ethernet networks. Explain how switching loops occur in a network. Briefly explain how STP prevents switching loops.
5. Explain the main differences between IPv4 and IPv6 addressing. Include at least three key differences and state the IPv6 equivalent of ARP.
6. Explain the role of Link-State Advertisements (LSAs) in OSPF and how the Dijkstra SPF algorithm uses the information contained in LSAs to build the routing table.
7. What is Dynamic ARP Inspection (DAI)? How does it detect and prevent ARP spoofing attacks? Explain how Dynamic ARP Inspection (DAI) uses the DHCP snooping binding database to prevent ARP spoofing attacks in a switched enterprise network.
8. Using VLSM, subnet the block `10.100.0.0/22` to allocate address space for the following departments. Write the Subnet Address and CIDR mask for each. Allocate efficiently and show the order of allocation.
   - Dept A: 250 hosts
   - Dept B: 120 hosts
   - Dept C: 50 hosts
   - **[The fourth bullet in the source is blank.]**
9. List the top five steps of the BGP path-selection decision process in priority order (highest priority first). Briefly describe how each criterion influences the selection of the best route when multiple routes to the same destination are available.
10. Explain how Port Address Translation (PAT) works and why it is more commonly used than Static or Dynamic NAT in most enterprise and home networks.
11. What is network topology? Explain the different network topologies.
12. Draw and explain the seven layers of the OSI model.
13. Differentiate between a firewall, an Intrusion Detection System (IDS), and an Intrusion Prevention System (IPS), and explain how each contributes to network security.
14. Divide the network `192.168.10.0/24` into four equal-sized subnets and determine the following for each subnet:
    - Network address
    - Subnet mask
    - Usable host range
    - Broadcast address
15. A computer can ping `8.8.8.8` but cannot access websites using domain names. Explain the likely cause and describe how you would diagnose and resolve the problem using standard network utilities.
16. Explain how a Man-in-the-Middle (MitM) attack can compromise a customer's online banking session and describe technologies to mitigate the threat.
17. Several computers in a bank branch become encrypted by ransomware. Describe the immediate actions the IT team should take in chronological order.
18. Consider `Employees (EmpID, Name, Department, Salary)`. Write an SQL query to retrieve employees whose salaries are greater than the average salary of their respective departments.
19. Explain the meaning of `chmod 750 backup.sh` and `chown root:admin backup.sh`. Write a command to grant the owner read/write/execute permissions, the group read/execute permissions, and no permissions to others.

---

## 10. RAKUB — Assistant Network System Engineer (ANSE)
**Exam date:** 05.06.2026 · **Exam taker:** E-Zone · **23-year based** · **Source:** PDF pages 15–16 (printed pages 17–18)

1. A high traffic web application suddenly begins failing with database connection timeouts under peak load. At the same time, the underlying Linux OS kernel hosting the database reports "too many open files" error and network socket exhaustion. Explain the root cause of this failure at the Linux OS kernel level.
2. Differentiate process from a thread regarding memory space allocation.
3. State the exact administrative activity performed by running the command `chmod 755 script.sh` on a Linux target file.
4. An engineering model is deployed to identify critical network hardware failures. Explain why an administrator must optimize for recall instead of precision if the business penalty for a missed failure is catastrophic.
5. What is Cross Site Scripting? Reflected XSS & stored XSS in terms of how the payload is delivered to the victim.
6. Define Amdahl's law. How does it mathematically dictate the absolute maximum performance speedup a system can achieve when adding more CPU cores?
7. Excessive broadcast traffic in LAN. What is the cause and solution?
8. A net link utilizes 16QAM. If the underlying signal system operates at baud rate 2400 Baud, calculate exact corresponding data in bps.
9. IPv6 headers enable faster processing and resulting throughput across intermediate transit routers than the legacy IPv4. Explain the key reasons.
10. A core router receives a packet with destination IP address `192.168.20.45`. The router's forwarding table contains the following overlapping routes: `192.168.0.0/16`, `192.168.16.0/20`, `192.168.20.0/22`, `192.168.20.32/27`. Identify the exact routing interface the router will use to forward this packet.
11. A corporate network pool experiences exhaustion due to a high volume of transient guest devices. What lease duration parameters adjustment resolves this?
12. Difference between compile-time polymorphism & run-time polymorphism.
13. Explain the distinct filtering behaviors of a WHERE clause versus a HAVING clause within a SQL statement containing an aggregate execution layout.
14. Describe run-time error vs compile-time error.
15. A satellite link has a one-way propagation delay of 250 ms and a transmission rate 1 Mbps. Frame size 1000 bytes; calculate utilization efficiency if stop-and-wait protocol is used. What is the minimum window size required to achieve 100% efficiency?

---

## 11. Combined Bank — Officer (IT)
**Exam date:** 31.07.2026 · **Job ID:** 25105 · **24-year based** · **Source:** PDF pages 16–18 (printed pages 18–20)

1. **Focus Writing in Bangla:** বাংলাদেশের অর্থনৈতিক খাতে খেলাপি ঋণ: কারণ, প্রভাব ও উত্তরণের উপায়।
2. **Focus Writing in English:** The Role of Sustainable Banking in Achieving the UN Sustainable Development Goals (SDGs) in Bangladesh.
3. **Translate the following passage into English:**

   > এক ক্ষুধার্ত শিয়াল একটি আঙুর ক্ষেতের পাশ দিয়ে যাচ্ছিল। উঁচুতে ঝুলে থাকা আঙুর দেখে সে তা খাওয়ার চেষ্টা করল, কিন্তু বারবার লাফিয়েও ব্যর্থ হলো। অবশেষে সে হতাশ হয়ে চলে গেল। যাওয়ার সময় বলল, আঙুরগুলো আসলে টক।

4. **Translate the following passage into Bangla:**

   > The boy found a lost wallet on his way to school. Instead of keeping it, he looked for the owner and returned it. The owner, impressed by his honesty, offered him a reward. The boy politely refused, saying that honesty is its own reward.

5. **General Knowledge (10 Marks):**
   - Which river is known as the "Lifeline of Bangladesh"?
   - What is the name of the international organization that monitors global health standards and coordinates the response to pandemics?
   - What is the name of Bangladesh's first deep-sea port?
   - Where is the headquarters of the International Monetary Fund (IMF) located?
   - Which country has the world's longest coastline?
6. An organization has been assigned the IPv4 network address `192.168.1.0/24`. As part of the network deployment, the network administrator is required to divide the address space into four equal-sized subnets to support different departments. Determine the Network Address, Subnet Mask (both CIDR and dotted-decimal notation).
7. Differentiate between a Fuse and a Miniature Circuit Breaker (MCB). Which one is more suitable for modern office electrical installations and why?
8. Explain the working principle of a PN junction diode. Draw its symbol and describe the difference between forward bias and reverse bias.
9. Differentiate between a Computer Virus and a Computer Worm based on how they spread and replicate across host networks.
10. Draw the circuit schematic diagrams to build an Exclusive-OR (XOR) logic function using only universal NAND gates.
11. What is the difference between a Multiplexer and a Demultiplexer? Explain one practical application of each in digital systems.
12. Explain the concepts of Inheritance and Polymorphism in Java. Write a Java program to demonstrate method overriding.
13. Describe any two key differences between the HTTP GET and HTTP POST methods used for communication between a web browser and a web server.
14. A physical server has 32 CPU cores, 96 GB RAM, and 4 TB storage. Each virtual machine (VM) requires 4 CPU cores, 16 GB RAM, and 500 GB storage. Calculate the maximum number of VMs that can be hosted on the server without overcommitting resources. Identify which hardware resource limits the number of VMs.
15. What is JDBC? Explain the steps required to connect a Java application to a MySQL database.
16. Describe the SQL Injection and Cross-Site Scripting (XSS) web security threats and suggest preventive measures for each.
17. Describe the functions of a Switch and a Router and explain two key differences between these networking devices.
18. A system has three processes with the following arrival times and CPU burst times:

    | Process | Arrival Time | Burst Time |
    |---|---:|---:|
    | P1 | 0 | 5 |
    | P2 | 1 | 3 |
    | P3 | 2 | 2 |

    Using the First-Come, First-Served (FCFS) CPU scheduling algorithm, calculate the average waiting time and the average turnaround time.
19. An institute wants to create a database table named `STUDENT` to store student information. The table should include the columns Roll Number, Name, Department, Email, and Admission Date. Specify the most appropriate SQL data type for each column and identify which column should be defined as the Primary Key, giving a brief justification for your choice.
20. A software company has been hired to develop an Online Library Management System for a university. The librarian wants the system to be delivered in phases so that feedback from users can be incorporated after each release. As a software developer, identify the most suitable Software Development Life Cycle (SDLC) model for this project. Justify your choice by mentioning two advantages of the selected model.

---

## 12. Combined Bank — Officer (IT)
**Exam date:** 09.05.2026 · **Job ID:** 10229 · **23-year based** · **Source:** PDF pages 18–19 (printed pages 20–21)

1. What is a communication system? Describe the different types of transmission modes with examples.
2. Explain the concepts of encryption and decryption with an example.
3. Explain how any Boolean function can be implemented using only universal gates.
4. Differentiate between system software and application software.
5. What are the main phases of the Software Development Life Cycle (SDLC)? Explain each phase briefly.
6. What is cloud computing? Why is it used? State the difference between cloud storage and traditional storage.
7. What is a phishing attack? Explain its types and discuss methods to prevent it.
8. Compare RAM, ROM, cache memory, and secondary storage in terms of speed and usage.
9. What does CIA stand for in information security? Explain each component briefly.
10. Consider a STUDENTS table with the following attributes: `StudentID, Name, Department, Marks (10 Marks)`:
    - (I) Write an SQL query to display only `StudentID, Name, and Marks` for students scoring more than 80 marks.
    - (II) Write an SQL query to count how many students scored more than 80 marks in each Department.
11. What are the different types of relationships in a relational database? Explain each with examples.
12. Multi-Factor Authentication (MFA) is mandatory in modern banking infrastructure. (a) Define the concept of MFA and explicitly list the three globally recognized categories of authentication factors.
13. Storage technology selection directly impacts banking operations. Server A will host the Core Banking Database. Server B will host 10 years of immutable archive data. Compare Hard Disk Drives (HDD) and Solid State Drives (SSD).
14. Network Address Translation (NAT) maps internal networks to the public internet.
    - (a) Explain the historical IP addressing limitation that made NAT a necessity globally.
    - (b) Explain the step-by-step logical translation process that occurs at a branch router when an internal employee (IP `192.168.1.5`) sends a web request to an external server, and how the router correctly handles the returning response packet.
15. Subnetting logic requires precise binary calculation. A network engineer is tasked with dividing the internal network `192.168.10.0/24` into exactly 4 equal subnets for four different bank branches. Show the mathematical calculation to determine how many bits must be borrowed to create 4 subnets, and state the new Subnet Mask in both CIDR notation and decimal format.

---

## 13. Combined Bank — Officer (IT)
**Exam date:** 03.01.2026 · **Job ID:** 10209 · **22-year based** · **Source:** PDF pages 19–20 (printed pages 21–22)

1. Mention the layers of the OSI Model and the function of each layer.
2. Compare TCP and UDP protocols with examples.
3. Explain the difference between compiler and interpreter.
4. What is cloud computing? Mention its service models.
5. What is authentication and authorization? What is the CIA triad in cyber security? How does it work?
6. What is the difference between functional and non-functional requirements? What is requirement validation?
7. What is social engineering? What is hashing? How is it different from encryption?
8. Critically analyze the limitations of the Waterfall model and explain how Agile methodologies address those limitations.
9. Define Virtualization. Explain the role of the Hypervisor and the difference between a Virtual Machine (VM) and a Container.
10. A new employee joins the bank. Describe the process of creating a new user account for them, focusing on security best practices (e.g., password policies).
11. Construct a Truth Table for a system that triggers an Alarm (Output 1) if: (Motion is Detected AND it is Night Time) OR (Panic Button is Pressed).
12. Based on the information given below, can User X write to Folder 1? Explain the precedence logic (Explicit Deny vs Explicit Allow) Access Logic.
    - User X belongs to Group A and Group B.
    - (i) Folder 1 grants "Read" to Group A.
    - (ii) Folder 1 has an "Explicit Deny Write" for Group B.
    - (iii) Folder 1 grants "Write" to User X individually.
13. You have 4 Hard Drives of 2 TB each. Calculate usable storage for RAID 0, RAID 5, and RAID 10.
14. Arrange the following in the correct chronological order of a computer's boot process: (OS Kernel Load, BIOS/UEFI POST, MBR/GPT Lookup, User Login, Driver initialization).
15. You have table `EMPLOYEES (ID, Name, DeptID)` and table `DEPARTMENTS (DeptID, DeptName)`. Write the logical steps for pseudo-SQL logic to get a list of Employee Names who work in "IT".

---

## 14. Combined Bank — Senior Officer (IT)
**Exam date:** 25.07.2026 · **Exam taker:** E-Zone · **24-year based** · **Source:** PDF pages 20–23 (printed pages 22–25)

1. **Focus Writing in Bangla:** বাংলাদেশের ব্যাংকিং খাতে চতুর্থ শিল্পবিপ্লবের (4th Industrial Revolution) প্রভাব: ডিজিটাল ব্যাংকিংয়ের সম্ভাবনা, আধুনিক প্রযুক্তির ব্যবহার, গ্রাহকসেবার পরিবর্তন এবং সংশ্লিষ্ট প্রযুক্তিগত চ্যালেঞ্জসমূহ বিশ্লেষণ করুন।
2. **Focus Writing in English:** The Importance of Digital Literacy in Expanding Cashless Transactions in Bangladesh: Discuss how digital skills influence financial inclusion, the adoption of digital payment systems, and the challenges of building a cashless economy.
3. **Translate the following passage into English:**

   > “কথায় আছে, সময়ের এক ফোঁড় অসময়ের দশ ফোঁড়। অথচ আমরা আজ করব কাল করব বলে কাজ ফেলে রেখে ভাগ্যের দোহাই দিতে পছন্দ করি। আকাশকুসুম কল্পনা করে জীবনে রাতারাতি সফল হওয়া যায় না। যে জাতি যত বেশি পরিশ্রমী, সে জাতি তত বেশি উন্নত। তাই কথায় কথায় অজুহাত না দেখিয়ে আমাদের এখনই কাজে নেমে পড়া উচিত।”

4. **Translate the following passage into Bangla:**

   > He decided to pull out of the agreement at the eleventh hour. This sudden move took everyone by surprise and put the entire project at stake. He had informed the team beforehand, we could have easily made alternative arrangements. Now, we are left with no other choice but to start everything from scratch. It just goes to show that you cannot always take people at their word.

5. **General Knowledge (10 Marks):**
   - What is the full form of NPSB in the banking sector of Bangladesh?
   - Who is the architect of the National Martyrs' Memorial in Savar?
   - What is the name of the central bank of the United Kingdom?
   - Which international organization publishes the "World Economic Outlook" report?
   - What is the name of the first submarine communications cable system that Bangladesh is connected to?
6. Why do modern processor designs favor a multi-stage pipelined approach over a single-cycle implementation?
7. Explain the operational difference between Hashing and Encryption.
8. Explain the difference between a "Compulsory Miss" (Cold Miss) and a "Capacity Miss" in cache memory.
9. Consider the following relation: `Employee(EmpID, Name, Department, Salary)`. Write an SQL query to retrieve the Department, the total number of employees, and the average salary for each department. The output should display one record for each department.
10. Explain the difference between Unit Testing and Integration Testing.
11. Why is a **Circular Queue** preferred over a **Linear Queue** in many operating systems? Explain with one example.
12. What do the following specific HTTP status codes mean? Write down the exact standard text phrase for each:
    - (a) 200
    - (b) 403
    - (c) 503
13. Simplify the following Boolean expression using a 4-variable K-map: `F(A,B,C,D) = Σ m(0,3,5,7,8,10,11,12,13,14,15)`. Draw the K-map grid, clearly show your groupings (loops), and write the final simplified Sum-of-Products (SOP) expression.
14. Five channels, each with a 100-kHz bandwidth, are to be multiplexed together. What is the minimum bandwidth of the link if there is a need for a guard band of 10 kHz between the channels to prevent interference?
15. An organization is granted the IPv4 network block `14.24.74.0/24` and needs to segment it into two subnets: Subnet A (requires 120 addresses) and Subnet B (requires 60 addresses). Allocating sequentially from the requirement first to maximize remaining address space, state only the Network Address (with its CIDR mask) and the Broadcast Address for both subnets.
16. A startup company wants to launch a new web application. They do not want to manage any underlying hardware, operating systems, or even the runtime environment; they only want to focus on writing and deploying their code. Based on your understanding of Cloud Service Models, which model (IaaS, PaaS, or SaaS) is most appropriate for them? Provide two real-world examples of platforms that provide this specific type of service.
17. Define the following terms used in tree data structures: (i) Tree, (ii) Leaf Node, (iii) Internal Node, and (iv) Height of a Tree. Provide a suitable example to illustrate each term.
18. Consider the following Java program and determine the integer value printed by the execution of the `main()` method.

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
19. An array contains one million sorted integers. Which searching algorithm would you choose to find a given element? Justify your answer.
20. Consider the grammar:

    ```text
    E -> E + E | E * E | id
    ```

    Show that the grammar is ambiguous for the string: `id + id * id`.

---

## 15. Combined Bank — Senior Officer (IT)
**Exam date:** 22.05.2026 · **Job ID:** 10225 · **23-year based** · **Source:** PDF pages 23–24 (printed pages 25–26)

1. What is Object-Oriented Programming (OOP)? What are the main principles of OOP? What is the difference between Method Overloading and Method Overriding?
2. Describe the phases of the Software Development Life Cycle (SDLC).
3. What is the OSI model? Explain the functions of each layer with examples.
4. Define Computer Network. Describe different types of Computer Networks.
5. Draw and clearly describe a step-by-step flowchart for a User Login system. Your login must include:
   - Taking a Username and Password as input.
   - Checking the database.
   - If correct: Granting access.
   - If wrong: Adding 1 to a "failed attempts counter."
   - Access denied blocks the account if the counter reaches 3.
6. What is Cloud Computing? What are its characteristics? Briefly describe the types of cloud computing and its applications.
7. A bank has the network block `192.168.10.0/24`. The IT manager wants to divide this into 4 equal subnets.
   - (a) How many bits do you need to borrow to make 4 subnets?
   - (b) What is the new Subnet Mask in dotted-decimal format?
   - (c) Write down the Network Address, the First Usable IP, and the Broadcast Address for the second subnet created. Show your calculation.
8. Why is cyber security important? What are the common types of cyber threat? Explain cyber security measures.
9. What is Encryption? What are the types? Explain the role of Encryption in security.
10. What is Normalization? How 1NF and 2NF works in database? Give examples.
11. What is a Linked List? What is searching? Explain Binary Search.
12. What is Cryptocurrency? What is Bitcoin? What are the advantages of Blockchain Technology?
13. A database has a Managers table and an Employees table. The Employees table references the Managers table using a Foreign Key. The database is set to `ON DELETE CASCADE`.
    - (a) Explain what `ON DELETE CASCADE` means in simple English.
    - (b) If you delete one Manager from the database, what will automatically happen to all Employees under that manager?
    - (c) Explain why this is very dangerous in a real banking system. What is the best practice and how does it fix this danger?
14. Explain the basic idea of RAID. Why do servers use multiple hard drives instead of one big drive? If you have six drives of 2 TB each in a RAID 6 setup, calculate the total usable storage space.
15. What are Compilers and Interpreters? Briefly describe their role and difference. Write some key points of advantages and disadvantages of Open Source Software.

---

## 16. Combined Bank — Senior Officer (IT)
**Exam date:** 17.10.2025 · **Job ID:** 10205 · **22-year based** · **Exam taker:** E-Zone · **Source:** PDF pages 24–26 (printed pages 26–28)

1. Determine whether the following pair of graphs are isomorphic, and justify your answer in one sentence. **[The pair of graphs is not included on the source page.]**
2. Explain the Quick Sort algorithm with a suitable example. Under what conditions does Quick Sort exhibit its worst-case time complexity, and why does this situation occur?
3. Consider a logical address space of 512 pages, each of 2-KB page size, mapped onto a physical memory containing 128 frames.
   - (a) How many bits are required in the logical address?
   - (b) How many bits are required in the physical address?
4. Why does the Domain Name System (DNS) primarily use UDP as its transport layer protocol instead of TCP? Describe the sequence of events that take place during the DNS name resolution process when a user enters into a web browser and presses enter.
5. Explain the concept of thrashing in an operating system, describing how it occurs in a demand-paged virtual memory system and how it impacts CPU utilization and overall system performance.
6. Write a structured program (in C or Python) that takes an integer input n and prints the sum of all even numbers from 1 to n.
7. Write a program using any object-oriented language (e.g., C++ / Java / Python) to represent a Bank Account. Your program should include:
   - (i) A class BankAccount with data members for account holder's name, account number, and balance.
   - (ii) Member functions to deposit money, withdraw money (ensuring sufficient balance), and display account details.
   - (iii) Demonstrate the concept of encapsulation by keeping data members private and providing appropriate public methods for accessing and modifying them.
8. Explain the difference between direct, immediate, and register addressing modes in the 8086 microprocessor.
9. Consider the following relation: `Sales(sales_id, salesman, region, sale_amount, sale_date)`. Write an SQL query to display the region, average sale amount, and total number of sales for each region where the average sale amount exceeds BDT 50,000 and the total number of sales in that region is at least 5.
10. Explain the concept of ACID properties in a database transaction. Describe how each property—Atomicity, Consistency, Isolation, and Durability—ensures the reliability and integrity of a database system.
11. What are SOAP and RESTful APIs in web services? State one main difference between SOAP and REST in terms of how they exchange data.
12. Explain the concepts of Reinforcement Learning (RL), Deep Learning (DL), and Federated Learning (FL) in the context of Machine Learning. Briefly describe how each approach differs in its learning mechanism, data usage, and real-world applications.
13. Imagine a government agency is developing an AI-based citizen service chatbot that can automatically generate responses, summarize documents, and provide policy information to citizens. Explain how Generative AI can be used to power such a system, and how Explainable AI (XAI) techniques can ensure that its responses are transparent, reliable, and accountable.
14. Describe how the principles of Confidentiality, Integrity, and Availability work together to protect organizational data, and provide one real-world example of a security breach where one or more of these principles were compromised.
15. A banking application requires users to enter a 4-digit PIN for login. Explain how you would test this input field to ensure that it accepts only valid 4-digit numbers and rejects invalid inputs. Mention a few test cases you would include and explain why such testing is important for system security and reliability.

---

## 17. Combined Bank — Assistant Engineer
**Exam date:** 08.05.2026 · **Exam taker:** E-Zone · **23-year based** · **Source:** PDF pages 26–28 (printed pages 28–30)

1. A maintenance engineer is setting up a RAID 5 array with five hard drives, each having a capacity of 4 TB. What is the total usable storage capacity, and why is it not 20 TB?
2. Distinguish between Preventive and Corrective maintenance with a real-world example for each in a data center environment. A critical system consists of three components (Power Supply, Motherboard, and Storage) connected in a series configuration. If each component has a reliability of 0.95, what is the total reliability of the system?
3. At which layer of the OSI model does a standard Router primarily operate, and what is the specific name of the Protocol Data Unit (PDU) at this layer? A router has four contiguous /24 routing table entries: `10.1.0.0/24`, `10.1.1.0/24`, `10.1.2.0/24`, and `10.1.3.0/24`. If you summarize (supernet) these into a single route, what will be the new CIDR notation?
4. What does the Consistency property in ACID guarantee during a bank fund transfer transaction? You are designing the schema for a Savings_Accounts table. Write the specific SQL constraint clause to ensure that the `current_balance` column can never drop below zero.
5. Briefly explain "Circular Wait." In a Resource Allocation Graph, if a cycle exists, does it absolutely guarantee that a Deadlock has occurred? Explain briefly.
6. A server suddenly starts sending abnormal traffic to external systems. Analyze the possible cause and suggest immediate actions.
7. Read the three real-world web development scenarios below. For each scenario, identify the single most appropriate HTTP Status Code from the provided list that the server should return.

   **Codes to choose from:** 204, 301, 400, 403, 503.
   - **(i) Scenario A:** A client sends a POST request to create a new user, but the JSON payload is malformed and missing a required bracket, making it impossible for the server to parse the data.
   - **(ii) Scenario B:** A user is successfully logged in, but they attempt to access a `/admin/settings` endpoint. They only have standard user privileges, not administrator rights.
   - **(iii) Scenario C:** A client successfully sends a DELETE request to remove a photo. The photo is deleted, and the server needs to acknowledge the success but has no actual data or message to send back in the response body.
8. Simplify the following Boolean expression using a 4-variable K-map: `F(A,B,C,D) = Σ m(0,3,5,7,8,10,11,12,13,14,15)`. Draw the K-map grid, clearly show your groupings (loops), and write the final simplified Sum-of-Products (SOP) expression. `[Combined Bank SO IT — 25.07.2026]`
9. Design a scalable big data analytics pipeline for an e-commerce platform that ingests real-time logs, stores petabyte-scale data, supports batch and stream processing, delivers near real-time recommendations, and runs large-scale machine learning models; from the following Hadoop ecosystem components — *MapReduce, HDFS, YARN, HBase, ZooKeeper, Pig, Hive, Mahout, Chukwa, Cassandra, Avro, Oozie, Flume, Sqoop* — select any five and explain the role of each component in this system.
10. (i) For securing a bank's sensitive customer data, what is the fundamental difference in the specific technologies used to protect "Data in Transit" versus "Data at Rest"?

    (ii) What defines a "Zero-Day" vulnerability, and why do traditional signature-based antivirus solutions fail to protect a bank's servers against them?
11. Let M be a 3 × 3 real matrix with eigenvalues 1, 2, and 3. What is the determinant of the matrix `M² − M + I`, where I is the 3 × 3 identity matrix?
12. Two machines, A and B, manufacture 60% and 40% of the total daily production of a factory, respectively. It is known that 2% of the items produced by machine A are defective, and 5% of the items produced by machine B are defective. If a randomly chosen item from the daily production is found to be defective, what is the probability (expressed as a decimal) that it was produced by machine B?
13. In each of the following questions, a related pair of words is given in capital letters. Select the option that best expresses a relationship similar to that expressed in the original pair.

    **(i) FAMISHED : HUNGRY :: ______ : ______**
    - A) wealthy : poor
    - B) meticulous : careful
    - C) treacherous : reliable
    - D) agile : clumsy

    **(ii) CACOPHONY : SOUND :: ______ : ______**
    - A) chorus : melody
    - B) aroma : smell
    - C) glare : light
    - D) flavor : taste

---



# Bangladesh Bank — Assistant Director (ICT)

**Exam date:** 22.05.2025 · **Exam taker:** DU (CSE) ·

---

1. Write a C program or Pseudo code to find the similar elements of two arrays and print the similar elements along with the total number of similar elements. **[10]**

---

2. For the Boolean expression:

```

X = AB + (A + B) · C

```

construct and write the complete Truth Table. **[10]**

---

3. What is the Total Latency for a 3-kbyte message (an e-mail) if the bandwidth of the network is 1Gbps? Assume that the distance between the sender and the receiver is 300 km and light travels at a speed of 2 × 10⁸ m/s. Given that Round Trip Time (RTT) is 50 ms and Queueing Time is 5 ms. **[10]**

---

4. Consider the following snapshot of a system running the Banker's Algorithm with 5 processes (P₀ through P₄) and 3 resource types: A (10 instances), B (5 instances), and C (7 instances) at time T₀:

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

**[10]**

---

### 5. Demonstrate the step-by-step construction of a **Min Heap** using the following set of given values:

```

12, 29, 33, 56, 66, 99, 100, and 344

```

Show the heap structure after each insertion. **[10]**

---

### 6.A relational database schema for a Bank is given below:

```

Bank(Br_Name, Br_City, Assets, Acc_name, Acc_Num, Balance)

```

(a). Identify the Functional Dependencies, decompose/normalize the schema up to **3NF**, and explicitly point out the **Primary Keys** and **Foreign Keys** for each normalized table.

(b). Show the final structured design and clearly state the technical reasons why your decomposed schema is in a good form.

---

### 7. Sinthia wants to send an email to her friend Afsana. The communication flows through the Application layer and Transport layer of the OSI/TCP-IP model.

(a) Mention the primary protocols used in both the Application layer and the Transport layer to support this functionality.

(b) Write down the detailed step-by-step process of Mail transfer from Sinthia's client environment to Afsana's mailbox.


---

### 8. Bangladesh Bank operates an internal client-server architecture communicating with a Mail Server, a DNS Server, and a Web Server. The bank network administration intends to maximize security by enforcing Firewall protection on these servers. Draw a clean network architecture diagram reflecting this secure infrastructure scenario. 
---

### 9. Solve the following mathematical and analytical problems:

(a) Evaluate the definite integral:

\[
\int_0^2 (2x^2 + 3x)\,dx
\]

(b) In Bangladesh Bank, there are 6 Assistant Directors (ADs) and 4 Deputy Directors (DDs). Each AD always brings a bag to the workplace, whereas only half of the DDs bring a bag. If a bag is selected completely at random from all the bags brought to the office, what is the probability that the chosen bag belongs to a Deputy Director (DD)?
---

### 10. Language Proficiency and Analytical Technical Writing:

(a). Translate the following sentences from Bengali to English:

1. নিরাপত্তা হতে জল অপচয় করা যায় না।  
2. আপনার ব্যাংক অ্যাকাউন্টের স্থিতি জানার জন্য মোবাইল ব্যাংকিং অ্যাপ্লিকেশন এ লগইন করুন।

### (b) Focus Writing (Short Note)

Write a comprehensive short note on:

**"The role of Artificial Intelligence (AI) and Machine Learning in mitigating the challenges of cyber attacks on the banking system."**

**Target word count: 100 to 150 words.**

<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>






*End of extracted questions. Notes and annotations in square brackets identify omissions or ambiguities found in the scanned source; they are not model-supplied questions.*
