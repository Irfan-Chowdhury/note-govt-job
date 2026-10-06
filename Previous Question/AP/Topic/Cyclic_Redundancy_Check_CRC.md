## Topic

**Computer Networks / Data Communication → Error Detection → CRC (Cyclic Redundancy Check)**


## 1. CRC কী?

CRC = **Cyclic Redundancy Check**

এটা হলো একটা **Error Detection Technique**।

মানে sender যখন data পাঠাবে, তখন data-এর সাথে কিছু extra bit যোগ করে পাঠায়। Receiver সেই extra bit use করে check করে:

> transmission-এর সময় data change/corrupt হয়েছে কি না।

---

## 2. CRC is a redundancy error technique used to determine the error. Suppose the original data is `11100` and the divisor is `1001`.


## 2. Question-এ কী দেওয়া আছে?

Original Data:

```text
11100
```

Divisor:

```text
1001
```

এখানে divisor-কে অনেক সময় **Generator**-ও বলা হয়।

---

## 3. কেন 3টা zero add করলাম?

Divisor হলো:

```text
1001
```

এর length = 4 bits।

Rule:

$$
\text{Number of zeros} = \text{Divisor length} - 1
$$

So,

$$
4-1=3
$$

তাই original data `11100`-এর শেষে 3টা zero:

```text
11100000
```

---

## 4. CRC division সাধারণ division না

CRC-তে normal subtraction করা হয় না।

এখানে use হয়:

**XOR operation**

XOR rules:

| A | B | XOR |
| - | - | --- |
| 0 | 0 | 0   |
| 0 | 1 | 1   |
| 1 | 0 | 1   |
| 1 | 1 | 0   |

সহজে মনে রাখো:

> **Same হলে 0, Different হলে 1**

---

## 5. Division করলে

আমরা divide করব:

```text
11100000
```

by:

```text
1001
```

Modulo-2/XOR division শেষে remainder পাওয়া যায়:

```text
111
```

এই remainder-টাই হলো:

$$
\boxed{CRC = 111}
$$

---

## 6. Sender কী পাঠাবে?

Original data:

```text
11100
```

CRC:

```text
111
```

একসাথে:

```text
11100111
```

এটাই transmitted codeword।

---

## 7. Receiver কীভাবে Error Detect করবে?

Receiver `11100111` পাবে।

তারপর আবার divisor `1001` দিয়ে divide করবে।

যদি remainder হয়:

```text
000
```

তাহলে সাধারণভাবে ধরা হয়:

> **No error detected**

আর যদি remainder non-zero হয়, যেমন:

```text
101
```

তাহলে:

> **Error detected**

---

### Exam Memory Trick

**CRC steps:**

```text
Data
 ↓
Append (divisor length - 1) zeros
 ↓
XOR Division
 ↓
Remainder = CRC
 ↓
Data + CRC = Codeword
```

এই question-এর shortcut:

```text
Data     = 11100
Divisor  = 1001
Zeros    = 3
Dividend = 11100000
CRC      = 111
Codeword = 11100111
```

$$
\boxed{\text{Final Answer: CRC = 111}}
$$
