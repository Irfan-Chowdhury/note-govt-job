
<h1 align="center">TOPIC 03 - Data Structures</h1> <br>


## 1. Difference between Stack and Queue. Write about 2 problems solved by stack and queue.


### Stack এবং Queue এর মধ্যে মূল পার্থক্য

| Feature | Stack | Queue |
| --- | --- | --- |
| **Principle (মূল নীতি)** | **LIFO** (Last In, First Out) মেনে চলে। অর্থাৎ, যে Data সবার শেষে ইনপুট হবে, সেটি সবার আগে আউটপুট হবে। | **FIFO** (First In, First Out) মেনে চলে। অর্থাৎ, যে Data সবার প্রথমে ইনপুট হবে, সেটি সবার আগে আউটপুট হবে। |
| **Data Operation** | Data যুক্ত করাকে **Push** এবং বের করাকে **Pop** বলা হয়। | Data যুক্ত করাকে **Enqueue** এবং বের করাকে **Dequeue** বলা হয়। |
| **Access Points** | Push এবং Pop—দুটোই শুধুমাত্র একদিক থেকে করা হয়, যাকে **Top** বলে। | Enqueue একদিক থেকে (যাকে **Rear** বলে) এবং Dequeue অন্যদিক থেকে (যাকে **Front** বলে) করা হয়। |
| **Pointers** | Stack পরিচালনা করতে শুধুমাত্র ১টি Pointer (`Top`) প্রয়োজন হয়। | Queue পরিচালনা করতে ২টি Pointer (`Front` এবং `Rear`) প্রয়োজন হয়। |

---

### Stack দিয়ে সমাধান করা যায় এমন ২টি Problem

**১. Balanced Parenthesis (ব্র্যাকেট ম্যাচিং):**
প্রোগ্রামিং কোড বা গাণিতিক সমীকরণে ব্যবহৃত ব্র্যাকেটগুলো `()`, `{}`, `[]` সঠিক অর্ডারে open এবং close হয়েছে কি না, তা চেক করতে Stack ব্যবহৃত হয়। যখনই কোনো Open bracket পাওয়া যায়, সেটি Stack-এ `Push` করা হয়। আর Close bracket পেলে Stack-এর `Top` থেকে `Pop` করে চেক করা হয় ব্র্যাকেটটি ম্যাচ করছে কি না।

**২. Undo Mechanism এবং Browser History:**
Text editor-এ (যেমন: MS Word) আমরা যখন `Ctrl+Z` (Undo) চাপি, তখন সবশেষ করা কাজটি বাতিল হয়ে আগের অবস্থায় ফিরে যায়। একইভাবে ওয়েব ব্রাউজারের 'Back' বাটনে ক্লিক করলে সর্বশেষ পেজটি আসে। ব্যবহারকারীর প্রতিটি কাজ বা ভিজিট করা পেজ Stack-এ জমা হয়। Undo বা Back করলে Stack-এর `Top` থেকে Data `Pop` হয়ে আগের অবস্থায় নিয়ে যায়।

---

### Queue দিয়ে সমাধান করা যায় এমন ২টি Problem

**১. CPU Task Scheduling:**
Operating System (OS) যখন একাধিক প্রসেস একসাথে রান করে, তখন কোন প্রসেস আগে CPU-এর সময় (Execution time) পাবে তা Queue দিয়ে নির্ধারণ করা হয়। FCFS (First-Come, First-Served) শিডিউলিং অ্যালগরিদমে যেই প্রসেসটি আগে Queue-তে প্রবেশ করে (Enqueue), সেটি আগেই CPU দ্বারা প্রসেস হয় (Dequeue)।

**২. Graph Traversal (Breadth-First Search - BFS):**
গ্রাফ (Graph) বা ট্রি (Tree) ডেটা স্ট্রাকচারে লেভেল অনুযায়ী (Level by level) নোডগুলো ভিজিট করার জন্য BFS অ্যালগরিদম ব্যবহার করা হয়। একটি নোড ভিজিট করার পর তার পাশের (Adjacent) নোডগুলোকে Queue-তে রাখা হয়। এর ফলে যে নোডগুলো আগে Discover হয়েছে, সেগুলো লজিক্যালি আগেই প্রসেস করা সম্ভব হয়।

### 🎯 মনে রাখুন

**Stack → LIFO → Push/Pop** <br>
**Queue → FIFO → Enqueue/Dequeue**


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


## 2. What is Hash function? Describe it.

**Hash Function** হলো এমন একটি function যা একটি input/key-কে একটি নির্দিষ্ট **hash value বা index**-এ রূপান্তর করে।

এটি মূলত **Hash Table**-এ data দ্রুত **search, insert এবং delete** করার জন্য ব্যবহৃত হয়।

**মূল বৈশিষ্ট্য (Key Features):** <br>
১. **One-way (একমুখী):** Hash value থেকে কোনোভাবেই অরিজিনাল ইনপুট ডেটা রিকভার (Reverse) করা যায় না। <br>
২. **Deterministic:** একই ডেটা ইনপুট দিলে সবসময় হুবহু একই Hash value তৈরি হবে। <br>
৩. **Fixed-length Output:** ইনপুটের সাইজ ১ কিলোবাইট বা ১ গিগাবাইট যাই হোক না কেন, আউটপুট সাইজ সবসময় নির্দিষ্ট (যেমন: ২৫৬ বিট) থাকবে।


### Example -1:

ধরি,

```text
Hash Function: h(key) = key % 10
```

তাহলে:

```text
key = 25
h(25) = 25 % 10 = 5
```

অর্থাৎ `25` key-টি **index 5**-এ রাখা হবে।

### Collision

যদি দুইটি key একই index দেয়, তাকে **Collision** বলে।

```text
25 % 10 = 5
35 % 10 = 5
```

এখানে 25 এবং 35 একই index `5` তৈরি করেছে → **Collision**।

### Example -2:
ধরা যাক, একটি ওয়েবসাইটের ইউজারের পাসওয়ার্ড `"admin123"`।
ডেটাবেসে এটি সরাসরি সেভ না করে একটি Hash Function (যেমন: SHA-256) এর মাধ্যমে রূপান্তর করে সেভ করা হয়:

* **Input:** `admin123`
* **Hash Value:** `240be518fabd2724ddb6f04eeb1da596...`

পরবর্তীতে ইউজার লগইন করার সময় ইনপুট দেওয়া পাসওয়ার্ডের Hash মিলিয়ে দেখা হয়। হ্যাকার ডেটাবেস হ্যাক করে এই Hash পেলেও মূল পাসওয়ার্ডটি জানতে পারবে না।


### 🎯 Government Job Exam Focus

> **A hash function maps a key to a fixed-size value or index, which is used to store and retrieve data efficiently in a hash table.**

**Key points:**
`Hash Function → Key → Hash Value/Index → Fast Search/Insertion/Deletion`


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>

## 3. Linked list, doubly linked list and circular linked list explains with diagram.

**লিংকড লিস্ট কী?** এটি একটি **linear data structure**, যেখানে উপাদানগুলো (node) মেমোরিতে পাশাপাশি থাকে না। প্রতিটি node পরের node-এর ঠিকানা (pointer) ধরে রাখে।

---

## ১. সিঙ্গলি লিংকড লিস্ট (Singly Linked List)

**সংজ্ঞা:** প্রতিটি node-এ দুটি অংশ থাকে: **data** (তথ্য) এবং **next** (পরের node-এর ঠিকানা)। শুধু সামনের দিকে যাওয়া যায়।

```
HEAD
 ↓
[10 | •]──►[20 | •]──►[30 | •]──►[40 | NULL]
```

```c
struct Node {
    int data;
    struct Node *next;
};
```

**বৈশিষ্ট্য:**
- শুধু **একদিকে** (forward) traverse করা যায়
- শেষ node-এর next = `NULL`
- মেমোরি কম লাগে (একটি pointer)

**উদাহরণ:** গানের playlist-এ একটি গান থেকে পরের গানে যাওয়া।

---

## ২. ডাবলি লিংকড লিস্ট (Doubly Linked List)

**সংজ্ঞা:** প্রতিটি node-এ **তিনটি অংশ** থাকে: `prev` (আগের node), `data` এবং `next` (পরের node)। তাই **দুই দিকেই** যাওয়া যায়।

```
NULL ◄──[• | 10 | •]◄──►[• | 20 | •]◄──►[• | 30 | •]──► NULL
         prev data next
```

```c
struct Node {
    int data;
    struct Node *prev;
    struct Node *next;
};
```

**বৈশিষ্ট্য:**
- **সামনে ও পেছনে** দুই দিকেই traversal সম্ভব
- Deletion সহজ, কারণ আগের node খুঁজতে হয় না
- বেশি মেমোরি লাগে (দুটি pointer)

**উদাহরণ:** ব্রাউজারের Back/Forward বাটন, ফটো ভিউয়ারে আগের/পরের ছবি।

---

## ৩. সার্কুলার লিংকড লিস্ট (Circular Linked List)

**সংজ্ঞা:** এখানে **শেষ node-এর next পয়েন্টার `NULL` না হয়ে প্রথম node-কে point করে**, ফলে একটি বৃত্ত তৈরি হয়।

```
      ┌──────────────────────────────┐
      ▼                              │
[10 | •]──►[20 | •]──►[30 | •]──►[40 | •]
```

**ধরন:** Singly Circular এবং Doubly Circular।

**বৈশিষ্ট্য:**
- কোনো node-এ `NULL` থাকে না
- যেকোনো node থেকে শুরু করে সব node-এ পৌঁছানো যায়
- Traversal-এ সতর্ক না হলে **infinite loop** হতে পারে

**উদাহরণ:** CPU-এর **Round Robin scheduling**, মাল্টিপ্লেয়ার গেমে পালাক্রমে খেলা।

---

## তুলনামূলক ছক

| বিষয় | Singly | Doubly | Circular |
|---|---|---|---|
| প্রতি node-এ pointer | ১টি (next) | ২টি (prev, next) | ১টি বা ২টি |
| Traversal | শুধু সামনে | দুই দিকে | ঘুরতে থাকে |
| শেষ node কোথায় point করে | NULL | NULL | প্রথম node |
| মেমোরি | কম | বেশি | কম/বেশি |
| Deletion | মাঝারি | সহজ | মাঝারি |

---

## পরীক্ষার টিপস ✍️

- **সুবিধা (Advantage):** আকার গতিশীল (dynamic size), Insertion/Deletion সহজ (শুরুতে O(1))
- **অসুবিধা (Disadvantage):** Random access নেই (array-র মতো `a[i]` করা যায় না), pointer-এর জন্য বাড়তি মেমোরি লাগে
- **Time Complexity:** Search = **O(n)**, Head-এ Insert = **O(1)**
- ডায়াগ্রামে অবশ্যই **তীরচিহ্ন (arrow)** ও **NULL** দেখাবে

চাইলে Insertion ও Deletion-এর C কোডও বাংলা ব্যাখ্যাসহ দিতে পারি।

<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


# 4. You have two stacks. Explain the logic required to implement a Queue (FIFO) using only these two stacks.

### দুইটি Stack দিয়ে Queue (FIFO) Implement করা

### মূল ধারণা (Core Idea)
---

**Stack = LIFO** (শেষে যা ঢোকে, আগে তা বের হয়), আর **Queue = FIFO** (আগে যা ঢোকে, আগে তা বের হয়)।

দুইটি stack-এ elements **একবার উল্টালে** LIFO-র order **উল্টে গিয়ে** FIFO হয়ে যায়। এটাই পুরো logic-এর মূল কথা।

- **Stack1 (`s1`)** → শুধু **Enqueue (input)**-এর জন্য
- **Stack2 (`s2`)** → শুধু **Dequeue (output)**-এর জন্য

---

## Diagram

```
 Enqueue(x)                          Dequeue()
     │                                   ▲
     ▼                                   │
 ┌────────┐   transfer (pop→push)   ┌────────┐
 │  s1    │ ──────────────────────► │  s2    │
 │ (input)│  শুধু যখন s2 খালি       │(output)│
 └────────┘                         └────────┘
```

---

## Algorithm

### Enqueue(x)
1. `x`-কে সরাসরি **s1-এ push** করো।
2. Time: **O(1)**

### Dequeue()
1. যদি **s2 খালি** হয়:
   - s1-এর **সব element pop** করে একে একে **s2-তে push** করো।
2. এখন **s2 থেকে pop** করো, এটাই Queue-র front element।
3. যদি s1 ও s2 দুটোই খালি হয় → **Underflow** (Queue empty)।

> ⚠️ **গুরুত্বপূর্ণ নিয়ম:** s2 তে element থাকলে **s1 থেকে transfer করা যাবে না**, নাহলে order নষ্ট হয়ে যাবে।

---

## Example (Step by Step)

**Enqueue(1), Enqueue(2), Enqueue(3):**

```
s1 (top→)   s2
  3
  2          (খালি)
  1
```

**Dequeue() → s2 খালি, তাই transfer:**

```
s1          s2
(খালি)       1   ← top
             2
             3
```

s2 থেকে pop করলে পাওয়া যায় **1** ✅ (প্রথমে ঢুকেছিল, প্রথমে বের হলো: FIFO)

**এরপর Enqueue(4):**

```
s1          s2
  4          2  ← top
             3
```

**Dequeue()** → s2 খালি না, তাই সরাসরি pop → **2** ✅

---

## C Pseudocode

```c
void enqueue(int x) {
    push(s1, x);
}

int dequeue() {
    if (isEmpty(s1) && isEmpty(s2)) {
        printf("Queue Underflow");
        return -1;
    }
    if (isEmpty(s2)) {
        while (!isEmpty(s1))
            push(s2, pop(s1));
    }
    return pop(s2);
}
```

---

## Time Complexity

| Operation | Worst Case | Amortized |
|---|---|---|
| Enqueue | O(1) | O(1) |
| Dequeue | O(n) | **O(1)** |

**Amortized O(1) কেন?** প্রতিটি element সর্বোচ্চ **একবার s1 → s2** এ যায়। তাই n টি operation-এ মোট কাজ O(n), গড়ে প্রতি operation O(1)।

---

## পরীক্ষার টিপস ✍️

- মূল পয়েন্ট লিখবে: **"দুইবার উল্টালে order সোজা হয়"** (s1-এ LIFO → s2-তে উল্টে FIFO)
- **s2 খালি হলেই কেবল transfer**, এই শর্তটা অবশ্যই লিখবে
- Diagram-এ s1 (input) ও s2 (output) আলাদা করে দেখাবে
- Alternative approach: **Enqueue costly** করা যায় (প্রতি enqueue-তে transfer), কিন্তু সেটা কম efficient


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


# 05. Consider a hash table of size 13 strong entities with integer keys. Suppose the hash
function is h(k) = k mod 13. Insert in the given order entries with keys 10, 3, 6, 16, 17, 19, 10, 3, 6,
16, 17, 19 into the hash table using linear probing to resolve collisions. Show all the work.