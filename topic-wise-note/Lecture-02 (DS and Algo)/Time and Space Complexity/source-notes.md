# ১. ভিত্তি: Algorithm, Analysis ও Input Size

> **Learning outcome:** Algorithm কী, কেন বিশ্লেষণ করি, `n` কী বোঝায়, এবং Time–Space Complexity-এর সঠিক পার্থক্য বুঝতে পারবেন।

## ১.১ Algorithm কী?

**English exam definition:** *An algorithm is a finite, well-defined sequence of unambiguous steps to solve a problem or compute a result.*

বাংলায়: একটি নির্দিষ্ট সমস্যা সমাধানের জন্য পরিষ্কার, সুনির্দিষ্ট এবং সসীম সংখ্যক ধাপের পদ্ধতিকে **Algorithm** বলে। উদাহরণ—ক্লাসের সর্বোচ্চ নম্বর বের করা: (১) প্রথম নম্বরকে সর্বোচ্চ ধরা, (২) বাকি নম্বরগুলোর সঙ্গে তুলনা করা, (৩) বেশি পেলে সর্বোচ্চ পরিবর্তন করা, (৪) শেষে ফল প্রকাশ করা।

**একটি ভালো Algorithm-এর বৈশিষ্ট্য:** Input (শূন্য বা একাধিক হতে পারে), Output (অন্তত একটি), Definiteness (প্রতিটি ধাপ স্পষ্ট), Finiteness (শেষ হবে), Effectiveness (ধাপ বাস্তবে সম্পাদনযোগ্য)। Correctness এবং Efficiency আলাদাভাবে বিচার করা হয়।

```text
MAXIMUM(A, n)
    largest = A[0]
    for i = 1 to n-1
        if A[i] > largest
            largest = A[i]
    return largest
```

এখানে সর্বোচ্চ **n−1**টি comparison হয়; তাই Input বাড়লে কাজ লিনিয়ারভাবে বাড়ে।

## ১.২ Algorithm Analysis কী এবং কেন প্রয়োজন?

**English exam definition:** *Algorithm analysis studies the computational resources, especially time and memory, required by an algorithm as a function of input size.*

একই সমস্যার একাধিক সমাধান থাকতে পারে। কোনটি বড় Input-এর ক্ষেত্রে বেশি কার্যকর, তা বোঝার জন্য Time ও Memory-এর Growth পরীক্ষা করি। শুধু ঘড়িতে মেপে '২ সেকেন্ড' বলা যথেষ্ট নয়—কম্পিউটার, Compiler, Language, Network, Cache ইত্যাদি বদলালে সময় বদলায়। Complexity মূলত **Input Size পরিবর্তনের সঙ্গে Resource Requirement-এর বৃদ্ধির ধরণ** প্রকাশ করে।

{{DIAGRAM:flow}}

## ১.৩ Input Size `n` কী?

- ৫টি সংখ্যার Array: `n = 5`; ১০ লাখের Array: `n = 1,000,000`।
- String Search-এ `n` String-এর দৈর্ঘ্য হতে পারে।
- Graph-এ প্রায়ই দুটি মাপ লাগে: `V` = Vertex ও `E` = Edge; তখন Complexity `O(V+E)` হতে পারে।
- Matrix-এ `r × c` Element; দুটি Dimension-ই আলাদাভাবে ধরতে হতে পারে।
- দুইটি ভিন্ন Array: দৈর্ঘ্য `n` ও `m` হলে Nested Loop-এর Complexity `O(nm)`, অকারণে `O(n²)` নয়।

## ১.৪ Time Complexity বনাম Space Complexity

| দিক | Time Complexity | Space Complexity |
|---|---|---|
| প্রশ্ন | কতগুলো মূল Operation/Step? | কত Memory প্রয়োজন? |
| সাধারণ একক | Growth in steps | Growth in memory cells/bytes |
| উদাহরণ | Array scan → `O(n)` time | Input বাদে sum variable → `O(1)` auxiliary |
| গুরুত্বপূর্ণ সতর্কতা | Big O সরাসরি সেকেন্ড নয় | Auxiliary ও Total Space এক বিষয় নয় |

**লাইব্রেরি উদাহরণ (আগের আলোচনার ধারণা):** সাজানো নয় এমন ১০০০টি বইয়ের মধ্যে একটি বই খুঁজতে শুরু থেকে একটি একটি করে দেখা (Linear Search) Worst Case-এ ১০০০টি পরীক্ষা করতে পারে, `O(n)`। সাজানো বইয়ের Catalog-এ Binary Search প্রত্যেক ধাপে সম্ভাব্য অংশ অর্ধেক করে, `O(log n)`। তবে Binary Search-এর জন্য সাজানো ও Random-Access উপযোগী তালিকা প্রয়োজন।

## ১.৫ Best, Average ও Worst Case

`A = [10, 20, 30, 40, 50]`-এ **Linear Search** দিয়ে `x` খুঁজলে:

| Case | উদাহরণ | Comparisons | Tight bound |
|---|---|---:|---|
| Best | `x = 10` | ১ | `Θ(1)` |
| Average* | লক্ষ্য সমান সম্ভাবনায় যেকোনো অবস্থানে | `(n+1)/2` | `Θ(n)` |
| Worst | `x = 50` অথবা অনুপস্থিত | সর্বোচ্চ `n` | `Θ(n)` |

\* **Average** নির্দিষ্ট Probability Distribution-এর ওপর নির্ভর করে; প্রতিটি Algorithm-এর জন্য 'মাঝের অবস্থান' ধরে নেওয়া যায় না।

**বিশেষ পরীক্ষার ফাঁদ:** `O()` নিজে Worst Case-এর সমার্থক নয়। এটি Mathematical Upper Bound; নির্দিষ্ট Best/Average/Worst-case Function-এর জন্যও Big O ব্যবহার করা যায়।

## ১.৬ একটি Code-এর Operation Count

```c
int sum = 0;                // একবার initialization
for (int i = 0; i < n; i++) // loop n iterations
    sum += a[i];            // n বার addition/assignment
printf("%d", sum);          // একবার output
```

এখানে মোট কাজ `an+b` আকারের (a,b ধ্রুবক)। **Growth:** `Θ(n)` time। `sum` এবং `i` স্থির সংখ্যক Memory Cell ⇒ `Θ(1)` auxiliary space। Input Array `a`-সহ মোট Space ⇒ `Θ(n)`।

# ২. Asymptotic Notation: Big O, Ω, Θ, o, ω

> **Learning outcome:** Bound-এর সঠিক অর্থ, Formal Definition, Constant ও Dominant Term বাদ দেওয়ার নিয়ম শিখবেন।

## ২.১ কেন Asymptotic Analysis?

ধরি দুটি Algorithm-এর Operation Count `T₁(n)=3n+5`, `T₂(n)=n²+2`। ছোট n-এ ফল ভিন্ন হতে পারে, কিন্তু অনেক বড় n-এর জন্য Growth Trend-ই প্রধান। Asymptotic Analysis-এ স্থির Constant এবং Lower-order Terms Growth Classification পরিবর্তন করে না।

## ২.২ Big O — Upper Bound

**English:** *`f(n) = O(g(n))` if there exist constants `c > 0` and `n₀` such that `0 ≤ f(n) ≤ c g(n)` for every `n ≥ n₀`.*

উদাহরণ: `f(n) = 3n + 5`। `n ≥ 1` হলে `3n+5 ≤ 8n`। কাজেই `3n+5 = O(n)`। **অর্থ:** পর্যাপ্ত বড় n-এ f(n) কোনো ধ্রুবক গুণিতক `n`-এর উপরে যায় না।

## ২.৩ Big Omega (Ω) — Lower Bound

**English:** *`f(n) = Ω(g(n))` if for all sufficiently large n, `f(n) ≥ c g(n)` for some constant `c > 0`.*

`3n+5 ≥ 3n` ⇒ `3n+5 = Ω(n)`। এর মানে **অন্তত সেই Growth Rate-এর সমান**।

## ২.৪ Big Theta (Θ) — Tight Bound

**English:** *`f(n) = Θ(g(n))` if `f(n)` is both `O(g(n))` and `Ω(g(n))`.*

`3n+5 = Θ(n)`; কারণ একই সঙ্গে Upper এবং Lower Bound `n` দিয়ে প্রতিষ্ঠিত। পরীক্ষায় 'Exact Asymptotic Order' জিজ্ঞেস করলে Θ উপযোগী। **সঠিকভাবে:** `n = O(n²)` সত্য, কিন্তু `n = Θ(n²)` ভুল।

{{DIAGRAM:bounds}}

## ২.৫ Little o এবং Little omega (Advanced)

- `f(n) = o(g(n))` মানে f **strictly slower-growing**: `lim f(n)/g(n) = 0` (যখন সংশ্লিষ্ট Limit প্রযোজ্য)। যেমন `n = o(n²)`।
- `f(n) = ω(g(n))` মানে f **strictly faster-growing**: `lim f(n)/g(n) = ∞`। যেমন `n² = ω(n)`।
- `n` কিন্তু `o(n)` নয়; `n = Θ(n)`।

## ২.৬ Growth Simplification — পরীক্ষার Shortcut

| Operation Count | Tight asymptotic bound | কারণ |
|---|---|---|
| `100` | `Θ(1)` | Constant |
| `7n + 900` | `Θ(n)` | Constant, coefficient বাদ |
| `3n² + 8n + 1` | `Θ(n²)` | Highest-degree term |
| `n log₂n + 20n` | `Θ(n log n)` | Dominant term |
| `n³ + 2ⁿ` | `Θ(2ⁿ)` | Exponential eventually dominates |
| `log₂n` vs `log₁₀n` | উভয় `Θ(log n)` | Base পরিবর্তন Constant Factor |

**পরীক্ষায় Calculation:** `T(n)=5n²+3n+7` ⇒ সবচেয়ে দ্রুত বাড়ে `n²` ⇒ **Θ(n²)**। কিন্তু সব ক্ষেত্রে সংখ্যাগত Runtime-ও বড় হবে, এমন দাবি করা যাবে না; Constant ও hardware গুরুত্বপূর্ণ।

<details><summary>Formal Bound প্রমাণ: `5n² + 3n + 7 = Θ(n²)`</summary>
`n ≥ 1`-এ `5n² ≤ 5n²+3n+7 ≤ 15n²` (কারণ `3n ≤ 3n²`, `7 ≤ 7n²`)। অতএব `c₁=5`, `c₂=15`, `n₀=1` বাছলে দুটি Bound পূরণ হয়।
</details>

# ৩. Common Time Complexities ও Growth Chart

> **Learning outcome:** সবচেয়ে সাধারণ আটটি Growth Class চিনবেন, তুলনা করবেন, Code-এর সঙ্গে মিলিয়ে দেখবেন।

{{CHART:growth}}

## ৩.১ `O(1)` — Constant

```c
int x = a[2];          // valid array index access
int y = x + 5;
```

স্থির সংখ্যক Operation। Array-তে ৫টি বা ১০ লাখ Element থাকলেও নির্দিষ্ট Index Access-এর Asymptotic Cost `Θ(1)`। **সতর্কতা:** Input-এর ওপর নির্ভর না করলেও বাস্তবে Operation Zero Time নয়।

## ৩.২ `O(log n)` — Logarithmic

```c
while (n > 1) {
    n = n / 2;
}
```

Input প্রতি Iteration-এ অর্ধেক: `16 → 8 → 4 → 2 → 1`। ৪টি Halving; `log₂16=4`। `1024 → 1` যেতে ১০টি Halving। `O(log n)` সাধারণত Binary Search ও Balanced Tree Search-এ পাওয়া যায়।

{{DIAGRAM:halving}}

## ৩.৩ `O(n)` — Linear

```c
for (int i = 0; i < n; i++) {
    printf("%d ", a[i]);
}
```

`n` Elements দেখলে `n` বার Visit করতে হয়। ৫ → ৫ iterations; ১০০ → ১০০ iterations। Loop variable fixed space ⇒ `O(1)` Auxiliary Space।

## ৩.৪ `O(n log n)` — Linearithmic

Merge Sort দুটি Half-এর Result Merge করে। Recursion depth প্রায় `log₂ n`; প্রতিটি Level-এ মোট `n` Element Process ⇒ `Θ(n log n)`। Standard Merge Sort-এর Auxiliary Array `Θ(n)` Space নেয়।

{{DIAGRAM:mergesort}}

## ৩.৫ `O(n²)` — Quadratic

```c
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        printf("*");
    }
}
```

প্রতি Outer Iteration-এ `n`টি Inner Iteration; মোট `n×n = n²`। `n=4 → 16`, `n=100 → 10,000`। কিন্তু **দুটি Nested Loop মানেই সর্বদা n² নয়**; Bounds পরীক্ষা করতে হবে।

## ৩.৬ `O(n³)` — Cubic

তিনটি স্বাধীন `n`-Iteration Loop হলে `n×n×n = n³`। উদাহরণ, Classical Triple-loop Matrix Multiplication (সমান আকারের n×n Matrix) `Θ(n³)` Arithmetic Operations।

## ৩.৭ `O(2ⁿ)` — Exponential

Naive Recursive Fibonacci-এর Recurrence `T(n)=T(n−1)+T(n−2)+Θ(1)`। এটি **Θ(φⁿ)** (φ≈1.618) Growth; `O(2ⁿ)` একটি বৈধ কিন্তু Loose Upper Bound। `2ⁿ`-এর নিখুঁত উদাহরণ হলো `n`টি Element-এর সব Subset Enumerate করা: **Θ(n·2ⁿ)** Output Cost হতে পারে যদি প্রতিটি Subset-এর Element-গুলোও ছাপানো হয়, এবং **Θ(2ⁿ)** Leaf/Subset Count।

## ৩.৮ `O(n!)` — Factorial

`n`টি ভিন্ন Item-এর সব Permutation-এর সংখ্যা `n! = n×(n−1)×…×1`। সব Permutation-এ nটি Item লেখা হলে Output Work `Θ(n·n!)`। Permutation Count `Θ(n!)`। `5! = 120`; `8! = 40320`। Exhaustive Permutation Search-এ এটি গুরুত্বপূর্ণ।

## ৩.৯ তুলনা: n বাড়লে কী ঘটে?

| n | log₂n | n | n log₂n | n² | n³ | 2ⁿ | n! |
|---:|---:|---:|---:|---:|---:|---:|---:|
| 2 | 1 | 2 | 2 | 4 | 8 | 4 | 2 |
| 4 | 2 | 4 | 8 | 16 | 64 | 16 | 24 |
| 8 | 3 | 8 | 24 | 64 | 512 | 256 | 40,320 |
| 10 | 3.32 | 10 | 33.22 | 100 | 1,000 | 1,024 | 3,628,800 |
| 16 | 4 | 16 | 64 | 256 | 4,096 | 65,536 | 20,922,789,888,000 |

**Typical growth ordering** (large n, positive constants ignored): `1 < log n < n < n log n < n² < n³ < 2ⁿ < n!`। এই Ordering **Asymptotic**; ছোট n-এ মানের ক্রম ভিন্ন হতে পারে।

# ৪. Code Analysis: Statement, Loop, Recursion

> **Learning outcome:** নতুন Code দেখে নিজের হাতে Count বের করবেন। প্রতিটি উদাহরণে Time ও Extra Space আলাদা ভাববেন।

## ৪.১ Simple Statements ও Conditionals

```c
int a = 10;                  // Θ(1)
int b = a * 4 + 2;           // Θ(1)
if (x > 0)                  // constant-time comparison
    printf("positive");
else
    printf("non-positive");
```

স্থির সংখ্যক Primitive Operation ⇒ `Θ(1)` Time, `Θ(1)` Extra Space। `if`-এর Branch-এর Cost আলাদা হলে **Worst Case** সর্বাধিক Branch Cost; **Best Case** সবচেয়ে কম Branch Cost (condition evaluation-সহ)।

```c
if (flag) {
    for (int i = 0; i < n; i++) work(); // Θ(n)
} else {
    work();                              // Θ(1)
}
```

Best `Θ(1)`; Worst `Θ(n)` (ধরা হচ্ছে work() constant-time)। **Branch-এর Cost যোগ করবেন না**, একবারে একটি Branch চলে।

## ৪.২ Consecutive Loops: Add

```cpp
for (int i = 0; i < n; ++i) std::cout << i;
for (int j = 0; j < n; ++j) std::cout << j;
```

`n + n = 2n` ⇒ `Θ(n)` Time। যদি প্রথম Loop n², দ্বিতীয় Loop n হয়, `n²+n` ⇒ `Θ(n²)`।

## ৪.৩ Nested Loops: Multiply — তবে Bounds দেখুন

```java
for (int i=0; i<n; i++) {
    for (int j=0; j<n; j++) {
        System.out.print("*");
    }
}
```

`n × n = n²` ⇒ `Θ(n²)`; কিন্তু `j<n`-এর বদলে `j<m` হলে `Θ(nm)`।

## ৪.৪ Triangular Loop

```c
for (int i = 0; i < n; i++) {
    for (int j = 0; j < i; j++) {
        count++;
    }
}
```

Inner Iterations = `0+1+2+…+(n−1) = n(n−1)/2` ⇒ `Θ(n²)`। এটি Bubble/Selection Sort-এর Comparison Count বুঝতে সাহায্য করে।

{{DIAGRAM:triangle}}

## ৪.৫ Independent Growth এবং Unusual Loops

```c
for (int i=1; i<n; i*=2) work();   // Θ(log n)
for (int i=n; i>0; i/=3) work();   // Θ(log n)
for (int i=1; i*i<=n; i++) work(); // Θ(√n) (safe arithmetic assumed)
```

```c
for (int i=0; i<n; i++) {
    for (int j=1; j<n; j*=2) work();
}
```

Outer `Θ(n)`, Inner `Θ(log n)` ⇒ `Θ(n log n)`। আবার `for(i=1; i<n; i+=i)` অর্থাৎ `i` দ্বিগুণ ⇒ `Θ(log n)`; কিন্তু `i=0` থেকে `i+=i` শুরু করলে **Infinite Loop** হতে পারে।

## ৪.৬ Two-Pointer Loop: Nested হলেও O(n)

```cpp
int j = 0;
for (int i = 0; i < n; ++i) {
    while (j < n && a[j] < a[i]) {
        ++j;
    }
}
```

`j` কখনো Reset হয় না এবং সর্বোচ্চ `n` বার বাড়ে। Outer Loop n বার, Inner `while`-এর সব Iteration মিলিয়েও সর্বোচ্চ n ⇒ মোট `Θ(n)` (condition checks-সহ)। **Shortcut:** Loop-এর বডি কতবার **সর্বমোট** চলে, সেটি গণনা করুন।

## ৪.৭ Recursion ও Recurrence Relation

Recursion-এ Function নিজেকেই Call করে। **Base Case** না থাকলে থামবে না। Time Complexity বের করতে প্রতিটি Call কত কাজ করে এবং কয়টি Sub-call হয় তা দেখতে হয়। Space Complexity নির্ভর করে **Maximum Active Call-Stack Depth**-এর ওপর।

```c
void countdown(int n) {
    if (n <= 0) return;
    printf("%d ", n);
    countdown(n-1);
}
```

`T(n)=T(n−1)+Θ(1)` ⇒ `Θ(n)` Time। একসঙ্গে n+1টি Call Frame ⇒ `Θ(n)` Stack Space।

{{DIAGRAM:stack}}

## ৪.৮ Recurrence-এর আরও উদাহরণ

| Recurrence | সমাধান | কোথায় দেখা যায় |
|---|---|---|
| `T(n)=T(n−1)+1` | `Θ(n)` | Countdown |
| `T(n)=T(n/2)+1` | `Θ(log n)` | Binary Search |
| `T(n)=2T(n/2)+n` | `Θ(n log n)` | Merge Sort |
| `T(n)=2T(n/2)+1` | `Θ(n)` | Full binary divide tree |
| `T(n)=T(n−1)+n` | `Θ(n²)` | Growing repeated work |
| `T(n)=T(n−1)+T(n−2)+1` | `Θ(φⁿ)` | Naive Fibonacci |

**Master Theorem (intro):** `T(n)=aT(n/b)+f(n)`-এ `a≥1`, `b>1` এবং যথাযথ Regularity Conditions পূরণ হলে `n^(log_b a)`-এর সঙ্গে `f(n)` তুলনা করে Bound পাওয়া যায়। সব Recurrence-এ Master Theorem প্রযোজ্য নয়।

## ৪.৯ Common Mistakes / ভুলগুলো এড়িয়ে চলুন

1. `Big O = always worst case` — ভুল; Upper Bound ও Case Analysis আলাদা।
2. Consecutive Loop-এ Multiply করা — ভুল; Consecutive হলে **Add**, nested হলে সাধারণত **Multiply**, তবে shared pointers ও nonuniform bounds আলাদা।
3. Nested Loop দেখেই `O(n²)` বলা — ভুল; Inner Iterations যোগ করুন।
4. `O(n+m)`-কে `O(n)` ধরা — যদি m independent হয়, ভুল।
5. Log-এর Base নিয়ে অতিরিক্ত চিন্তা — Fixed-base Logs শুধু Constant Factor-এ আলাদা।
6. `T(n)=Θ(n²)` থেকে বাস্তব সময় 'নিশ্চয়ই n² সেকেন্ড' বলা — ভুল।
7. Recursive Algorithm-এ Call Stack বাদ দেওয়া — ভুল।
8. Binary Search Unsorted Data-তে চালানো — Standard Binary Search-এর Precondition লঙ্ঘন।
9. Mutable String Concatenation ও Immutable String Concatenation-কে একই Cost ধরা — ভুল; Representation গুরুত্বপূর্ণ।
10. Algorithm-এর Print/Output Work উপেক্ষা — Output Size নিজেই Lower Bound তৈরি করতে পারে।

<details><summary>পরীক্ষার ৫ ধাপের Decision Method</summary>
(১) Input size ও একাধিক dimension চিহ্নিত করুন। (২) Basic Operations-এর সংখ্যা Count করুন। (৩) Conditional হলে Case পৃথক করুন। (৪) Loops/Recurrence সমাধান করুন। (৫) Leading Term রেখে Bound লিখুন এবং Memory আলাদাভাবে গণনা করুন।
</details>

# ৫. Space Complexity: Input, Auxiliary, Stack, Trade-off

> **Learning outcome:** অতিরিক্ত Memory, Call Stack, In-place এবং Time–Space Trade-off সম্পর্কে সঠিক ধারণা অর্জন করবেন।

## ৫.১ Input Space বনাম Auxiliary Space

**English exam definitions:** *Input space is the storage occupied by the input. Auxiliary space is the additional working memory used by the algorithm, excluding its input.*

```c
int sum_array(const int a[], int n) {
    int sum = 0;
    for (int i=0; i<n; ++i) sum += a[i];
    return sum;
}
```

- Input Array storage = `Θ(n)` (ধরা হচ্ছে integer-এর Size Fixed)।
- `sum`, `i`, `n`-এর মতো কয়েকটি Scalar = `Θ(1)` **Auxiliary Space**।
- Array-সহ **Total Space** = `Θ(n)`।

## ৫.২ Variable Memory: Copy Array

```c
int *b = malloc(n * sizeof(int)); // ধারণাগত O(n) allocation
for (int i=0; i<n; ++i) b[i] = a[i];
free(b);
```

আরেকটি `n` Element-এর Array ⇒ `Θ(n)` Auxiliary Space; Copy Loop ⇒ `Θ(n)` Time। `malloc` ব্যর্থ হলে Check করতে হয়—উপরের Code শুধুমাত্র Complexity প্রদর্শনের জন্য।

{{DIAGRAM:memory}}

## ৫.৩ Arrays, Strings, Stack, Queue

| Data / Operation | Typical Time | Extra Space / মন্তব্য |
|---|---|---|
| Fixed Array Index Access | `Θ(1)` | `Θ(1)` |
| Copy n-length Array | `Θ(n)` | `Θ(n)` for new copy |
| Mutable String Character Access | `Θ(1)` when random-access representation | `Θ(1)` |
| String Scan / Length Calculation | `Θ(n)` if scanning | `Θ(1)` |
| Stack Push/Pop | `O(1)` typical | stored stack items take `Θ(k)` |
| Queue Enqueue/Dequeue | `O(1)` typical | queue contents take `Θ(k)` |
| Hash Table Lookup | `O(1)` average, `O(n)` worst possible | Table may use `Θ(n)` storage |

**সতর্কতা:** কোনো ভাষায় String Length cached থাকতে পারে (`O(1)`); অন্য Implementation-এ Scan করতে হতে পারে (`O(n)`)। Dynamic Array Append সাধারণত **Amortized O(1)**, একক Resize Operation `O(n)` হতে পারে।

## ৫.৪ Recursion Stack Visual

```c
void f(int n) {
    if (n == 0) return;
    f(n - 1);
}
```

`f(4) → f(3) → f(2) → f(1) → f(0)`। Base Case-এ পৌঁছানোর মুহূর্তে সর্বাধিক ৫টি Stack Frame। n-এর সঙ্গে Frame Number লিনিয়ার ⇒ `Θ(n)` Stack Space। Tail-call Optimization **নিশ্চিত নয়**, তাই সাধারণ পরীক্ষার বিশ্লেষণে সেটি ধরে নেবেন না।

## ৫.৫ Balanced vs Skewed Tree, Height ও Width

{{DIAGRAM:trees}}

Recursive DFS (Preorder/Inorder/Postorder): **Time `Θ(n)`, auxiliary stack `O(h)`** যেখানে `h` Tree Height (edge count হলে asymptotically frame count `h+1`)। Balanced Tree-তে `h=Θ(log n)`; skewed Tree-তে `h=Θ(n)`।

Level-order BFS: Queue-এর Space `O(w)`, যেখানে `w` Maximum Number of Nodes at One Level। একটি Balanced Complete Tree-এর শেষ Level বড় ⇒ `w=Θ(n)` হতে পারে। Skewed Tree-তে `w=1`, Queue Space `Θ(1)`। সর্বক্ষেত্রে Node Visit `Θ(n)` Time।

## ৫.৬ Iterative বনাম Recursive

**Binary Search:** Iterative Version: `Θ(log n)` Time, `Θ(1)` Extra Space। Recursive Version: `Θ(log n)` Time, `Θ(log n)` Stack Space (Tail-call Optimization না ধরে)। উভয় Algorithm-ই Sorted Array-তে সঠিক।

**Tree DFS:** Recursive Version Height অনুযায়ী Stack; Explicit Stack-ভিত্তিক Iterative DFS-এও Worst Case `O(h)` বা `O(n)` Storage পরিস্থিতি/Implementation অনুযায়ী হতে পারে।

## ৫.৭ In-place Algorithm

*An in-place algorithm uses only a constant amount of auxiliary memory*—এটি প্রচলিত ধারণা (কিছু Context-এ `O(log n)` Stack-সহ “in-place” বলা হয়; নির্দিষ্ট Definition স্পষ্ট রাখা ভালো)। Bubble Sort ও Selection Sort `Θ(1)` Auxiliary Space-এ Element Swap করতে পারে; Standard Merge Sort সাধারণত `Θ(n)` Extra Array ব্যবহার করে।

## ৫.৮ Time–Space Trade-off

- Hash Table-এ অতিরিক্ত Memory ব্যবহার করলে Search **Average `O(1)`**, কিন্তু Collision ও Resize-এর বিবেচনা আছে।
- Cached/Memoized Fibonacci অতিরিক্ত `O(n)` Memo Memory ব্যবহার করে `O(n)` Time অর্জন করতে পারে; Naive Recursive Version Exponential।
- Array Copy করলে Original Data অক্ষত থাকে, তবে `O(n)` অতিরিক্ত Storage লাগে।

**Exam Tip:** সবসময় দুটি আলাদা Line লিখুন: `Time = ...` এবং `Auxiliary Space = ...`।

# ৬. Important Algorithms: Search, Sort, Fibonacci, Array & String

> **Learning outcome:** Algorithm কীভাবে কাজ করে, Complexity কেন হয়, কোন Case ভিন্ন তা বিশ্লেষণ করতে পারবেন।

## ৬.১ Linear Search

**Idea:** প্রথম Element থেকে একটির পর একটি Target Compare করা।

```c
int linearSearch(const int a[], int n, int x) {
    for (int i=0; i<n; ++i)
        if (a[i] == x) return i;
    return -1;
}
```

- Best Time `Θ(1)` (প্রথম Element)।
- Average Time `Θ(n)` (সমান সম্ভাবনায় Target Position ধরলে)।
- Worst Time `Θ(n)` (শেষে/অনুপস্থিত)।
- Auxiliary Space `Θ(1)`।

## ৬.২ Binary Search — Sorted Array আবশ্যক

{{WIDGET:binary}}

{{DIAGRAM:binaryflow}}

```cpp
int binarySearch(const vector<int>& a, int target) {
    int lo = 0, hi = (int)a.size()-1;
    while (lo <= hi) {
        int mid = lo + (hi-lo)/2;
        if (a[mid] == target) return mid;
        if (a[mid] < target) lo = mid + 1;
        else hi = mid - 1;
    }
    return -1;
}
```

প্রতি Step-এ অপ্রয়োজনীয় অর্ধেক বাদ। Best `Θ(1)`, Worst `Θ(log n)`, Iterative Auxiliary `Θ(1)`। Recursive Binary Search-এর Stack `Θ(log n)` Worst Case। `mid = lo+(hi-lo)/2` লেখা Overflow Risk কমায়।

## ৬.৩ Bubble Sort

**Idea:** পাশাপাশি দুটি Element Compare করে ভুল ক্রম হলে Swap করা; প্রতি Pass-এ বড় Element শেষের দিকে ওঠে। **Early-exit Flag** দিলে ইতিমধ্যে Sorted Input-এর Best Time `Θ(n)`।

```c
void bubbleSort(int a[], int n) {
    for (int i=0; i<n-1; ++i) {
        int swapped = 0;
        for (int j=0; j<n-i-1; ++j) {
            if (a[j] > a[j+1]) {
                int t=a[j]; a[j]=a[j+1]; a[j+1]=t;
                swapped=1;
            }
        }
        if (!swapped) break;
    }
}
```

Best `Θ(n)` (optimized), Average/Worst `Θ(n²)`; Auxiliary `Θ(1)`; **Stable**।

## ৬.৪ Selection Sort

**Idea:** বাকি Unsorted অংশ থেকে Minimum বের করে বর্তমান Position-এ Swap করা। প্রায় প্রতিটি Case-এ Comparisons = `n(n−1)/2`।

```text
FOR i=0..n-2:
    minIndex = i
    FOR j=i+1..n-1:
        IF A[j] < A[minIndex]: minIndex = j
    SWAP A[i], A[minIndex]
```

Best/Average/Worst `Θ(n²)` Time, Auxiliary `Θ(1)`; Conventional Swapping Selection Sort সাধারণত **Unstable**।

## ৬.৫ Insertion Sort

**Idea:** প্রতিটি নতুন Element-কে ইতিমধ্যে Sorted Left Portion-এর সঠিক অবস্থানে Insert করা।

```java
for (int i=1; i<a.length; i++) {
    int key = a[i];
    int j = i-1;
    while (j>=0 && a[j]>key) {
        a[j+1] = a[j];
        --j;
    }
    a[j+1] = key;
}
```

Sorted Input Best `Θ(n)`, Average/Worst `Θ(n²)`; Auxiliary `Θ(1)`; **Stable**। Small/Nearly-sorted Input-এ কার্যকর।

{{WIDGET:sorting}}

## ৬.৬ Merge Sort

```text
MERGE_SORT(A)
    IF len(A) <= 1: RETURN A
    Split A into Left, Right
    RETURN MERGE(MERGE_SORT(Left), MERGE_SORT(Right))
```

`T(n)=2T(n/2)+Θ(n)` ⇒ Best/Average/Worst **Θ(n log n)**; Conventional Array Version Auxiliary **Θ(n)**, Stack `Θ(log n)` (buffer space dominates); **Stable** with correct merge tie handling।

## ৬.৭ Quick Sort

**Idea:** Pivot দিয়ে Array-কে Partition; Left-এর ছোট Values এবং Right-এর বড় Values (scheme-dependent), দুই ভাগে Recursion।

```text
QUICKSORT(A, lo, hi)
    IF lo >= hi: RETURN
    p = PARTITION(A, lo, hi)
    QUICKSORT(A, lo, p-1)
    QUICKSORT(A, p+1, hi)
```

Balanced Partitions ⇒ `Θ(n log n)`; Highly Unbalanced Partitions ⇒ `Θ(n²)` Worst। Typical randomized-pivot Quick Sort-এর **Expected `Θ(n log n)`** Time; In-place Partition সহ Recursive Stack **Expected `O(log n)`**, Naive Worst `O(n)`। Conventional Quick Sort **Unstable**।

## ৬.৮ Fibonacci: Naive Recursive vs Iterative vs Memoization

```c
int fibRecursive(int n) {
    if (n <= 1) return n;
    return fibRecursive(n-1) + fibRecursive(n-2);
}
```

**Naive Recursive**: Time `Θ(φⁿ)` (often upper-bounded by `O(2ⁿ)`); Stack `Θ(n)`। Repeated Calls অনেক বেশি।

{{DIAGRAM:fibtree}}

```c
long long fibIterative(int n) {
    if (n <= 1) return n;
    long long a=0, b=1;
    for (int i=2; i<=n; ++i) {
        long long next=a+b;
        a=b; b=next;
    }
    return b;
}
```

**Iterative**: Time `Θ(n)`, Extra Space `Θ(1)` (fixed-width integer ও arithmetic Cost O(1) ধরে; বড় n-এ Overflow হতে পারে)। Memoization: Time `Θ(n)`, Memo Storage `Θ(n)`, Recursive Stack `Θ(n)`।

{{WIDGET:recursion}}

## ৬.৯ Array & String Operations

| Operation | Typical Time | Auxiliary Space |
|---|---|---|
| Array Index Access | `Θ(1)` | `Θ(1)` |
| Array Traversal | `Θ(n)` | `Θ(1)` |
| Unsorted Array Linear Search | Best `Θ(1)`, Worst `Θ(n)` | `Θ(1)` |
| Insert at Front of Contiguous Array | `Θ(n)` shift | `Θ(1)` if capacity exists |
| Append to Dynamic Array | Amortized `O(1)` | Resizing can use `O(n)` |
| Reverse Mutable Array/String In-place | `Θ(n)` | `Θ(1)` |
| Copy String Length n | `Θ(n)` | `Θ(n)` for copy |
| Count Character Frequencies (fixed alphabet) | `Θ(n)` | `Θ(1)` for fixed alphabet |
| Build String by repeatedly copying immutable prefixes | `Θ(n²)` common naive pattern | Implementation-dependent |

## ৬.১০ Algorithm Comparison Table (Most Tested)

| Algorithm | Best Time | Average / Expected | Worst Time | Auxiliary Space | Stable? |
|---|---|---|---|---|---|
| Linear Search | Θ(1) | Θ(n) | Θ(n) | Θ(1) | N/A |
| Binary Search (iterative) | Θ(1) | Θ(log n) | Θ(log n) | Θ(1) | N/A |
| Bubble Sort (optimized) | Θ(n) | Θ(n²) | Θ(n²) | Θ(1) | Yes |
| Selection Sort | Θ(n²) | Θ(n²) | Θ(n²) | Θ(1) | Usually No |
| Insertion Sort | Θ(n) | Θ(n²) | Θ(n²) | Θ(1) | Yes |
| Merge Sort (array) | Θ(n log n) | Θ(n log n) | Θ(n log n) | Θ(n) | Yes |
| Quick Sort (randomized pivot) | Θ(n log n) | Expected Θ(n log n) | Θ(n²) | Stack: expected O(log n), worst O(n) | Usually No |
| Fibonacci (naive recursion) | By n: exponential | By n: exponential | Θ(φⁿ) | Θ(n) stack | N/A |
| Fibonacci (iteration) | By n: Θ(n) | Θ(n) | Θ(n) | Θ(1) | N/A |

**Comparability Note:** Fibonacci-এর Complexity-তে Input হলো `n`-এর Numeric Value; Bit-length of n বিবেচনা করলে Complexity Model বদলাবে। এখানে Conventional Introductory DSA Model ব্যবহার হয়েছে।

# ৭. Bangladesh Government IT Exam & Interview Preparation

> **Source disclosure:** নিচের প্রশ্নগুলো **এই গাইডের জন্য তৈরি অনুশীলনী**; যাচাইকৃত কোনো নির্দিষ্ট Bangladesh Government/Bank Past Paper হিসেবে দাবি করা হচ্ছে না।

## ৭.১ Written Exam-এর জন্য ছোট English Definitions

| Term | Concise exam-ready definition |
|---|---|
| Algorithm | A finite sequence of precise steps for solving a problem. |
| Time complexity | Asymptotic growth of operations with input size. |
| Space complexity | Asymptotic growth of memory requirement with input size. |
| Auxiliary space | Extra working memory excluding the input storage. |
| Big O | An asymptotic upper bound. |
| Big Omega | An asymptotic lower bound. |
| Big Theta | An asymptotically tight bound. |
| Best case | Minimum cost among inputs of the same size. |
| Worst case | Maximum cost among inputs of the same size. |
| Recursion | A technique in which a function calls itself, subject to a base case. |
| In-place algorithm | An algorithm using constant additional storage under the strict definition. |

## ৭.২ Short-answer Questions (Worked)

**Q1. Why is Binary Search faster than Linear Search on large sorted arrays?** Binary Search discards approximately half the remaining possibilities each step (`O(log n)` worst), whereas Linear Search may examine all n items (`O(n)` worst)। Sorted input এবং Direct Index Access প্রয়োজন।

**Q2. What is the difference between `O(n)` and `Θ(n)`?** `O(n)` শুধু Upper Bound; `Θ(n)` একই সঙ্গে Upper ও Lower Bound। যেমন `1 = O(n)` কিন্তু `1 ≠ Θ(n)`।

**Q3. Why is Merge Sort `O(n log n)`?** প্রায় log₂n স্তরের Divide Tree, প্রতিটি স্তরে মোট Θ(n) Merge Work; ফলে Θ(n log n) Time।

**Q4. What is amortized complexity?** Sequence of operations-এর মোট Cost ভাগ করে প্রতি Operation-এর গড় Guaranteed Bound; Dynamic Array Append-এর Amortized O(1), মাঝে মাঝে Resize O(n)। এটি Random Input-এর Average Case-এর সমার্থক নয়।

**Q5. What is the difference between stack space and heap space?** Recursion-related Active Function Frames সাধারণত Call Stack-এ থাকে; Dynamically allocated Arrays/Objects সাধারণত Heap/Managed Memory-তে থাকে। উভয়ই যথাযথ Space Analysis-এ বিবেচনা করতে হয়।

## ৭.৩ Code Output ও Calculation Practice

**Problem 1**
```c
for (int i=0; i<4; i++) printf("%d", i);
```
**Output:** `0123`; ৪টি Print। n কে Variable করলে Θ(n)।

**Problem 2**
```c
int s=0;
for (int i=1; i<=4; i++) s+=i;
printf("%d",s);
```
**Output:** `10`; n পর্যন্ত করলে Θ(n) Time, Θ(1) Auxiliary।

**Problem 3**
```c
for (int i=1; i<=16; i*=2) printf("%d ",i);
```
**Output:** `1 2 4 8 16`; Θ(log n) যদি Upper Limit n হয়।

**Problem 4**
```c
int c=0;
for (int i=0; i<4; i++)
  for (int j=0; j<i; j++) c++;
printf("%d",c);
```
**Output:** `6` (0+1+2+3); General Time Θ(n²)।

**Problem 5:** `T(n)=2T(n/2)+n` — **Θ(n log n)**। প্রতিটি স্তরের কাজ n; স্তর log n।

**Problem 6:** `T(n)=T(n/2)+1` — **Θ(log n)**; Input প্রতি Call-এ অর্ধেক।

**Problem 7:** `for(i=0;i<n;i++) for(j=0;j<m;j++) work();` — **Θ(nm)**, দুটি independent Dimension।

**Problem 8:** `for(i=1;i*i<=n;i++) work();` — **Θ(√n)**, কারণ i চলে প্রায় √n পর্যন্ত।

**Problem 9:** DFS Traversal for n-node Tree — **Θ(n)** Time, **O(h)** Recursive Stack।

**Problem 10:** BFS Traversal for n-node Tree — **Θ(n)** Time, **O(w)** Queue।

## ৭.৪ MCQ Bank, Difficulty ও Interactive Practice Test

HTML Guide-এর **MCQ Practice** Tab-এ Beginner / Intermediate / Advanced নির্বাচন করে উত্তর দিন। সঙ্গে সঙ্গে সঠিক/ভুল, কারণ, Score এবং Reset পাবেন। PDF-এর শেষে সম্পূর্ণ Question Bank ও Answer Key সংযুক্ত আছে।

## ৭.৫ Interview-oriented Questions (Quick Responses)

1. **Why is O(n log n) often desirable for sorting?** Comparison-based sorting has an Ω(n log n) Worst-case Lower Bound in the comparison model; Merge Sort achieves Θ(n log n)।
2. **Can an O(n²) Algorithm outperform O(n log n)?** নির্দিষ্ট ছোট n এবং Constant Factor-এ পারে; Asymptotic Class একা Benchmark নয়।
3. **Why is Hash Lookup not guaranteed O(1)?** Worst-case Collision Pattern-এ many keys একই Bucket-এ পড়ে O(n) পর্যন্ত হতে পারে (Implementation-এর ওপর নির্ভর করে)।
4. **What is the memory cost of recursive Binary Search?** Θ(log n) Stack, unless TCO/Optimization assumption explicitly given।
5. **Does in-place always mean faster?** না; Memory কমতে পারে, কিন্তু Operation/Cache Behavior/Algorithm ভিন্ন।
6. **What if input is two dimensional?** n এবং m যথাযথভাবে ধরে `Θ(nm)` বা `Θ(V+E)`-এর মতো Bound লিখতে হবে।

# ৮. Final Revision Sheet — One-Page Exam Checklist

> **Before writing the answer:** Input Size চিহ্নিত করুন → Main Operation Count করুন → Worst/Average/Best Case আলাদা করুন → Dominant Term নিন → Auxiliary Space লিখুন।

## ৮.১ Formula Flashcards

| Code Pattern / Idea | Time (Typical) | Memory Reminder |
|---|---|---|
| `a[k]` | `Θ(1)` | `Θ(1)` extra |
| `for i=0..n−1` | `Θ(n)` | loop scalar `Θ(1)` |
| `i *= 2` | `Θ(log n)` | `Θ(1)` |
| Two independent length-n loops | `Θ(n)` | `Θ(1)` |
| Fully nested n×n loops | `Θ(n²)` | `Θ(1)` if only scalars |
| Outer n, inner log n | `Θ(n log n)` | `Θ(1)` if only scalars |
| Triple nested n×n×n | `Θ(n³)` | `Θ(1)` if only scalars |
| Array copy | `Θ(n)` | `Θ(n)` new array |
| Recursive linear chain | `Θ(n)` | `Θ(n)` stack |
| Balanced Tree DFS | `Θ(n)` | `O(log n)` stack |
| Skewed Tree DFS | `Θ(n)` | `O(n)` stack |
| Tree BFS | `Θ(n)` | `O(w)` queue |
| Binary Search iterative | `Θ(log n)` worst | `Θ(1)` |
| Merge Sort | `Θ(n log n)` | `Θ(n)` |
| Quick Sort | Expected `Θ(n log n)` randomized | Expected `O(log n)` stack |

## ৮.২ Rapid Memory Hooks

- **Constant:** Input বড় হলেও Direct Access-এর ধাপ স্থির।
- **Linear:** প্রতিটি Element একবার।
- **Logarithmic:** প্রতিবার অর্ধেক / নির্দিষ্ট Ratio-তে কমে।
- **Quadratic:** প্রায় সব জোড়ার Comparison।
- **Recursive Space:** সর্বোচ্চ Simultaneously Active Call Count।
- **Time বনাম Space:** Operation Count আর Memory Count এক জিনিস নয়।
- **Big O বনাম Θ:** Upper Bound বনাম Tight Bound।
- **Exam Safeguard:** Worst/Expected/Amortized শব্দগুলো বাদ দেবেন না।

<details><summary>Suggested 30-minute Revision Plan</summary>
৫ মিনিট: Big O/Ω/Θ + Growth Ordering। ১০ মিনিট: ৮টি Loop/Recursion Pattern। ৫ মিনিট: ৭টি Sort/Search Algorithm Complexity Table। ১০ মিনিট: Advanced MCQ ও ভুলগুলো পুনরায় দেখুন।
</details>
