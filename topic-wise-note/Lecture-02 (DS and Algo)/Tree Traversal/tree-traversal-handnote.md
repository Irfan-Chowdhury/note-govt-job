# 🌳 Tree Traversal in Data Structure — বাংলায় সম্পূর্ণ ব্যাখ্যা

> **Tree Traversal** হলো একটি Tree-এর প্রতিটি Node নির্দিষ্ট নিয়ম অনুসারে **একবার করে Visit** করার প্রক্রিয়া।
> Binary Tree, Binary Search Tree (BST), Recursion ও Algorithm বোঝার জন্য এটি খুব গুরুত্বপূর্ণ।

---

## 📑 সূচিপত্র
1. Tree-এর Basic Concept
2. Traversal কত প্রকার
3. Preorder
4. Inorder
5. Postorder
6. Level Order (BFS)
7. নিজে Practice করুন
8. Algorithm (Pseudocode)
9. Time ও Space Complexity
10. Expression Tree-তে ব্যবহার
11. পরীক্ষায় গুরুত্বপূর্ণ তথ্য

---

## 1. Tree-এর Basic Concept

আমাদের উদাহরণ Binary Tree:

```
              A            ← Level 0 (Root)
            /   \
          B       C        ← Level 1
         / \     / \
        D   E   F   G      ← Level 2 (Leaf)
```

| শব্দ | এই Tree-তে | মানে |
|---|---|---|
| **Root Node** | A | Tree-এর সর্বোচ্চ Node |
| **Parent Node** | B (D ও E-এর) | যার নিচে Child আছে |
| **Child Node** | D, E (B-এর) | Parent-এর ঠিক নিচের Node |
| **Leaf Node** | D, E, F, G | যাদের কোনো Child নেই |
| **Left Subtree** | B, D, E | Root-এর বাম দিকের অংশ |
| **Right Subtree** | C, F, G | Root-এর ডান দিকের অংশ |

> 💡 **মূল কথা:** Tree একই থাকে, শুধু Traversal-এর **নিয়ম বদলালে Visit-এর ক্রম বদলে যায়।**

---

## 2. Tree Traversal কত প্রকার?

```
                    Tree Traversal
                  ┌───────┴────────┐
          DFS (Depth First)    BFS (Breadth First)
          ┌──────┼──────┐             │
      Preorder Inorder Postorder  Level Order
       (NLR)    (LNR)    (LRN)    (Queue ব্যবহার)
```

| Traversal | Visiting Order | সংক্ষেপে |
|---|---|---|
| **Preorder** | Root → Left → Right | NLR |
| **Inorder** | Left → Root → Right | LNR |
| **Postorder** | Left → Right → Root | LRN |
| **Level Order** | Level by Level | BFS |

> **Root** মানে: যে Node বা Subtree নিয়ে আমরা কাজ করছি, তার Root।

### এক নজরে: Root কখন Visit হয়?

```
Preorder  :  ★ Root  →  Left  →  Right     (Root আগে)
Inorder   :  Left  →  ★ Root  →  Right     (Root মাঝে)
Postorder :  Left  →  Right  →  ★ Root     (Root শেষে)
```

---

## 3. Preorder Traversal (Root → Left → Right)

**নিয়ম:** প্রথমে Root, তারপর Left Subtree, সবশেষে Right Subtree। **(NLR)**

**ধাপে ধাপে:**
1. প্রথমে Root **A** Visit
2. Left Subtree-তে গিয়ে **B**, তারপর **D**, তারপর **E**
3. Right Subtree-তে গিয়ে **C**, তারপর **F**, তারপর **G**

**Visit-এর ক্রম (নম্বর = কত নম্বরে Visit):**

```
              A(1)
            /     \
         B(2)      C(5)
        /   \      /   \
     D(3)  E(4)  F(6)  G(7)
```

### ✅ Preorder Output: `A - B - D - E - C - F - G`

> মনে রাখবেন: Preorder-এ **প্রতিটি Subtree-এর Root সর্বপ্রথম** Visit হয়।

---

## 4. Inorder Traversal (Left → Root → Right)

**নিয়ম:** প্রথমে Left Subtree, তারপর Root, সবশেষে Right Subtree। **(LNR)**

**ধাপে ধাপে:**
1. A-এর Left Subtree-তে যাই
2. B-এর Left Child **D** Visit
3. এরপর **B** Visit
4. তারপর **E** Visit
5. এখন Root **A** Visit
6. Right Subtree-তে গিয়ে **F, C, G** Visit

```
              A(4)
            /     \
         B(2)      C(6)
        /   \      /   \
     D(1)  E(3)  F(5)  G(7)
```

### ✅ Inorder Output: `D - B - E - A - F - C - G`

> ⭐ **গুরুত্বপূর্ণ:** **BST-এর Inorder Traversal** করলে মানগুলো **Ascending (ছোট থেকে বড়) Order**-এ পাওয়া যায়। (শর্ত: Left-এর মান ছোট, Right-এর মান বড়)

---

## 5. Postorder Traversal (Left → Right → Root)

**নিয়ম:** Root সবার **শেষে** Visit হয়। **(LRN)**

**ধাপে ধাপে:**
1. B-এর Left Child **D** Visit
2. B-এর Right Child **E** Visit
3. এরপর **B** Visit
4. C-এর Left Child **F** Visit
5. C-এর Right Child **G** Visit
6. এরপর **C** Visit
7. সবশেষে Root **A** Visit

```
              A(7)
            /     \
         B(3)      C(6)
        /   \      /   \
     D(1)  E(2)  F(4)  G(5)
```

### ✅ Postorder Output: `D - E - B - F - G - C - A`

> মনে রাখবেন: Postorder-এ **প্রতিটি Subtree-এর Root তার Child-গুলোর পরে** Visit হয়।

---

## 6. Level Order Traversal (BFS)

ওপর থেকে নিচে, প্রতিটি Level বাম থেকে ডানে Visit করা হয়।

```
Level 0 :        A
                 │
Level 1 :     B     C
              │     │
Level 2 :  D  E  F  G
```

| Level | Nodes |
|---|---|
| 0 | A |
| 1 | B, C |
| 2 | D, E, F, G |

### ✅ Output: `A → B → C → D → E → F → G`

**Queue (FIFO) কীভাবে কাজ করে:**

```
শুরু       : Queue = [A]
A বের করো  : Visit A,  Queue = [B, C]
B বের করো  : Visit B,  Queue = [C, D, E]
C বের করো  : Visit C,  Queue = [D, E, F, G]
D, E, F, G : একে একে বের করে Visit
```

> Level Order সাধারণত **Queue (FIFO)** দিয়ে Implement করা হয়।

---

## 7. ✍️ নিজে Practice করুন

### Practice 1: BST
**Node Insert-এর ক্রম:** 50, 30, 70, 20, 40, 60, 80

```
              50
            /    \
          30      70
         /  \    /  \
       20   40  60   80
```

| Traversal | Output |
|---|---|
| **Preorder** | 50, 30, 20, 40, 70, 60, 80 |
| **Inorder** | 20, 30, 40, 50, 60, 70, 80 *(Sorted ✅)* |
| **Postorder** | 20, 40, 30, 60, 80, 70, 50 |
| **Level Order** | 50, 30, 70, 20, 40, 60, 80 |

### Practice 2: নিজে করুন
উপরের মূল Tree (A–G) দেখে **হাতে লিখে** চারটি Traversal বের করুন, তারপর নিচের উত্তরের সাথে মিলিয়ে নিন।

<details>
<summary>উত্তর দেখুন</summary>

- Preorder: A-B-D-E-C-F-G
- Inorder: D-B-E-A-F-C-G
- Postorder: D-E-B-F-G-C-A
- Level Order: A-B-C-D-E-F-G

</details>

---

## 8. Traversal-এর Algorithm (Recursion)

### Preorder
```
PREORDER(node)
    IF node is NULL
        RETURN

    PRINT node.data          ← শুরুতে PRINT
    PREORDER(node.left)
    PREORDER(node.right)
```

### Inorder
```
INORDER(node)
    IF node is NULL
        RETURN

    INORDER(node.left)
    PRINT node.data          ← মাঝখানে PRINT
    INORDER(node.right)
```

### Postorder
```
POSTORDER(node)
    IF node is NULL
        RETURN

    POSTORDER(node.left)
    POSTORDER(node.right)
    PRINT node.data          ← শেষে PRINT
```

> 🔑 **তিনটি Algorithm-এর একমাত্র পার্থক্য: `PRINT node.data`-এর অবস্থান।**
> - শুরুতে PRINT = **Preorder**
> - মাঝখানে PRINT = **Inorder**
> - শেষে PRINT = **Postorder**

---

## 9. Time Complexity ও Space Complexity

ধরি, Node সংখ্যা = **n**, Tree-এর Height = **h**, সবচেয়ে প্রশস্ত Level-এর Node সংখ্যা = **w**

| Traversal | Time Complexity | Auxiliary Space |
|---|---|---|
| Preorder | **O(n)** | **O(h)** |
| Inorder | **O(n)** | **O(h)** |
| Postorder | **O(n)** | **O(h)** |
| Level Order | **O(n)** | **O(w)** |

**কেন Time Complexity O(n)?**
প্রতিটি Node **ঠিক একবার** Visit হয়। ৭টি Node হলে ৭ বার, ১০০টি হলে ১০০ বার।

**Space (DFS-এর Recursion Stack):**

| Tree-এর ধরন | Height (h) | Space |
|---|---|---|
| Balanced Tree | log n | **O(log n)** |
| Skewed Tree (সম্পূর্ণ একপাশে) | n | **O(n)** |

---

## 10. Expression Tree-তে Traversal

Expression: **(A + B) * C**

```
            *
          /   \
         +     C
        / \
       A   B
```

| Traversal | Output | Expression-এর নাম |
|---|---|---|
| **Preorder** | `* + A B C` | **Prefix** |
| **Inorder** | `A + B * C` | **Infix** (বন্ধনী ছাড়া) |
| **Postorder** | `A B + C *` | **Postfix** |

---

## 11. 📌 পরীক্ষায় গুরুত্বপূর্ণ তথ্য

| প্রশ্ন | উত্তর |
|---|---|
| Preorder-এ Root কখন Visit হয়? | **প্রথমে** |
| Inorder-এ Root কখন Visit হয়? | Left ও Right Subtree-এর **মাঝখানে** |
| Postorder-এ Root কখন Visit হয়? | **সবশেষে** |
| BFS-এর জন্য কোন Data Structure? | **Queue** |
| Iterative DFS-এ কোন Data Structure? | **Stack** |
| BST-এর কোন Traversal Sorted Output দেয়? | **Inorder** |
| Traversal-এর Time Complexity? | **O(n)** |
| Expression Tree-তে Prefix পাওয়া যায় কোন Traversal-এ? | **Preorder** |
| Postfix Expression পাওয়া যায় কোন Traversal-এ? | **Postorder** |
| Level Order-এর Space Complexity? | **O(w)** (সবচেয়ে প্রশস্ত Level) |
| DFS-এর Space Complexity? | **O(h)** |

### অতিরিক্ত তথ্য
- **Preorder + Inorder** (অথবা **Postorder + Inorder**) দিলে Binary Tree **অনন্যভাবে** পুনর্গঠন করা যায়।
- Tree **copy** করতে সাধারণত **Preorder**, আর Tree **delete** করতে **Postorder** ব্যবহৃত হয় (Child আগে মুছে তারপর Parent)।

---

## 🎯 পরীক্ষার টিপস

- **Root-এর অবস্থান মনে রাখার কৌশল:** Pre = আগে, In = মাঝে, Post = পরে।
- Traversal লিখতে বললে আগে **Tree আঁকুন**, তারপর প্রতিটি Subtree-তে **একই নিয়ম** প্রয়োগ করুন (Recursion)।
- BST দেওয়া থাকলে **Inorder সবসময় Sorted**, এটি দিয়ে দ্রুত উত্তর যাচাই করা যায়।
- MCQ-তে মনে রাখুন: **BFS = Queue, DFS = Stack/Recursion।**
- Time Complexity সবসময় **O(n)**, শুধু Space নিয়ে প্রশ্ন বেশি আসে: **O(h)** বনাম **O(w)**।

---

## ⚡ এক নজরে মনে রাখুন

```
Preorder   : Root আগে          → Prefix Expression, Tree Copy
Inorder    : Root মাঝখানে       → BST-এ Sorted Output
Postorder  : Root শেষে          → Postfix Expression, Tree Delete
Level Order: ওপর থেকে নিচে      → Queue ব্যবহার (BFS)
```

> Tree Traversal শেখার পর **Recursion Call Stack**, **BST Traversal** ও **Expression Tree** অনুশীলন করলে Data Structure-এর এই অংশ আরও পরিষ্কার হবে।
