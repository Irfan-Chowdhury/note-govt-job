# 🏔️ Heap Data Structure — বাংলায় সম্পূর্ণ ব্যাখ্যা

> **Heap** হলো একটি বিশেষ **Complete Binary Tree**, যেখানে Parent ও Child-এর মধ্যে নির্দিষ্ট বড়-ছোট সম্পর্ক বজায় থাকে।
> Priority Queue, Heap Sort, Heapify ও Time Complexity বোঝার জন্য এটি খুব গুরুত্বপূর্ণ।

---

## 📑 সূচিপত্র
1. Heap কী?
2. Heap কত প্রকার (Max / Min)
3. Complete Binary Tree কেন গুরুত্বপূর্ণ
4. Array Representation
5. Insertion
6. Deletion / Extract Max
7. নিজে Practice করুন
8. Heapify ও Build Heap
9. Heap Sort
10. Time Complexity
11. Heap বনাম BST
12. ব্যবহার
13. পরীক্ষার আগে Revision

---

## 1. Heap কী? (Definition)

Heap হলো একটি **Complete Binary Tree**, যেখানে Parent ও Child Node-এর মধ্যে **Max Heap অথবা Min Heap**-এর নিয়ম মানা হয়।

**Heap হওয়ার জন্য দুটি শর্ত:**

| # | শর্ত | মানে |
|---|---|---|
| 1 | **Complete Binary Tree Property** | শেষ Level ছাড়া সব Level পূর্ণ; শেষ Level-এর Node **বাম দিক থেকে ধারাবাহিকভাবে** বসবে |
| 2 | **Heap Property** | Parent ও Child-এর মধ্যে Max বা Min Heap-এর নিয়ম থাকবে |

```
Heap = Complete Binary Tree  +  Heap Property
```

> ⚠️ **গুরুত্বপূর্ণ:** Heap একটি **BST নয়**। Heap-এ Left Child, Right Child-এর চেয়ে ছোট বা বড় হতেই হবে, এমন নিয়ম নেই।

---

## 2. Heap কত প্রকার?

```
                 Heap
            ┌─────┴─────┐
        Max Heap     Min Heap
     (Parent ≥ Child) (Parent ≤ Child)
     Root = সর্বোচ্চ    Root = সর্বনিম্ন
```

### 🔺 Max Heap
প্রতিটি Parent-এর মান তার Child-এর মানের **সমান বা বড়**।

```
              90
            /    \
          70      80
         /  \    /  \
       20   40  50   60

Array: [90, 70, 80, 20, 40, 50, 60]
```

### 🔻 Min Heap
প্রতিটি Parent-এর মান তার Child-এর মানের **সমান বা ছোট**।

```
              10
            /    \
          20      30
         /  \
       40   50

Array: [10, 20, 30, 40, 50]
```

### তুলনা

| বৈশিষ্ট্য | Max Heap | Min Heap |
|---|---|---|
| **Root** | Maximum Value | Minimum Value |
| **Parent ও Child** | Parent ≥ Child | Parent ≤ Child |
| **বেশি Priority পায়** | বড় Value | ছোট Value |
| **Root-এর মান খোঁজা** | O(1) | O(1) |

---

## 3. Complete Binary Tree কেন গুরুত্বপূর্ণ?

সব Binary Tree Heap হতে পারে না। Heap **অবশ্যই Complete Binary Tree** হতে হবে।

```
✅ Complete Binary Tree          ❌ Complete নয়              ❌ Complete নয়
(বাম থেকে ক্রমানুসারে পূর্ণ)      (2-এর Left নেই,            (2-এর Child নেই,
                                  কিন্তু Right আছে)          অথচ 3-এর Child আছে)

        1                              1                          1
      /   \                          /   \                      /   \
     2     3                        2     3                    2     3
    / \   /                          \                              /
   4   5 6                            4                            4
```

> এই পার্থক্য Competitive Exam-এ প্রায়ই প্রশ্ন হিসেবে আসে।

---

## 4. Heap-এর Array Representation

Complete Binary Tree-এর Node-গুলো **Level Order**-এ Array-তে ফাঁক ছাড়া সাজানো যায়। তাই Heap সাধারণত **Array** দিয়ে সংরক্ষণ করা হয় (Pointer লাগে না)।

```
Max Heap:                     Array (Level Order):
              90
            /    \             Index:  0   1   2   3   4   5   6
          70      80           Value: [90, 70, 80, 20, 40, 50, 60]
         /  \    /  \
       20   40  50   60
```

### Index সূত্র

| সম্পর্ক | **0-based** | **1-based** |
|---|---|---|
| **Parent** | ⌊(i − 1) / 2⌋ | ⌊i / 2⌋ |
| **Left Child** | 2i + 1 | 2i |
| **Right Child** | 2i + 2 | 2i + 1 |

### উদাহরণ (0-based): Index 1-এ মান 70

- Left Child Index = 2 × 1 + 1 = **3** → Value **20**
- Right Child Index = 2 × 1 + 2 = **4** → Value **40**
- Parent Index = ⌊(1 − 1) / 2⌋ = **0** → Value **90**

### দরকারি তথ্য (n টি Node, 0-based)

| বিষয় | মান |
|---|---|
| **শেষ Non-leaf Node-এর Index** | ⌊n/2⌋ − 1 |
| **Leaf Node-এর Index** | ⌊n/2⌋ থেকে n − 1 |
| **Leaf সংখ্যা** | ⌈n/2⌉ |
| **Height** | ⌊log₂ n⌋ |

---

## 5. Heap Insertion — নতুন Node কীভাবে যোগ হয়?

**নিয়ম:**
1. নতুন Node **সবশেষে** ফাঁকা জায়গায় বসবে
2. Parent-এর সাথে তুলনা
3. নতুন Node **বড় হলে** (Max Heap) Parent-এর সাথে **Swap**
4. Heap Property ঠিক না হওয়া পর্যন্ত ওপরে উঠতে থাকবে

এই প্রক্রিয়ার নাম: **Heapify Up / Bubble Up / Sift Up**

**Max Heap:** `[50, 30, 40, 10, 20, 35, 37]` — এখন **45** Insert করব।

```
শুরুতে:
            50
          /    \
        30      40
       /  \    /  \
     10   20  35   37

ধাপ 1: 45 সবশেষে বসাই (Index 7, Parent = 10)
            50
          /    \
        30      40
       /  \    /  \
     10   20  35   37
    /
  45

ধাপ 2: 45 > 10, তাই Swap
            50
          /    \
        30      40
       /  \    /  \
     45   20  35   37
    /
  10

ধাপ 3: 45 > 30, তাই Swap
            50
          /    \
        45      40
       /  \    /  \
     30   20  35   37
    /
  10

ধাপ 4: 45 < 50, তাই থামি ✅
```

**ফলাফল Array:** `[50, 45, 40, 30, 20, 35, 37, 10]`

> ⏱️ **Insertion Time Complexity: O(log n)**, কারণ সর্বোচ্চ Tree-এর Height বরাবর ওপরে উঠতে পারে।

---

## 6. Heap Deletion / Extract Max

Max Heap-এ সবচেয়ে বড় মান **Root**-এ থাকে। **Extract Max** দিয়ে Root সরানো হয়।

**নিয়ম:**
1. Root-এর মান (50) সরিয়ে রাখি
2. **শেষ Node**-কে Root-এ আনি
3. শেষ Position মুছে দিই
4. নতুন Root-কে **বড় Child**-এর সাথে Swap করে নিচে নামাই (**Heapify Down**)
5. Heap Property ঠিক হলে থামি

**Max Heap:** `[50, 45, 40, 30, 20, 35, 37, 10]` — 50 Delete করব।

```
শুরুতে:
            50
          /    \
        45      40
       /  \    /  \
     30   20  35   37
    /
  10

ধাপ 1-3: শেষ Node (10) Root-এ আনি, শেষ Position মুছি
            10
          /    \
        45      40
       /  \    /  \
     30   20  35   37

ধাপ 4: 10-এর Child 45 ও 40 → বড় 45-এর সাথে Swap
            45
          /    \
        10      40
       /  \    /  \
     30   20  35   37

ধাপ 5: 10-এর Child 30 ও 20 → বড় 30-এর সাথে Swap
            45
          /    \
        30      40
       /  \    /  \
     10   20  35   37

ধাপ 6: 10 এখন Leaf, থামি ✅
```

**ফলাফল Array:** `[45, 30, 40, 10, 20, 35, 37]`

> ⏱️ **Extract Max Time Complexity: O(log n)**

---

## 7. ✍️ নিজে Practice করুন

### Practice 1: খালি Max Heap-এ ক্রমানুসারে Insert: 20, 15, 30, 10, 40

| Insert | Array (ধাপ) | কী ঘটল |
|---|---|---|
| 20 | `[20]` | Root |
| 15 | `[20, 15]` | 15 < 20, Swap নেই |
| 30 | `[30, 15, 20]` | 30 > 20 → Swap |
| 10 | `[30, 15, 20, 10]` | 10 < 15, Swap নেই |
| 40 | `[40, 30, 20, 10, 15]` | 40 > 15 → Swap, 40 > 30 → Swap |

```
Final Max Heap:
            40
          /    \
        30      20
       /  \
     10   15
```

### Practice 2: নিজে করুন
Array `[12, 11, 13, 5, 6, 7]` থেকে **Max Heap** বানান।

<details>
<summary>উত্তর দেখুন</summary>

- শেষ Non-leaf Index = ⌊6/2⌋ − 1 = 2 (মান 13), Child 7 → ঠিক আছে
- Index 1 (মান 11), Child 5, 6 → ঠিক আছে
- Index 0 (মান 12), Child 11, 13 → বড় 13-এর সাথে Swap → `[13, 11, 12, 5, 6, 7]`
- 12-এর নতুন Child 7 → ঠিক আছে

**Max Heap: `[13, 11, 12, 5, 6, 7]`**

</details>

---

## 8. Heapify কী?

**Heapify** হলো Heap Property নষ্ট হয়ে গেলে সেটি **পুনরায় ঠিক করার প্রক্রিয়া।**

| Heapify Type | কীভাবে কাজ করে | কোথায় ব্যবহার হয় |
|---|---|---|
| **Heapify Up** | Child থেকে Parent-এর দিকে | **Insertion** |
| **Heapify Down** | Parent থেকে Child-এর দিকে | **Root Deletion, Build Heap** |

### Build Heap: Unsorted Array থেকে Heap

**Unsorted Array:** `[10, 20, 15, 30, 40]` → **Max Heap**

**নিয়ম:** শেষ Non-leaf Node (⌊n/2⌋ − 1 = Index 1) থেকে শুরু করে **Index 0 পর্যন্ত পেছন দিকে** Heapify Down চালাই (**Bottom-Up**)।

```
শুরুতে (Heap Property নেই):
        10
       /  \
     20    15
    /  \
  30   40

ধাপ 1: Index 1 (20) Heapify → বড় Child 40, Swap
        10
       /  \
     40    15
    /  \
  30   20

ধাপ 2: Index 0 (10) Heapify → বড় Child 40, Swap
        40
       /  \
     10    15
    /  \
  30   20

ধাপ 3: 10 আরও নিচে → বড় Child 30, Swap
        40
       /  \
     30    15
    /  \
  10   20     ✅ Max Heap
```

**ফলাফল:** `[40, 30, 15, 10, 20]`

> ⭐ **Build Heap-এর Time Complexity: O(n)**, **O(n log n) নয়!**
>
> **কেন?** একটি Heapify-এর Worst Case O(log n) হলেও, **অর্ধেক Node-ই Leaf** (Heapify লাগে না), আর বেশিরভাগ Node Tree-এর নিচের দিকে, যাদের নামার দূরত্ব কম। যোগ করলে মোট O(n)।

---

## 9. Heap Sort কীভাবে কাজ করে?

**Heap Sort** একটি **Comparison-Based** Sorting Algorithm। **Ascending** Order-এ সাজাতে **Max Heap** ব্যবহার হয়।

```
ধাপ A: Array থেকে Max Heap বানাও                 (Build Heap, O(n))
ধাপ B: Root (সর্বোচ্চ) কে শেষ Element-এর সাথে Swap
ধাপ C: Heap Size ১ কমাও (শেষ Element Sorted হয়ে গেছে)
ধাপ D: নতুন Root-এ Heapify Down
ধাপ E: Size ১ হওয়া পর্যন্ত B–D পুনরাবৃত্তি
```

**Array:** `[4, 10, 3, 5, 1]`

**Max Heap তৈরি:** `[10, 5, 3, 4, 1]`

```
        10
       /  \
      5    3
     / \
    4   1
```

| ধাপ | কাজ | Array (দাঁড়ির ডান পাশ = Sorted অংশ) | Heap Size |
|---|---|---|---|
| শুরু | Max Heap | `[10, 5, 3, 4, 1]` | 5 |
| 1 | 10 ↔ 1 Swap, Heapify | `[5, 4, 3, 1 \| 10]` | 4 |
| 2 | 5 ↔ 1 Swap, Heapify | `[4, 1, 3 \| 5, 10]` | 3 |
| 3 | 4 ↔ 3 Swap, Heapify | `[3, 1 \| 4, 5, 10]` | 2 |
| 4 | 3 ↔ 1 Swap | `[1 \| 3, 4, 5, 10]` | 1 |

### ✅ Sorted Output: `[1, 3, 4, 5, 10]`

> ⏱️ **Heap Sort: O(n log n)**, Best, Average ও Worst **তিন Case-এই।** Space: **O(1)** (In-place)। Stable নয়।

---

## 10. Heap-এর Time Complexity

| Operation | Time Complexity |
|---|---|
| Get Min / Get Max (Root) | **O(1)** |
| Insert | **O(log n)** |
| Extract Root | **O(log n)** |
| Heapify একটি Node | **O(log n)** (Worst Case) |
| Build Heap (Bottom-Up) | **O(n)** |
| Search Arbitrary Value | **O(n)** |
| Heap Sort | **O(n log n)** |

(n = মোট Node সংখ্যা)

**কেন Insertion O(log n)?** Complete Binary Tree-এর Height **O(log n)**। নতুন Node-কে সর্বোচ্চ Root পর্যন্ত উঠতে হতে পারে।

---

## 11. Heap বনাম Binary Search Tree (BST)

| বিষয় | **Heap** | **BST** |
|---|---|---|
| **Structure** | **Complete** Binary Tree | সাধারণ Binary Tree (Complete হওয়া বাধ্যতামূলক নয়) |
| **Property** | Parent ≥ / ≤ Child | Left ছোট, Right বড় |
| **Root** | Min বা Max | যেকোনো মান |
| **Search** | O(n) Worst Case | O(log n) Average, O(n) Worst |
| **প্রধান ব্যবহার** | **Priority Queue** | Searching, Ordered Data |
| **Inorder Sorted?** | সাধারণত **না** | **হ্যাঁ** |

> ⚠️ **MCQ Trap:** Max Heap-এ Root সর্বোচ্চ হলেও Left ও Right Subtree **সম্পূর্ণ Sorted থাকে না।**

---

## 12. Heap কোথায় ব্যবহার হয়?

```
                         Heap-এর ব্যবহার
   ┌──────────┬─────────────┬────────────┬───────────┬──────────┐
Priority    Heap Sort   Dijkstra's   Prim's     Top K       Median
Queue                   Algorithm    Algorithm  Elements    Finding
```

| ব্যবহার | কীভাবে |
|---|---|
| **Priority Queue** | সর্বোচ্চ/সর্বনিম্ন Priority-এর Task আগে Process |
| **Heap Sort** | Array Sort করা |
| **Dijkstra's Algorithm** | Min Priority Queue দিয়ে সবচেয়ে কম tentative distance-এর Vertex নির্বাচন |
| **Prim's Algorithm** | MST তৈরিতে পরবর্তী Minimum Edge নির্বাচন |
| **Top K Elements** | সবচেয়ে বড়/ছোট K টি Value দক্ষতার সাথে বের করা |
| **Median Finding** | দুটি Heap (Max + Min) দিয়ে চলমান Data Stream-এর Median |

### Real Scenario
**হাসপাতালের Emergency বিভাগ:** রোগী আসার ক্রমে নয়, **অবস্থার গুরুত্ব (Priority)** অনুযায়ী চিকিৎসা হয়। সবচেয়ে বেশি Priority-র রোগী সবার আগে ডাকা হয়, ঠিক **Max Heap-ভিত্তিক Priority Queue**-র মতো।

### PHP Reference
```php
// Max Heap: সবচেয়ে বড় মান আগে বের হয়
$heap = new SplMaxHeap();
foreach ([10, 40, 20] as $n) { $heap->insert($n); }   // Insert: O(log n)
echo $heap->top();       // 40 (Root, O(1))
echo $heap->extract();   // 40 (Extract Max, O(log n))

// Min Heap
$min = new SplMinHeap();

// Priority Queue
$pq = new SplPriorityQueue();
$pq->insert('Critical Patient', 10);   // (value, priority)
$pq->insert('Normal Patient', 1);
echo $pq->extract();     // 'Critical Patient' (বেশি priority আগে)
```

---

## 13. 📌 পরীক্ষার আগে এক নজরে Revision

### Heap-এর সবচেয়ে গুরুত্বপূর্ণ ৮টি তথ্য

1. Heap হলো একটি **Complete Binary Tree**।
2. **Max Heap**-এর Root-এ **Maximum** Value থাকে।
3. **Min Heap**-এর Root-এ **Minimum** Value থাকে।
4. Heap সাধারণত **Array** দিয়ে Implement করা হয়।
5. **Insertion** ও **Extract Root**-এর Complexity **O(log n)**।
6. **Bottom-Up Build Heap**-এর Complexity **O(n)**।
7. **Heap Sort**-এর Complexity **O(n log n)**।
8. Heap **Sorted Tree নয়**; শুধু Parent–Child Ordering বজায় থাকে।

### অতিরিক্ত MCQ-তথ্য

| প্রশ্ন | উত্তর |
|---|---|
| Heap-এ Root-এর মান জানতে সময়? | **O(1)** |
| Heap-এ যেকোনো মান খুঁজতে সময়? | **O(n)** |
| Heap Sort কি Stable? | **না** |
| Heap Sort-এর Space Complexity? | **O(1)** |
| Ascending Sort-এ কোন Heap? | **Max Heap** |
| Descending Sort-এ কোন Heap? | **Min Heap** |
| Insertion-এ কোন Heapify? | **Heapify Up** |
| Deletion/Build Heap-এ কোন Heapify? | **Heapify Down** |
| 1-based Index-এ Parent, Left, Right? | **⌊i/2⌋, 2i, 2i+1** |
| Heap-এর Height? | **⌊log₂ n⌋** |

## 🎯 পরীক্ষার টিপস

- **Numerical প্রশ্নে** প্রতিটি Swap-এর পর **Array আবার লিখুন**, ধাপ-অনুযায়ী নম্বর পাওয়া যায়।
- Insert, Delete, Build Heap, Heap Sort, এই **চারটি** Step-by-step করতে পারলে Written ও MCQ-র বেশিরভাগ প্রশ্ন হয়ে যায়।
- প্রশ্নে **0-based না 1-based** Index, তা আগে দেখে নিন, নইলে Formula ভুল হবে।
- **Build Heap = O(n)** আর **Heap Sort = O(n log n)**, এই পার্থক্য প্রায়ই ফাঁদ হিসেবে আসে।
- **Heap ≠ BST**, এই তুলনা Written ও MCQ দুটোতেই আসে।

> **পরবর্তী গুরুত্বপূর্ণ Topic:** Priority Queue এবং Heap Sort-এর Numerical Problems।
