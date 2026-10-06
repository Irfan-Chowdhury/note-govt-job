## First Format — Exam Answer

**Topic:** Data Structure & Graph Theory → Graph Representation → Adjacency List vs Adjacency Matrix

**Answer:**

* **Adjacency List is more efficient** for **sparse graphs**, graph traversal (BFS/DFS), and finding all neighbors of a vertex.
* **Adjacency Matrix is more efficient** for **dense graphs** and checking whether an edge exists between two vertices.

**Complexity:**

| Operation          | Adjacency List | Adjacency Matrix |
| ------------------ | -------------: | ---------------: |
| Space              |     \(O(V+E)\) |       \(O(V^2)\) |
| Check edge \(u,v\) | \(O(\deg(u))\) |         \(O(1)\) |
| Find neighbors     | \(O(\deg(u))\) |         \(O(V)\) |
| BFS / DFS          |     \(O(V+E)\) |       \(O(V^2)\) |

---

# Second Format — Basic Topic-wise Explanation in Bangla

### 1. Graph কী?

Graph হলো **Vertex (Node)** এবং **Edge** দিয়ে তৈরি একটি data structure।

উদাহরণ:

```text
A ----- B
|       |
|       |
C ----- D
```

এখানে:

* Vertex = A, B, C, D
* Edge = A-B, A-C, B-D, C-D

Graph computer-এ store করার দুটি common method:

1. **Adjacency List**
2. **Adjacency Matrix**

---

## 2. Adjacency List কী?

Adjacency List-এ প্রতিটি vertex-এর সাথে তার connected vertices-এর list রাখা হয়।

উপরের graph-এর জন্য:

```text
A → B, C
B → A, D
C → A, D
D → B, C
```

অর্থাৎ A-এর সাথে কারা connected?

`B, C`

এগুলো সরাসরি list-এ পাওয়া যায়।

### Space Complexity

$$
O(V+E)
$$

এখানে:

* \(V\) = number of vertices
* \(E\) = number of edges

তাই graph-এ edge কম থাকলে এটি খুব memory-efficient।

---

# 3. Sparse Graph কী?

যখন vertex অনেক, কিন্তু edge তুলনামূলকভাবে কম, তখন সেটিকে **Sparse Graph** বলে।

যেমন:

```text
A --- B     C --- D     E
```

এখানে vertex অনেক হলেও connection কম।

এই ধরনের graph-এর জন্য:

> **Adjacency List ভালো।**

কারণ matrix ব্যবহার করলে অনেক unnecessary `0` store করতে হবে।

---

# 4. Adjacency Matrix কী?

Adjacency Matrix হলো একটি \(V \times V\) table।

যদি দুটি vertex connected থাকে:

$$
1
$$

না থাকলে:

$$
0
$$

উপরের graph:

```text
    A B C D
A   0 1 1 0
B   1 0 0 1
C   1 0 0 1
D   0 1 1 0
```

যেমন A এবং B-এর মধ্যে edge আছে।

তাই:

$$
Matrix[A][B]=1
$$

---

## 5. Matrix-এর সবচেয়ে বড় সুবিধা

ধরুন প্রশ্ন:

> A এবং D-এর মধ্যে সরাসরি edge আছে কি?

Matrix-এ শুধু check করতে হবে:

$$
Matrix[A][D]
$$

যদি 1 → edge আছে
যদি 0 → edge নেই

তাই time:

$$
O(1)
$$

অর্থাৎ **constant time**।

---

# 6. কোন Problem Adjacency List-এ বেশি Efficient?

### BFS / DFS Traversal

BFS বা DFS করার সময় প্রতিটি vertex-এর neighbor দরকার।

Adjacency List-এ neighbors সরাসরি পাওয়া যায়।

Time Complexity:

$$
O(V+E)
$$

কিন্তু Matrix-এ প্রতিটি vertex-এর জন্য পুরো row check করতে হয়।

তাই:

$$
O(V^2)
$$

সুতরাং:

> **BFS/DFS → Adjacency List বেশি efficient।**

---

## 7. কোন Problem Adjacency Matrix-এ বেশি Efficient?

যদি বারবার জানতে হয়:

> Vertex \(u\) এবং \(v\)-এর মধ্যে edge আছে কি?

Adjacency Matrix:

$$
O(1)
$$

Adjacency List:

$$
O(\deg(u))
$$

কারণ u-এর neighbor list search করতে হবে।

তাই:

> **Frequent edge existence checking → Adjacency Matrix ভালো।**

---

# 8. Dense Graph কী?

যখন অধিকাংশ vertex একে অপরের সাথে connected থাকে, তখন তাকে **Dense Graph** বলে।

যেমন:

```text
A ----- B
|\     /|
| \   / |
|  \ /  |
|  / \  |
| /   \ |
C ----- D
```

এখানে অনেক edge রয়েছে।

Dense graph-এ:

$$
E \approx V^2
$$

তাই Matrix-এর \(O(V^2)\) space তখন খুব বেশি waste হয় না।

---

# 9. Main Comparison

| Feature          | Adjacency List | Adjacency Matrix |
| ---------------- | -------------- | ---------------- |
| Best for         | Sparse Graph   | Dense Graph      |
| Memory           | কম             | বেশি             |
| Edge checking    | তুলনামূলক slow | খুব fast         |
| Neighbor finding | Fast           | তুলনামূলক slow   |
| BFS/DFS          | Efficient      | Less efficient   |
| Space            | \(O(V+E)\)     | \(O(V^2)\)       |

---

### Govt Job Exam Shortcut

মনে রাখবেন:

> **LIST = Less edges**

অর্থাৎ Sparse Graph → **Adjacency List**

আর:

> **MATRIX = Quick Match**

অর্থাৎ দুটি vertex connected কিনা check → **Adjacency Matrix**

সবচেয়ে গুরুত্বপূর্ণ:

$$
\boxed{\text{Sparse Graph → Adjacency List}}
$$

$$
\boxed{\text{Dense Graph → Adjacency Matrix}}
$$

$$
\boxed{\text{BFS/DFS → Adjacency List}}
$$

$$
\boxed{\text{Edge Checking → Adjacency Matrix}}
$$
