অবশ্যই। **Software Project Estimation → Function Point Analysis (FPA)** পরীক্ষার জন্য সহজভাবে বুঝতে হলে প্রথমে একটা মূল ধারণা মনে রাখুন:

> **Function Point (FP) হলো Software কতটুকু functionality/user-service দিচ্ছে—তা মাপার একটি unit।**

অর্থাৎ, **কত লাইন কোড লিখতে হবে (LOC)** সেটা না দেখে, software-এর **কী কী কাজ করার capability আছে** সেটা দেখে size estimate করা হয়।

---

# 1. Function Point Analysis (FPA) কী?

**Function Point Analysis (FPA)** হলো software-এর size/functional complexity estimate করার একটি পদ্ধতি।

এটি সাধারণত ব্যবহার করা হয়:

* Software size estimate করতে
* Development effort estimate করতে
* Development cost estimate করতে
* Development time estimate করতে
* বিভিন্ন software project-এর size compare করতে

### সহজ উদাহরণ

ধরুন একটি **Banking System** আছে:

* Customer login করতে পারে
* টাকা জমা দিতে পারে
* টাকা তুলতে পারে
* Account balance দেখতে পারে
* Transaction history দেখতে পারে

এখানে আমরা সরাসরি বলব না:

> "এই software-এ 20,000 lines of code লাগবে।"

বরং দেখব:

> "Software কতগুলো input, output, query, file এবং external interface provide করছে?"

এগুলো থেকে **Function Point** calculate করা হয়।

---

# 2. FPA-এর 5টি প্রধান Function Type

এটা সবচেয়ে গুরুত্বপূর্ণ অংশ। **FPA-তে 5 ধরনের function** থাকে।

মনে রাখার shortcut:

### **EI – EO – EQ – ILF – EIF**

| Function | Full Form               | সহজ অর্থ                             |
| -------- | ----------------------- | ------------------------------------ |
| **EI**   | External Input          | বাইরের source থেকে data system-এ আসে |
| **EO**   | External Output         | System থেকে processed data বাইরে যায় |
| **EQ**   | External Inquiry        | Data search/query করা হয়             |
| **ILF**  | Internal Logical File   | System নিজে যে data maintain করে     |
| **EIF**  | External Interface File | অন্য system-এর data ব্যবহার করে      |

---

# 3. External Input (EI)

### EI = External Input

User বা external system থেকে **data system-এর ভিতরে প্রবেশ করে**।

### Example:

Banking System:

* Customer registration
* New account creation
* Deposit money
* Withdraw money
* Update profile

এগুলোতে external source থেকে data system-এ প্রবেশ করছে।

তাই এগুলো **EI**।

### মনে রাখবেন:

> **Data comes INTO the system → EI**

---

# 4. External Output (EO)

### EO = External Output

System থেকে user/external system-এর কাছে **processed information বের হয়**।

এখানে শুধু data display নয়; সাধারণত system কিছু **processing/calculation** করে output তৈরি করে।

### Example:

Banking System:

* Monthly account statement
* Salary report
* Profit calculation report
* Transaction summary
* Tax report

যেমন:

```text
Deposit = 50,000
Interest = 2,500

Total = 52,500
```

System calculation করেছে এবং output দিয়েছে।

তাই এটি **EO**।

### Shortcut:

> **Processed data goes OUT → EO**

---

# 5. External Inquiry (EQ)

### EQ = External Inquiry

User system-কে কোনো information সম্পর্কে **query/search** করে এবং system existing data থেকে answer দেয়।

এখানে সাধারণত **significant calculation/processing থাকে না**।

### Example:

Banking System:

* Account balance check
* Search customer
* View transaction history
* Search account by account number

যেমন:

```text
User:
Account No = 12345

System:
Balance = 50,000
```

এখানে system existing information retrieve করে দেখিয়েছে।

তাই এটি **EQ**।

### EO বনাম EQ

এটা পরীক্ষায় খুব গুরুত্বপূর্ণ।

**EQ:**

> Search/retrieve existing information

**EO:**

> Processing/calculation করে output তৈরি করা

---

# 6. Internal Logical File (ILF)

### ILF = Internal Logical File

Software নিজে যে logical data maintain করে।

সহজভাবে:

> **নিজের database-এর logical data group**

### Example:

একটি Banking System-এর database:

```text
Customers
Accounts
Transactions
Loans
Employees
```

যদি এগুলো application নিজেই create/update/delete/manage করে, তাহলে এগুলো **ILF**।

### Shortcut:

> **System owns & maintains the data → ILF**

---

# 7. External Interface File (EIF)

### EIF = External Interface File

এটি এমন data/file যা **অন্য system maintain করে**, কিন্তু আমাদের software সেটি শুধু ব্যবহার/read করে।

### Example

ধরুন Banking System অন্য একটি system থেকে:

```text
National ID Information
```

ব্যবহার করছে।

NID system-এর data আমাদের Banking System maintain করছে না।

তাই এটি **EIF**।

### ILF বনাম EIF

| ILF                                 | EIF                           |
| ----------------------------------- | ----------------------------- |
| আমাদের system data maintain করে     | অন্য system data maintain করে |
| আমাদের application-এর internal data | External system-এর data       |
| Create/update/delete করতে পারে      | সাধারণত read/use করে          |

### Shortcut:

> **We maintain → ILF**
> **Others maintain → EIF**

---

# 8. FPA-তে Complexity

প্রতিটি function-এর complexity সাধারণত তিন ধরনের:

### 1. Low

কম complexity

### 2. Average

মাঝারি complexity

### 3. High

বেশি complexity

প্রতিটি function type-এর জন্য আলাদা **weight** থাকে।

---

# 9. Standard Function Point Weight

এগুলো অবশ্যই মনে রাখার মতো।

| Function Type | Low | Average | High |
| ------------- | --: | ------: | ---: |
| **EI**        |   3 |       4 |    6 |
| **EO**        |   4 |       5 |    7 |
| **EQ**        |   3 |       4 |    6 |
| **ILF**       |   7 |      10 |   15 |
| **EIF**       |   5 |       7 |   10 |

এগুলো দিয়ে প্রথমে **Unadjusted Function Point (UFP)** বের করা হয়।

---

# 10. UFP কী?

### UFP = Unadjusted Function Point

প্রথমে প্রতিটি function-এর:

```text
Number × Weight
```

করতে হবে।

তারপর সব যোগ করতে হবে।

### Formula:

$$
UFP = \sum (Number\ of\ Functions \times Weight)
$$

---

# 11. একটি Example

ধরুন একটি software-এ আছে:

| Function | Number | Complexity |
| -------- | -----: | ---------- |
| EI       |     10 | Average    |
| EO       |      5 | Average    |
| EQ       |      8 | Low        |
| ILF      |      4 | Average    |
| EIF      |      2 | Low        |

এখন calculation করি।

### EI

Average EI weight = 4

$$
10 \times 4 = 40
$$

### EO

Average EO weight = 5

$$
5 \times 5 = 25
$$

### EQ

Low EQ weight = 3

$$
8 \times 3 = 24
$$

### ILF

Average ILF weight = 10

$$
4 \times 10 = 40
$$

### EIF

Low EIF weight = 5

$$
2 \times 5 = 10
$$

তাহলে:

$$
UFP = 40+25+24+40+10
$$

$$
\boxed{UFP=139}
$$

---

# 12. Value Adjustment Factor (VAF)

শুধু UFP দিয়ে traditional FPA শেষ হয় না।

Software-এর বিভিন্ন **General System Characteristics (GSC)** বিবেচনা করে **Value Adjustment Factor (VAF)** বের করা হয়।

এখানে মোট **14টি General System Characteristic** থাকে।

যেমন:

* Data Communications
* Distributed Data Processing
* Performance
* Heavily Used Configuration
* Transaction Rate
* Online Data Entry
* End-User Efficiency
* Online Update
* Complex Processing
* Reusability
* Installation Ease
* Operational Ease
* Multiple Sites
* Facilitate Change

প্রতিটির rating সাধারণত:

$$
0 \text{ to } 5
$$

---

# 13. TDI

প্রতিটি GSC-এর rating যোগ করলে পাওয়া যায়:

### TDI = Total Degree of Influence

যেহেতু 14টি characteristic এবং প্রতিটির maximum rating 5:

$$
Maximum\ TDI = 14 \times 5 = 70
$$

অর্থাৎ:

$$
0 \leq TDI \leq 70
$$

---

# 14. VAF Formula

Traditional IFPUG-style FPA-তে:

$$
VAF = 0.65 + (0.01 \times TDI)
$$

যেহেতু TDI 0 থেকে 70:

### Minimum VAF:

$$
0.65+(0.01\times0)=0.65
$$

### Maximum VAF:

$$
0.65+(0.01\times70)=1.35
$$

তাই:

$$
\boxed{0.65 \leq VAF \leq 1.35}
$$

---

# 15. Final Function Point

শেষে:

$$
\boxed{FP = UFP \times VAF}
$$

ধরুন:

$$
UFP=139
$$

এবং

$$
TDI=40
$$

তাহলে:

$$
VAF=0.65+(0.01\times40)
$$

$$
=0.65+0.40
$$

$$
=1.05
$$

তাহলে:

$$
FP=139\times1.05
$$

$$
\boxed{FP=145.95}
$$

অর্থাৎ প্রায়:

$$
\boxed{146\ Function\ Points}
$$

---

# 16. পুরো FPA Formula একসাথে

Exam-এর জন্য এই flow-টা মনে রাখুন:

```text
Identify Functions
       ↓
EI, EO, EQ, ILF, EIF
       ↓
Determine Complexity
       ↓
Apply Weight
       ↓
Calculate UFP
       ↓
Rate 14 GSCs
       ↓
Calculate TDI
       ↓
VAF = 0.65 + 0.01 × TDI
       ↓
FP = UFP × VAF
```

---

# 17. FPA কেন ব্যবহার করা হয়?

### LOC-এর সমস্যা

LOC (Lines of Code) দিয়ে software size estimate করলে সমস্যা হতে পারে।

একজন developer:

```php
$result = $a + $b;
```

লিখতে পারে।

অন্যজন একই কাজ করতে 10 lines code লিখতে পারে।

Functionality একই, কিন্তু LOC আলাদা।

FPA এখানে functionality দেখে।

### তাই FPA:

* Programming language independent
* User functionality-এর উপর ভিত্তি করে
* Early-stage estimation-এ ব্যবহার করা যায়
* Effort/cost estimation-এ সাহায্য করে

---

# 18. FPA বনাম LOC

| FPA                                       | LOC                                   |
| ----------------------------------------- | ------------------------------------- |
| Functionality measure করে                 | Code-এর line measure করে              |
| Language independent                      | Programming language dependent        |
| User perspective বেশি গুরুত্বপূর্ণ        | Developer/code perspective            |
| Early estimation-এ useful                 | Code structure জানা থাকলে বেশি useful |
| Input/output/query/data-এর উপর ভিত্তি করে | Source code-এর উপর ভিত্তি করে         |

---

# 19. Exam-এর জন্য সবচেয়ে গুরুত্বপূর্ণ Short Notes

এগুলো মুখস্থ রাখলে MCQ + Written দুটোতেই কাজে দেবে:

### 5 Function Types

> **EI, EO, EQ, ILF, EIF**

### Weights

```text
       Low   Avg   High

EI      3     4     6
EO      4     5     7
EQ      3     4     6
ILF     7    10    15
EIF     5     7    10
```

### Important formulas

$$
\boxed{UFP=\sum(Number\times Weight)}
$$

$$
\boxed{VAF=0.65+0.01\times TDI}
$$

$$
\boxed{TDI=Sum\ of\ 14\ GSC\ ratings}
$$

$$
\boxed{FP=UFP\times VAF}
$$

### Maximum TDI

$$
\boxed{70}
$$

### VAF range

$$
\boxed{0.65\ to\ 1.35}
$$

---

## সবচেয়ে সহজে মনে রাখার কৌশল

**EI → Input**
**EO → Processed Output**
**EQ → Query**
**ILF → আমাদের Data**
**EIF → অন্যের Data**

আর পুরো calculation:

> **Functions → Weight → UFP → 14 GSC → TDI → VAF → FP**

এটাই **Function Point Analysis-এর core concept**।
