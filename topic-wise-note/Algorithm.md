
<h1 align="center">TOPIC 04 - Algorithms, Search, Sorting & Graphs</h1> <br>

## Question 01. Compare BFS & DFS with examples.


### মূল ধারণা

- **BFS (Breadth First Search):** আগে **level by level** যায়, মানে আগে সব neighbour visit করে, তারপর পরের level-এ যায়। **Queue (FIFO)** ব্যবহার করে।
- **DFS (Depth First Search):** একটা path ধরে **যতদূর সম্ভব গভীরে** যায়, শেষ হলে **backtrack** করে। **Stack (LIFO)** বা **recursion** ব্যবহার করে।

---

## Example Graph

```
          A          ← Level 0
         / \
        B   C        ← Level 1
       / \   \
      D   E   F      ← Level 2
```

### BFS Traversal (Queue দিয়ে)

```
Start: Queue = [A]

Visit A → Queue = [B, C]
Visit B → Queue = [C, D, E]
Visit C → Queue = [D, E, F]
Visit D, E, F → Queue = []
```

**BFS Output: A → B → C → D → E → F**

### DFS Traversal (Stack/Recursion দিয়ে)

```
A → B → D   (D-te deadend, backtrack to B)
      → E   (E-te deadend, backtrack to A)
  → C → F
```

**DFS Output: A → B → D → E → C → F**

---

## Algorithm (Short)

**BFS:**
```
1. Start node-ke queue-te rakho, visited mark koro
2. Jotokkhon queue khali na hoy:
     node = dequeue()
     node-er shob unvisited neighbour-ke visit kore enqueue koro
```

**DFS:**
```
DFS(node):
   visited[node] = true
   for each neighbour of node:
       if not visited → DFS(neighbour)
```

---

## তুলনামূলক ছক (Comparison Table)

| বিষয় | BFS | DFS |
|---|---|---|
| Full form      | Breadth-First Search             | Depth-First Search    |
| Data Structure | **Queue** (FIFO) | **Stack** / Recursion (LIFO) |
| Traversal ধরন | Level by level (প্রস্থ) | Depth-first (গভীরতা) |
| Time Complexity | **O(V + E)** | **O(V + E)** |
| শুরু           | কাছের node আগে                   | গভীরে যায় আগে         |
| Space Complexity | O(V), widest level-এর size | O(V), longest path-এর depth |
| Shortest Path | **পাওয়া যায়** (unweighted graph) | নিশ্চিত না |
| Implementation | Iterative | Recursive (সহজ) বা Iterative |
| Memory | Wide graph-এ বেশি লাগে | Deep graph-এ stack overflow হতে পারে |
| Completeness | সবসময় solution পায় | Infinite path-এ আটকে যেতে পারে |


---

## Applications

**BFS:**
- Unweighted graph-এ **shortest path**
- Social network-এ "friends of friends" খোঁজা
- GPS/Network broadcasting, Web crawler

**DFS:**
- **Cycle detection**
- **Topological sorting**
- Maze solving, Backtracking (N-Queens, Sudoku)
- Connected components খোঁজা

---

## কখন কোনটা?

- Target **কাছাকাছি** থাকলে বা shortest path লাগলে → **BFS**
- Target **অনেক গভীরে** থাকতে পারে বা সব path explore করতে হলে → **DFS**

---

## পরীক্ষার টিপস ✍️

- Graph diagram আঁকবে এবং **দুটোর output order আলাদা করে** দেখাবে (A B C D E F বনাম A B D E C F)
- মূল পার্থক্য এক লাইনে লিখবে: **"BFS uses Queue, DFS uses Stack"**
- দুটোরই complexity **O(V+E)** (Adjacency List-এ), Adjacency Matrix-এ হবে **O(V²)**
- **Visited array** ব্যবহারের কথা অবশ্যই লিখবে, নাহলে cycle-এ infinite loop হয়
- BFS → Queue → Level-wise <br> DFS → Stack → Depth-wise




<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


##  Question 02. Describe step-by-step how Binary Search locates a target value in a sorted array. Why does it fail if the array is unsorted?

### মূল ধারণা

**Binary Search** হলো একটি **divide and conquer** algorithm। Sorted array-র **মাঝের element** এর সাথে target compare করে প্রতিবার **search space অর্ধেক** করে ফেলা হয়।

> ⚠️ **Precondition:** Array অবশ্যই **sorted** হতে হবে।

---

## Step-by-Step Algorithm

1. দুটি pointer নাও: `low = 0`, `high = n - 1`
2. Jotokkhon `low <= high`:
   - `mid = low + (high - low) / 2` বের করো
   - যদি `arr[mid] == target` → **পাওয়া গেছে**, `mid` return করো ✅
   - যদি `arr[mid] < target` → target **ডান দিকে** আছে, তাই `low = mid + 1`
   - যদি `arr[mid] > target` → target **বাম দিকে** আছে, তাই `high = mid - 1`
3. Loop শেষ হলে (`low > high`) → target **নেই**, `-1` return করো ❌

---

## Example

**Array:** `[5, 12, 18, 25, 31, 40, 52]` (index 0 থেকে 6), **Target = 40**

```
Index:   0   1   2   3   4   5   6
Value:   5  12  18  25  31  40  52
```

| Step | low | high | mid | arr[mid] | Compare | Action |
|---|---|---|---|---|---|---|
| 1 | 0 | 6 | 3 | 25 | 25 < 40 | `low = 4` |
| 2 | 4 | 6 | 5 | 40 | 40 == 40 | **Found at index 5** ✅ |

মাত্র **২ ধাপে** পাওয়া গেল। Linear search-এ লাগত ৬ ধাপ।

```
Step 1: [5  12  18 |25| 31  40  52]  → বাম অংশ বাদ
Step 2:             [31 |40| 52]     → পাওয়া গেছে
```

---

## C Code

```c
int binarySearch(int arr[], int n, int target) {
    int low = 0, high = n - 1;
    while (low <= high) {
        int mid = low + (high - low) / 2;
        if (arr[mid] == target) return mid;
        else if (arr[mid] < target) low = mid + 1;
        else high = mid - 1;
    }
    return -1;
}
```

---

## Unsorted Array-তে কেন Fail করে?

Binary Search-এর পুরো logic এই **assumption**-এর উপর দাঁড়িয়ে: *"`arr[mid] < target` হলে target-এর জায়গা mid-এর ডানেই হবে।"* এটা শুধু **sorted** array-তেই সত্য। Unsorted হলে এই অনুমান ভুল হয় এবং algorithm ভুল দিকে চলে যায়, ফলে **আসল element থাকা সত্ত্বেও "not found"** দেয়।

**Example:** Array = `[40, 10, 50, 20, 30]`, Target = **20** (index 3-এ আছে)

| Step | low | high | mid | arr[mid] | Decision |
|---|---|---|---|---|---|
| 1 | 0 | 4 | 2 | 50 | 50 > 20, তাই `high = 1` (বাম দিকে যাও) |
| 2 | 0 | 1 | 0 | 40 | 40 > 20, তাই `high = -1` |
| 3 | low > high | | | | **Not found ❌** |

20 আসলে **ডান দিকে** ছিল, কিন্তু algorithm বাম অংশ বেছে নিয়ে ডান অংশ **চিরতরে বাদ** দিয়ে দিল। কারণ unsorted array-তে `50 > 20` মানেই এই না যে 20 বাম দিকে আছে।

---

## Complexity

| | Binary Search | Linear Search |
|---|---|---|
| Time (Best) | O(1) | O(1) |
| Time (Worst/Avg) | **O(log n)** | O(n) |
| Space | O(1) (iterative) | O(1) |
| Sorted লাগে? | **হ্যাঁ** | না |

**Note:** Unsorted array-তে binary search চালানোর জন্য আগে sort করলে O(n log n) লাগে, তাই **একবারই search** করলে linear search-ই ভালো।

---

## পরীক্ষার টিপস ✍️

- Trace table (low, high, mid) অবশ্যই আঁকবে
- Failure-এর কারণ এক লাইনে লিখবে: **"Sorted order না থাকলে mid-এর তুলনা থেকে কোন দিক বাদ দেওয়া যাবে তা নিশ্চিত হওয়া যায় না"**
- `mid = (low + high)/2` এর বদলে `low + (high - low)/2` লিখলে **integer overflow** এড়ানো যায়, এটা mention করলে extra নম্বর পাওয়া যায়
- Recurrence: **T(n) = T(n/2) + O(1)** → **O(log n)**



<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


## Question 03. Explain the logic of "Bubble Sort". Why is it considered inefficient for large datasets compared to Merge Sort?

# Bubble Sort (Exam Short Note)

## মূল ধারণা

**Bubble Sort** হলো একটি simple **comparison-based** sorting algorithm। এটি পাশাপাশি **adjacent দুটি element compare** করে, ভুল order-এ থাকলে **swap** করে। প্রতিটি pass-এ সবচেয়ে বড় element পানির বুদবুদের মতো **ভেসে ডান দিকে (শেষে)** চলে যায়, তাই নাম "Bubble"।

---

## Step-by-Step Logic

1. Array-র শুরু থেকে শেষ পর্যন্ত **adjacent pair** compare করো।
2. যদি `arr[j] > arr[j+1]` হয় → দুটি **swap** করো।
3. এক pass শেষে **সবচেয়ে বড় element তার সঠিক জায়গায়** বসে যায়।
4. পরের pass-এ শেষের sorted অংশ বাদ দিয়ে আবার চালাও (n-1 টা pass লাগে)।
5. যদি কোনো pass-এ **একটাও swap না হয়** → array sorted, থেমে যাও (**optimized version**)।

---

## Example

**Array:** `[5, 1, 4, 2, 8]`

```
Pass 1:
[5 1 4 2 8] → 5>1 swap → [1 5 4 2 8]
[1 5 4 2 8] → 5>4 swap → [1 4 5 2 8]
[1 4 5 2 8] → 5>2 swap → [1 4 2 5 8]
[1 4 2 5 8] → 5<8 no   → [1 4 2 5 |8|]   ← 8 fixed

Pass 2:
[1 4 2 5] → 1<4 no
          → 4>2 swap → [1 2 4 5]
          → 4<5 no   → [1 2 4 |5 8|]

Pass 3:
কোনো swap হয়নি → Sorted ✅  [1 2 4 5 8]
```

---

## C Code

```c
void bubbleSort(int arr[], int n) {
    for (int i = 0; i < n - 1; i++) {
        int swapped = 0;
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
                swapped = 1;
            }
        }
        if (!swapped) break;   // already sorted
    }
}
```

---

## Complexity

| Case | Time |
|---|---|
| Best (already sorted, optimized) | **O(n)** |
| Average | **O(n²)** |
| Worst (reverse sorted) | **O(n²)** |
| Space | **O(1)** (in-place) |

মোট comparison হয় প্রায় **n(n-1)/2**, যা n-এর square-এর সমানুপাতিক।

---

## Merge Sort-এর তুলনায় কেন Inefficient?

**মূল কারণ:** Bubble Sort প্রতিবার শুধু **পাশের element**-এর সাথে compare করে, তাই একটা element-কে তার সঠিক জায়গায় পৌঁছাতে **এক ঘর করে** সরতে হয়। অনেক দূরে থাকা element-এর জন্য অনেক বেশি swap লাগে। অন্যদিকে Merge Sort **divide and conquer** ব্যবহার করে array-কে বারবার অর্ধেক করে, তারপর **merge** করে, ফলে কাজ অনেক কম লাগে।

**Number দিয়ে তুলনা (n = 1,000,000):**

| | Bubble Sort | Merge Sort |
|---|---|---|
| Complexity | O(n²) | O(n log n) |
| মোটামুটি operation | ~10¹² (এক ট্রিলিয়ন) | ~2 × 10⁷ (দুই কোটি) |

Merge Sort প্রায় **৫০,০০০ গুণ দ্রুত**।

| বিষয় | Bubble Sort | Merge Sort |
|---|---|---|
| Time (Worst) | O(n²) | **O(n log n)** |
| Time (Best) | O(n) | O(n log n) |
| Space | **O(1)** | O(n) (extra array লাগে) |
| Stable? | হ্যাঁ | হ্যাঁ |
| Large data-তে | অচল | উপযুক্ত |
| Swap সংখ্যা | অনেক বেশি | কম |

**Trade-off:** Bubble Sort-এ extra memory লাগে না (O(1)), কিন্তু সময় অনেক বেশি। Merge Sort-এ O(n) বাড়তি memory লাগে, কিন্তু অনেক দ্রুত।

---

## পরীক্ষার টিপস ✍️

- Pass-by-pass **trace diagram** অবশ্যই আঁকবে
- **Swapped flag** optimization-এর কথা লিখবে, এতে best case O(n) হয়
- Inefficiency-র মূল কারণ এক লাইনে: **"Bubble Sort adjacent swap করে, তাই element এক ঘর করে সরে; আর Merge Sort array ভাগ করে log n level-এ কাজ শেষ করে"**
- Merge Sort-এর recurrence: **T(n) = 2T(n/2) + O(n)** → **O(n log n)**
- Bubble Sort ছোট বা প্রায় sorted data-তে, বা শেখার জন্য ব্যবহার করা যায়, কিন্তু real-world large dataset-এ নয়


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


# Question 04. Explain the time complexity of merge sort. Best, Average, Worst.


## মূল ধারণা

Merge Sort হলো **divide and conquer** algorithm। তিনটি ধাপ:

1. **Divide:** Array-কে মাঝখান থেকে দুই ভাগে ভাগ করো
2. **Conquer:** দুই ভাগকে recursively sort করো
3. **Merge:** দুটি sorted অংশকে merge করে একটি sorted array বানাও

---

## Recurrence Relation

```
T(n) = 2T(n/2) + O(n)
        ↑          ↑
   দুই অর্ধেক sort   merge করতে n কাজ
```

**Recursion Tree:**

```
Level 0:              [n]                  → কাজ = n
                     /     \
Level 1:        [n/2]       [n/2]          → কাজ = n/2 + n/2 = n
                /   \       /   \
Level 2:    [n/4] [n/4] [n/4] [n/4]        → কাজ = n
                 ...
Level k:    [1] [1] [1] ......... [1]      → কাজ = n
```

- মোট **level** = **log₂n** (প্রতিবার অর্ধেক হয়)
- প্রতি level-এ merge-এর কাজ = **n**
- মোট কাজ = n × log n = **O(n log n)**

---

## Best, Average, Worst Case

| Case | Time Complexity | কারণ |
|---|---|---|
| **Best** | **O(n log n)** | Array আগে থেকে sorted হলেও divide ও merge সব ধাপ করতে হয় |
| **Average** | **O(n log n)** | Random data-তেও একই structure |
| **Worst** | **O(n log n)** | Reverse sorted হলেও level সংখ্যা log n-ই থাকে |

**মূল কথা:** Merge Sort-এর complexity **input-এর order-এর উপর নির্ভর করে না**। Array-র split সবসময় ঠিক মাঝখানে হয়, তাই তিন case-এই **O(n log n)**।

(Best case-এ শুধু comparison একটু কম লাগে, কিন্তু asymptotic complexity একই থাকে।)

---

## Example

**Array:** `[38, 27, 43, 3]` (n = 4, তাই log₂4 = 2 level)

```
          [38 27 43 3]
          /          \
     [38 27]        [43 3]       ← Divide
      /   \          /   \
   [38]  [27]     [43]   [3]

   [27 38]        [3 43]         ← Merge (Level 2: 4 কাজ)
          \        /
        [3 27 38 43]             ← Merge (Level 1: 4 কাজ)
```

মোট কাজ ≈ n × log n = 4 × 2 = **8 operation**

---

## Space Complexity

| | Merge Sort |
|---|---|
| Space | **O(n)** (merge-এর জন্য extra array লাগে) |
| Stable? | হ্যাঁ |
| In-place? | না |

---

## Master Theorem দিয়ে প্রমাণ

`T(n) = aT(n/b) + f(n)`-এ **a = 2, b = 2, f(n) = n**

- n^(log_b a) = n^(log₂2) = **n¹ = n**
- f(n) = n এর সমান, তাই **Case 2** প্রযোজ্য
- ফলাফল: **T(n) = Θ(n log n)**

---

## পরীক্ষার টিপস ✍️

- **Recursion tree** আঁকবে এবং লিখবে: "**log n level × প্রতি level-এ n কাজ = n log n**"
- তিন case-এই **O(n log n)** লিখবে, এবং কারণ দেবে: "**Input order-এর উপর নির্ভর করে না**"
- Recurrence **T(n) = 2T(n/2) + O(n)** অবশ্যই লিখবে
- Quick Sort-এর সাথে পার্থক্য: Quick Sort-এর worst case **O(n²)**, কিন্তু Merge Sort-এর worst case **O(n log n)**
- Disadvantage mention করবে: **O(n) extra space** লাগে


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


## 05. Problem solved more efficiently in adjacency list representation then adjacency matrix representation and problem solved more effective in adjacency matrix adjacency list.

### Adjacency List vs Adjacency Matrix: কোন Problem-এ কোনটা ভালো?

### Example Graph

```
    0 ─── 1
    │     │
    │     │
    3 ─── 2        (V = 4, E = 4)
```

**Adjacency Matrix** (V × V 2D array):

```
     0  1  2  3
 0 [ 0  1  0  1 ]
 1 [ 1  0  1  0 ]
 2 [ 0  1  0  1 ]
 3 [ 1  0  1  0 ]
```

**Adjacency List** (প্রতি vertex-এর neighbour-এর list):

```
0 → [1, 3]
1 → [0, 2]
2 → [1, 3]
3 → [0, 2]
```

---

## ১. Adjacency List-এ Problem বেশি Efficiently Solve হয়

### (a) Space কম লাগে (Sparse Graph)

- List: **O(V + E)**, শুধু যে edge আছে সেগুলোই store হয়
- Matrix: **O(V²)**, edge না থাকলেও জায়গা নষ্ট হয়

**Example:** V = 1000, E = 2000 হলে Matrix-এ 10,00,000 ঘর লাগে, কিন্তু List-এ লাগে মাত্র ~3000।

### (b) BFS / DFS Traversal

- List: **O(V + E)**, প্রতি vertex-এর শুধু আসল neighbour গুলোতে যাওয়া হয়
- Matrix: **O(V²)**, প্রতি vertex-এর জন্য পুরো row (V ঘর) scan করতে হয়

### (c) একটি vertex-এর সব Neighbour বের করা

- List: **O(degree)**, সরাসরি list পড়ো
- Matrix: **O(V)**, পুরো row দেখতে হয়

### (d) নতুন Vertex যোগ করা

- List: সহজ, নতুন list বানালেই হয়
- Matrix: পুরো matrix resize করতে হয়, **O(V²)**

### (e) Shortest path / MST (Dijkstra, Prim, Kruskal) sparse graph-এ

Priority queue-র সাথে list ব্যবহার করলে **O((V+E) log V)**, যা matrix-এর O(V²)-এর চেয়ে sparse graph-এ ভালো।

---

## ২. Adjacency Matrix-এ Problem বেশি Efficiently Solve হয়

### (a) Edge আছে কিনা Check করা

- Matrix: **O(1)**, শুধু `matrix[u][v]` দেখো
- List: **O(degree)**, u-এর list-এ v খুঁজতে হয়

**Example:** "2 আর 3-এর মধ্যে edge আছে?" → `matrix[2][3] == 1` → হ্যাঁ।

### (b) Edge Add / Remove করা

- Matrix: **O(1)** (`matrix[u][v] = 1` বা `0`)
- List: **O(degree)**, remove করতে খুঁজে বের করতে হয়

### (c) Dense Graph

E ≈ V² হলে List-এর বাড়তি pointer overhead-এর কারণে Matrix-ই কম বা সমান জায়গা নেয় এবং সহজ।

### (d) Floyd-Warshall (All-pairs shortest path)

পুরো V × V distance table-ই লাগে, তাই matrix স্বাভাবিক এবং সহজ। **O(V³)**।

### (e) Matrix-based operation

Graph-এর **matrix multiplication** (path counting, transitive closure) করা যায়। Implementation সহজ।

---

## তুলনামূলক ছক

| বিষয় | Adjacency List | Adjacency Matrix |
|---|---|---|
| Space | **O(V + E)** ✅ | O(V²) |
| Edge আছে কিনা check | O(degree) | **O(1)** ✅ |
| Add edge | O(1) | **O(1)** |
| Remove edge | O(degree) | **O(1)** ✅ |
| সব neighbour বের করা | **O(degree)** ✅ | O(V) |
| BFS / DFS | **O(V + E)** ✅ | O(V²) |
| Add vertex | **সহজ** ✅ | কঠিন, O(V²) |
| Best for | **Sparse graph** | **Dense graph** |
| Implementation | একটু জটিল | **সহজ** ✅ |

---

## কখন কোনটা?

```
E << V²  (Sparse)  →  Adjacency LIST
E ≈ V²   (Dense)   →  Adjacency MATRIX
বারবার "edge আছে?" check লাগলে  →  MATRIX
Traversal / memory গুরুত্বপূর্ণ  →  LIST
```

**Real-life Example:** Facebook-এ কোটি user, কিন্তু প্রত্যেকের বন্ধু অল্প, তাই **List** লাগে (Matrix-এ কয়েক হাজার TB লাগত)।

---

## পরীক্ষার টিপস ✍️

- মূল পার্থক্য এক লাইনে লিখবে: **"List space-efficient ও traversal-এ দ্রুত; Matrix edge lookup-এ O(1)"**
- **Sparse → List, Dense → Matrix**, এটা অবশ্যই লিখবে
- ছোট একটি graph এঁকে **দুই representation পাশাপাশি** দেখাবে
- Undirected graph-এ matrix **symmetric** হয় (`matrix[i][j] == matrix[j][i]`), এটা mention করলে extra নম্বর
- Weighted graph-এ matrix-এ `1`-এর জায়গায় **weight** বসে, list-এ `(neighbour, weight)` pair থাকে

<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


## 06. Given an adjacency list representation for a complete binary tree on 7 vertices, give the equivalent adjacency matrix representation. Assume that vertices are numbered from 1 to 7 as in a binary heap.

### Complete Binary Tree (7 Vertices): Adjacency List থেকে Adjacency Matrix

### Tree Diagram (Heap Numbering)

```
            1
          /   \
         2     3
        / \   / \
       4   5 6   7
```

**Heap নিয়ম:** vertex `i`-এর
- Left child = **2i**
- Right child = **2i + 1**
- Parent = **⌊i/2⌋**

তাই edge গুলো: **1-2, 1-3, 2-4, 2-5, 3-6, 3-7** (মোট E = 6, কারণ tree-তে E = V - 1)

---

## Adjacency List (Given Representation)

```
1 → [2, 3]
2 → [1, 4, 5]
3 → [1, 6, 7]
4 → [2]
5 → [2]
6 → [3]
7 → [3]
```

(Undirected tree ধরা হয়েছে, তাই প্রতিটি edge দুই দিকেই আছে।)

---

## Equivalent Adjacency Matrix (7 × 7)

নিয়ম: vertex `i`-এর list-এ `j` থাকলে `M[i][j] = 1`, নাহলে `0`।

```
      1  2  3  4  5  6  7
 1  [ 0  1  1  0  0  0  0 ]
 2  [ 1  0  0  1  1  0  0 ]
 3  [ 1  0  0  0  0  1  1 ]
 4  [ 0  1  0  0  0  0  0 ]
 5  [ 0  1  0  0  0  0  0 ]
 6  [ 0  0  1  0  0  0  0 ]
 7  [ 0  0  1  0  0  0  0 ]
```

---

## Verification

| Row | List-এর neighbour | Matrix-এ `1` কোথায় |
|---|---|---|
| 1 | 2, 3 | column 2, 3 ✅ |
| 2 | 1, 4, 5 | column 1, 4, 5 ✅ |
| 3 | 1, 6, 7 | column 1, 6, 7 ✅ |
| 4 | 2 | column 2 ✅ |
| 5 | 2 | column 2 ✅ |
| 6 | 3 | column 3 ✅ |
| 7 | 3 | column 3 ✅ |

---

## লক্ষণীয় বিষয়

- Matrix **symmetric**: `M[i][j] = M[j][i]` (undirected graph)
- **Diagonal সব 0**: কোনো self-loop নেই
- মোট `1`-এর সংখ্যা = **2E = 12** (প্রতি edge দুইবার গোনা হয়)
- Matrix-এ 49 ঘরের মধ্যে মাত্র 12টি `1`, মানে এটি **sparse**, তাই এই graph-এ **List-ই বেশি space-efficient** (O(V+E) বনাম O(V²))

---

## পরীক্ষার টিপস ✍️

- আগে **edge list** বের করবে (heap নিয়মে `i → 2i, 2i+1`), তারপর matrix বানাবে
- **Row/column label (1 থেকে 7)** অবশ্যই দেবে
- Question-এ "directed" বলা না থাকলে **symmetric matrix** দেবে
- যদি **directed (parent → child)** ধরা হয়, তাহলে শুধু উপরের triangle-এ `1` থাকবে: row 1: `0 1 1 0 0 0 0`, row 2: `0 0 0 1 1 0 0`, row 3: `0 0 0 0 0 1 1`, বাকি row সব `0`
- Tree-তে **E = V - 1 = 6** লিখলে extra নম্বর


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


# 07. Solve Fibonacci series using dynamic programming.

অবশ্যই। **Fibonacci Series-কে Dynamic Programming (DP) দিয়ে কীভাবে solve করা হয়**, সেটা পরীক্ষার উপযোগী করে বাংলায় বুঝি।

## ১. Fibonacci Series কী?

Fibonacci series হলো:

**0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...**

এখানে প্রতিটি সংখ্যা তার আগের **দুইটি সংখ্যার যোগফল**।

অর্থাৎ,

$$
F(n)=F(n-1)+F(n-2)
$$

প্রাথমিক মান:

$$
F(0)=0
$$

$$
F(1)=1
$$

উদাহরণ:

$$
F(2)=F(1)+F(0)=1+0=1
$$

$$
F(3)=F(2)+F(1)=1+1=2
$$

$$
F(4)=F(3)+F(2)=2+1=3
$$

---

## ২. সমস্যা কোথায়?

সাধারণ Recursive পদ্ধতিতে যদি `F(5)` বের করি:

```
                    F(5)
                  /      \
              F(4)        F(3)
             /    \       /   \
          F(3)   F(2)   F(2)  F(1)
          /  \    / \    / \
       F(2) F(1) F(1) F(0) F(1) F(0)
       / \
    F(1) F(0)
```

```text
F(5)
├── F(4)
│   ├── F(3)
│   │   ├── F(2)
│   │   └── F(1)
│   └── F(2)
└── F(3)
    ├── F(2)
    └── F(1)
```

এখানে লক্ষ্য করো:
একই subproblem বারবার calculate হয় (overlapping subproblems)। \
**F(3), F(2)** ইত্যাদি একই calculation বারবার হচ্ছে।

- **F(3) দুইবার**, **F(2) তিনবার** calculate হচ্ছে \
- Time Complexity: **O(2ⁿ)** (exponential), n = 40-এও অনেক slow

DP-র সমাধান: একবার calculate করে result store করে রাখো, পরে সরাসরি ব্যবহার করো।

এটাকে বলে:

### Overlapping Subproblems

অর্থাৎ একই ছোট সমস্যার সমাধান বারবার করতে হচ্ছে।

Dynamic Programming এই repeated calculation-টা এড়িয়ে যায়।

---

## ৩. Dynamic Programming কী করে?

DP-তে একবার কোনো Fibonacci value বের করলে সেটাকে **store করে রাখি**।

ধরো `n = 7`।

আমরা একে একে হিসাব করব:

|  i | Fibonacci |
| -: | --------: |
|  0 |         0 |
|  1 |         1 |
|  2 |         1 |
|  3 |         2 |
|  4 |         3 |
|  5 |         5 |
|  6 |         8 |
|  7 |        13 |

তাই:

$$
\boxed{F(7)=13}
$$

---

## ৪. DP দিয়ে Algorithm

এখানে আমরা একটি `dp[]` array ব্যবহার করব।

```text
Fibonacci(n):

    dp[0] = 0
    dp[1] = 1

    for i = 2 to n:
        dp[i] = dp[i-1] + dp[i-2]

    return dp[n]
```

### সহজভাবে বুঝলে

প্রথমে:

```text
dp[0] = 0
dp[1] = 1
```

তারপর:

```text
dp[2] = dp[1] + dp[0]
      = 1 + 0
      = 1
```

এরপর:

```text
dp[3] = dp[2] + dp[1]
      = 1 + 1
      = 2
```

তারপর:

```text
dp[4] = dp[3] + dp[2]
      = 2 + 1
      = 3
```

এভাবে চলতে থাকবে।

---

## ৫. `F(7)` সম্পূর্ণভাবে

```text
dp[0] = 0
dp[1] = 1

dp[2] = dp[1] + dp[0] = 1
dp[3] = dp[2] + dp[1] = 2
dp[4] = dp[3] + dp[2] = 3
dp[5] = dp[4] + dp[3] = 5
dp[6] = dp[5] + dp[4] = 8
dp[7] = dp[6] + dp[5] = 13
```

সুতরাং:

**Answer = 13**

---

## ৬. Time Complexity

এখানে `2` থেকে `n` পর্যন্ত মাত্র একবার loop চলছে।

তাই:

$$
\boxed{Time\ Complexity=O(n)}
$$

আর আমরা `dp[0]` থেকে `dp[n]` পর্যন্ত array রাখছি।

তাই:

$$
\boxed{Space\ Complexity=O(n)}
$$

---

## ৭. আরও Efficient DP

একটা গুরুত্বপূর্ণ বিষয় পরীক্ষায় আসতে পারে।

আমাদের আসলে পুরো `dp[]` array দরকার নেই।

কারণ:

$$
dp[i]=dp[i-1]+dp[i-2]
$$

অর্থাৎ নতুন value বের করার জন্য শুধু **আগের দুইটি value** দরকার।

তাই:

```text
a = 0
b = 1

for i = 2 to n:
    c = a + b
    a = b
    b = c

return b
```

এখানে:

```text
a → আগের আগের সংখ্যা
b → আগের সংখ্যা
c → বর্তমান সংখ্যা
```

তাই Space Complexity হয়ে যায়:

$$
\boxed{O(1)}
$$

Time Complexity এখনও:

$$
\boxed{O(n)}
$$

---

## ৮. পরীক্ষার জন্য সবচেয়ে গুরুত্বপূর্ণ

| বিষয়                | উত্তর                      |
| ------------------- | -------------------------- |
| Fibonacci formula   | `F(n) = F(n-1) + F(n-2)`   |
| Base cases          | `F(0)=0, F(1)=1`           |
| DP কেন ব্যবহার করি? | Repeated calculation এড়াতে |
| DP-এর মূল concept   | Overlapping Subproblems    |
| Tabulation time     | **O(n)**                   |
| Tabulation space    | **O(n)**                   |
| Space-optimized DP  | **O(1)** space             |
| `F(7)`              | **13**                     |
| Fibonacci sequence  | 0, 1, 1, 2, 3, 5, 8...     |

### 🎯 Government Exam-এর জন্য এক লাইনে

> **Dynamic Programming ব্যবহার করে Fibonacci Series-এর পূর্বে গণনা করা ফল সংরক্ষণ করা হয়, ফলে overlapping subproblems পুনরায় calculate করতে হয় না এবং time complexity O(2ⁿ) থেকে O(n)-এ কমে যায়।**

**মনে রাখার shortcut:**

> **Fibonacci → Previous 2 → Store Result → Avoid Repetition → O(n)**

<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>

# 08.Construct a logical argument explaining why a heuristic (like A search) can be faster than a blind search (like BFS), even if it doesn't guarantee the absolute shortest path in all cases.

## Heuristic Search (A*) কেন Blind Search (BFS)-এর চেয়ে দ্রুত হতে পারে

## মূল Argument (এক লাইনে)

**BFS goal-এর দিক জানে না, তাই সব দিকে সমানভাবে ছড়ায়। Heuristic goal-এর দিকে "guide" করে, তাই অপ্রয়োজনীয় node expand করতে হয় না।**

---

## Logical Argument (Step by Step)

**Premise 1:** BFS শুধু start থেকে দূরত্ব (depth) দেখে node expand করে। Goal কোন দিকে, সেই তথ্য ব্যবহার করে না। তাই এটি **সব দিকে বৃত্তের মতো** ছড়ায়।

**Premise 2:** Branching factor `b` এবং goal depth `d` হলে BFS-এর expand করা node প্রায় **O(bᵈ)**।

**Premise 3:** A* প্রতিটি node-এর জন্য `f(n) = g(n) + h(n)` হিসাব করে এবং **সবচেয়ে কম f(n)** আগে expand করে।
- `g(n)` = start থেকে n পর্যন্ত আসল cost
- `h(n)` = n থেকে goal পর্যন্ত **আনুমানিক** cost (heuristic)

**Premise 4:** যে node goal থেকে দূরে সরে যাচ্ছে, তার `h(n)` বড় হয়, তাই `f(n)` বড় হয় এবং সেটি **priority queue-র পেছনে পড়ে থাকে**, expand-ই হয় না।

**Conclusion:** A* অনেক node **prune (বাদ)** করে, শুধু goal-মুখী node expand করে। ফলে কম node, কম time, কম memory লাগে।

---

## Diagram: Grid-এ তুলনা

`S` = Start, `G` = Goal (ডান দিকে)

```
BFS (সব দিকে ছড়ায়):          A* (goal-এর দিকে যায়):

 · · · · · · · ·               · · · · · · · ·
 · · ○ ○ ○ · · ·               · · · · · · · ·
 · ○ ○ ○ ○ ○ · ·               · · · · ○ ○ · ·
 · ○ ○ S ○ ○ ○ G               · · S ○ ○ ○ ○ G
 · ○ ○ ○ ○ ○ · ·               · · · · ○ ○ · ·
 · · ○ ○ ○ · · ·               · · · · · · · ·
 · · · · · · · ·               · · · · · · · ·

 ○ = expanded node             ○ = expanded node
 (প্রায় ২৫টি)                 (প্রায় ৮টি)
```

BFS **পেছনের ও উল্টো দিকের** node-ও expand করে, A* করে না।

---

## Numerical Example

Branching factor **b = 3**, goal depth **d = 10**:

| Algorithm | Expanded Node (আনুমানিক) |
|---|---|
| BFS | 3¹⁰ ≈ **59,000** |
| A* (ভালো heuristic, effective b ≈ 1.5) | 1.5¹⁰ ≈ **58** |

Heuristic ভালো হলে **effective branching factor (b\*)** কমে যায়, আর সেটাই exponential সাশ্রয়ের মূল কারণ।

---

## "Shortest Path Guarantee না থাকলেও" কেন Faster?

এখানে একটি গুরুত্বপূর্ণ কথা: **Admissible heuristic** (`h(n) ≤ আসল cost`, কখনো বাড়িয়ে বলে না) হলে A* **optimal path-ই দেয়**। Guarantee হারায় শুধু এই অবস্থায়:

- Heuristic **overestimate** করলে (inadmissible)
- **Greedy Best-First** ব্যবহার করলে (শুধু `h(n)` দেখে)
- **Weighted A\*** (`f = g + w·h`, w > 1) ব্যবহার করলে

**তখন কেন faster?** কারণ heuristic-কে বেশি বিশ্বাস করলে search আরও **aggressively goal-মুখী** হয়, কম node expand হয়। বিনিময়ে path সামান্য লম্বা হতে পারে। এটি একটি **speed vs optimality trade-off**।

```
Admissible h      → Optimal path, তুলনামূলক বেশি node
Overestimating h  → দ্রুত, কিন্তু path suboptimal হতে পারে
h = 0             → A* = Dijkstra (blind), কোনো speedup নেই
```

**Real-life Example:** Google Maps-এ Dhaka থেকে Chittagong যেতে BFS সব রাস্তা সমানভাবে দেখত। A* সরাসরি দূরত্ব (straight-line) দিয়ে শুধু Chittagong-মুখী রাস্তা দেখে। কয়েক সেকেন্ডের মধ্যে পাওয়া যায় "যথেষ্ট ভালো" route।

---

## তুলনামূলক ছক

| বিষয় | BFS (Blind) | A* (Heuristic) |
|---|---|---|
| Goal-এর তথ্য | ব্যবহার করে না | `h(n)` দিয়ে ব্যবহার করে |
| Expand করা node | অনেক বেশি | কম |
| Time | O(bᵈ) | O(b\*ᵈ), b\* < b |
| Optimal? | হ্যাঁ (unweighted-এ) | হ্যাঁ, যদি h admissible |
| Memory | অনেক বেশি | কম (সাধারণত) |
| Worst case | O(bᵈ) | O(bᵈ), h খারাপ হলে BFS-এর সমান |

---

## পরীক্ষার টিপস ✍️

- মূল যুক্তি লিখবে: **"Heuristic search space prune করে, তাই কম node expand হয়"**
- Formula অবশ্যই লিখবে: **f(n) = g(n) + h(n)**
- **Admissible** শব্দটি ও তার সংজ্ঞা (`h(n) ≤ h*(n)`) লিখবে, এতে extra নম্বর
- সৎভাবে লিখবে: **A\* admissible heuristic-এ optimal**; guarantee যায় শুধু inadmissible বা greedy/weighted ক্ষেত্রে
- **Worst case-এ A\* ≈ BFS** (heuristic অকেজো হলে), এটা mention করলে answer পূর্ণাঙ্গ হয়
- BFS vs A*-এর grid diagram এঁকে **expanded node-এর পার্থক্য** দেখাবে

<br>

# Explanation about Heuristic
# Heuristic Search: একদম বেসিক থেকে

আগের উত্তরটা একটু কঠিন হয়ে গিয়েছিল। চলো ধাপে ধাপে বুঝি।

---

## ধাপ ১: Search Problem মানে কী?

কম্পিউটারকে বলা হয়: **Start থেকে Goal-এ যাওয়ার পথ খুঁজে বের করো।**

যেমন: Google Maps-এ তুমি **ঢাকা** থেকে **চট্টগ্রাম** যেতে চাও। কম্পিউটারকে হাজার হাজার রাস্তার মধ্য থেকে সঠিক পথ বের করতে হবে। একে বলে **Search**।

---

## ধাপ ২: Blind Search (BFS) কী?

**Blind = অন্ধ।** এই search-এর কাছে কোনো hint নেই। Goal কোন দিকে, সে জানে না।

**উদাহরণ:** অন্ধকার ঘরে হারানো চাবি খুঁজছো। তুমি কী করবে? প্রথমে নিজের চারপাশ, তারপর একটু দূরে, তারপর আরও দূরে। **সব দিকে সমানভাবে** হাতড়াতে থাকবে।

BFS ঠিক এভাবেই কাজ করে: **সব দিকে ছড়ায়**, ভুল দিকেও যায়। সে শেষে goal পাবেই, কিন্তু **অনেক সময় নষ্ট** হয়।

---

## ধাপ ৩: Heuristic কী?

**Heuristic = আন্দাজ বা অনুমান** (educated guess)। এটা একটা **hint**, যা বলে "Goal এখান থেকে মোটামুটি কতদূর।"

**উদাহরণ:** ঢাকায় দাঁড়িয়ে তুমি জানো চট্টগ্রাম **দক্ষিণ-পূর্ব দিকে**। রাস্তা না জেনেও তুমি বুঝতে পারো, উত্তরে (রংপুরের দিকে) গেলে চট্টগ্রাম থেকে দূরে সরে যাচ্ছি।

এই **"সোজা দূরত্ব (straight-line distance)"** অনুমানটাই একটা heuristic। একে `h(n)` লেখা হয়।

---

## ধাপ ৪: Heuristic Search কী?

> **Heuristic Search = Hint (আন্দাজ) ব্যবহার করে Goal-এর দিকে বুদ্ধি খাটিয়ে খোঁজা।**

সহজ তুলনা:

| | Blind Search (BFS) | Heuristic Search (A*) |
|---|---|---|
| তুলনা | অন্ধকারে হাতড়ানো | টর্চ নিয়ে goal-এর দিকে যাওয়া |
| Goal কোন দিকে | জানে না | আন্দাজ করতে পারে |
| কোথায় যায় | সব দিকে | শুধু ভালো দিকে |

---

## ধাপ ৫: ছোট Example (Step by Step)

নিচের map-এ **S** থেকে **G**-তে যেতে হবে। প্রতিটি রাস্তার cost = **1**।

```
          ┌── A ──┬─ A1
          │       └─ A2
    S ────┼── B ──┬─ B1
          │       └─ B2
          └── C ── E ── G  (Goal)
```

A আর B-এর দিকে গেলে goal পাওয়া যায় না (ভুল দিক)। সঠিক পথ: **S → C → E → G**

### BFS কী করে?

Level by level সব দেখে:

```
Level 0: S
Level 1: A, B, C         ← তিনটাই দেখলো
Level 2: A1, A2, B1, B2, E   ← ভুল দিকের ৪টাও দেখলো!
Level 3: G  ✅
```

**Expand করা node = ৯টি** (S, A, B, C, A1, A2, B1, B2, E)

### Heuristic Search (A*) কী করে?

প্রতিটি node-এর জন্য একটা **score f** হিসাব করে এবং **সবচেয়ে কম score** আগে বেছে নেয়।

```
f = g + h

g = Start থেকে এখন পর্যন্ত আসল cost
h = এখান থেকে Goal পর্যন্ত আন্দাজ (heuristic)
```

ধরো আন্দাজ (h) এরকম: Goal-এর কাছে হলে ছোট সংখ্যা, দূরে হলে বড়।

| Node | g (এসেছি) | h (আন্দাজ বাকি) | f = g + h |
|---|---|---|---|
| A | 1 | 4 (দূরে) | **5** |
| B | 1 | 4 (দূরে) | **5** |
| C | 1 | 2 (কাছে) | **3** ✅ |
| E | 2 | 1 | **3** ✅ |
| G | 3 | 0 | **3** ✅ |

**S থেকে শুরু করে A*-এর চিন্তা:**

```
Step 1: S থেকে A(f=5), B(f=5), C(f=3) পেলাম
        → সবচেয়ে কম f = C, তাই C-তে যাই
Step 2: C থেকে E(f=3) পেলাম
        → A, B-এর f=5 বেশি, তাই E-তে যাই
Step 3: E থেকে G(f=3) পেলাম → Goal পেয়ে গেছি! ✅
```

**Expand করা node = ৪টি** (S, C, E, G)। A আর B **একবারও expand হয়নি।**

---

## তুলনা

| | BFS | A* |
|---|---|---|
| Expand করা node | **৯টি** | **৪টি** |
| ভুল দিকে সময় নষ্ট | হয়েছে | হয়নি |

**এটাই heuristic search-এর সুবিধা:** hint দেখে ভুল দিকের রাস্তা **বাদ দিয়ে** দেয়, তাই কম কাজে goal পায়। Map যত বড় হবে, এই পার্থক্য তত বিশাল হবে।

---

## ধাপ ৬: "Shortest Path Guarantee না থাকলেও" মানে কী?

প্রশ্নে এই অংশটা কঠিন লাগছে, তাই সহজ করে বলি।

আন্দাজ (heuristic) দুই রকম হতে পারে:

1. **সৎ আন্দাজ (Admissible):** কখনো আসল দূরত্বের **বেশি** বলে না।
   - যেমন সোজা দূরত্ব। আসল রাস্তা সোজা দূরত্বের চেয়ে কম হতে পারে না।
   - এতে A* **সবসময় সবচেয়ে ছোট পথই** পায়।

2. **বেশি আত্মবিশ্বাসী আন্দাজ:** আন্দাজকে **অতিরিক্ত বিশ্বাস** করে।
   - এতে search আরও দ্রুত goal-এর দিকে ছোটে।
   - কিন্তু মাঝে মাঝে **একটু লম্বা পথ** পেয়ে যেতে পারে।

**মূল কথা:** আন্দাজকে যত বেশি বিশ্বাস করবে, তত **দ্রুত** পাবে, কিন্তু path সামান্য লম্বা হওয়ার ঝুঁকি থাকে। এটা একটা **speed বনাম perfect path**-এর trade-off। তাই প্রশ্নে বলা হয়েছে, "shortest path না পেলেও faster হতে পারে।"

---

## এক নজরে সারসংক্ষেপ

```
Blind Search (BFS)  → hint নেই → সব দিকে ছড়ায় → ধীর
Heuristic Search    → hint আছে (h) → goal-মুখী → দ্রুত

A* formula:  f(n) = g(n) + h(n)
             g = এসেছি কতটা,  h = বাকি আছে আন্দাজ কতটা
```

---

## পরীক্ষায় যা লিখবে ✍️

- **সংজ্ঞা:** "Heuristic হলো goal পর্যন্ত দূরত্বের একটি অনুমান, যা search-কে সঠিক দিকে guide করে।"
- **যুক্তি:** "BFS সব দিকে ছড়ায়, কিন্তু heuristic search ভুল দিকের node বাদ দেয়, তাই কম node expand হয় এবং দ্রুত হয়।"
- **Formula:** `f(n) = g(n) + h(n)`
- ছোট একটা graph এঁকে **BFS-এ ৯টি vs A*-এ ৪টি node** দেখাও
- একটা real-life example দাও: Google Maps-এ সোজা দূরত্ব দিয়ে route খোঁজা

কোন অংশটা এখনো পরিষ্কার না হলে বলো, আমি সেটা আরও সহজ করে বুঝিয়ে দেব।