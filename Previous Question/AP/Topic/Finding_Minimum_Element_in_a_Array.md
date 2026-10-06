## First Format: Exam Answer

### Topic:

**Data Structure / Programming → Array Traversal and Searching → Finding Minimum Element in an Array**

### C Function to Find Smallest Element from an Array

```c
#include <stdio.h>

int findSmallest(int arr[], int n)
{
    int smallest = arr[0];

    for(int i = 1; i < n; i++)
    {
        if(arr[i] < smallest)
        {
            smallest = arr[i];
        }
    }

    return smallest;
}

int main()
{
    int arr[] = {5, 2, 8, 1, 9};
    int n = 5;

    printf("Smallest element = %d", findSmallest(arr, n));

    return 0;
}
```

### Output:

```
Smallest element = 1
```

---

# Second Format: Basic Explanation (Bangla + English)

## Topic: Array Traversal

এই question-এ বলা হয়েছে:

> একটি array থেকে সবচেয়ে ছোট value (minimum element) বের করতে হবে।

Example:

```text
Array = {5, 2, 8, 1, 9}
```

এখানে smallest number হলো:

```
1
```

---

## Logic কী?

আমরা প্রথম element-কে temporarily smallest ধরে নেই।

মানে:

```c
smallest = arr[0];
```

Array:

```
Index:   0  1  2  3  4
Value:   5  2  8  1  9
```

প্রথমে:

```
smallest = 5
```

---

তারপর একে একে সব element check করবো।

### Step 1:

Compare:

```
2 < 5 ?
```

হ্যাঁ।

তাই:

```
smallest = 2
```

---

### Step 2:

Compare:

```
8 < 2 ?
```

না।

কোনো change হবে না।

---

### Step 3:

Compare:

```
1 < 2 ?
```

হ্যাঁ।

তাই:

```
smallest = 1
```

---

### Step 4:

Compare:

```
9 < 1 ?
```

না।

শেষে:

```
smallest = 1
```

---

## Function Explanation

```c
int findSmallest(int arr[], int n)
```

মানে:

* `arr[]` → array receive করবে
* `n` → array-এর size
* return করবে smallest value

---

## Loop কেন ব্যবহার করেছি?

কারণ array-এর সব element check করতে হবে।

```c
for(int i = 1; i < n; i++)
```

এখানে:

* শুরু করেছি `1` থেকে কারণ `arr[0]` already smallest ধরে নিয়েছি।
* শেষ পর্যন্ত সব element compare হবে।

---

## Time Complexity

Array-এর প্রতিটি element একবার করে check হয়।

তাই:

$$
\boxed{O(n)}
$$

Space Complexity:

$$
\boxed{O(1)}
$$

কারণ extra কোনো array ব্যবহার করা হয়নি।

---

### Exam-এর জন্য মনে রাখার সহজ নিয়ম:

**Find Minimum Algorithm:**

1. প্রথম element কে minimum ধরো
2. Remaining elements compare করো
3. ছোট পেলে minimum update করো
4. শেষে minimum return করো

Pseudo Code:

```
min = array[0]

for each element:
    if element < min:
        min = element

return min
```

এটি Assistant Programmer exam-এর জন্য খুব common **Basic Array Problem**।
