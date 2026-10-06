<h1 align="center">TOPIC 10 - Digital Logic</h1> <br>

## Question 01. What is a Universal Gate? Prove that the NAND Gate is a Universal Gate.

# Universal Gate ও NAND Gate (Exam Short Note)

## Universal Gate কী?

**যে gate শুধু নিজেকে (একা) ব্যবহার করে AND, OR, NOT তিনটি basic gate বানানো যায়, তাকে Universal Gate বলে।**

কারণ যেকোনো digital circuit শুধু AND, OR, NOT দিয়ে বানানো যায়। তাই এই তিনটি বানাতে পারলে **যেকোনো logic circuit** বানানো সম্ভব।

**Universal Gate মাত্র দুটি:** **NAND** ও **NOR**।

---

## NAND Gate-এর পরিচিতি

**NAND = NOT + AND।** AND-এর output উল্টে দেয়।

```
Boolean: Y = (A · B)'

Symbol:   A ──┐
              │D○── Y
          B ──┘
```

**Truth Table:**

| A | B | Y = (A·B)' |
|---|---|---|
| 0 | 0 | **1** |
| 0 | 1 | **1** |
| 1 | 0 | **1** |
| 1 | 1 | **0** |

**মনে রাখার নিয়ম:** দুই input-ই 1 হলে output 0, বাকি সব ক্ষেত্রে 1।

---

## Proof: NAND দিয়ে NOT, AND, OR বানানো

### ১. NOT Gate (NAND দিয়ে)

**দুই input একসাথে জুড়ে দাও।**

```
A ──┬──┐
    │  │D○── Y = A'
    └──┘
```

**Proof:** `Y = (A · A)' = A'` (কারণ A·A = A)

| A | A NAND A |
|---|---|
| 0 | 1 |
| 1 | 0 |

এটাই NOT gate-এর truth table ✅

---

### ২. AND Gate (NAND দিয়ে)

**দুটি NAND লাগে:** প্রথমটি NAND, দ্বিতীয়টি NOT হিসেবে।

```
A ──┐
    │D○──┬──┐
B ──┘    │  │D○── Y = A·B
         └──┘
```

**Proof:**
```
প্রথম NAND:   X = (A·B)'
দ্বিতীয় NAND (NOT): Y = (X·X)' = X' = ((A·B)')' = A·B
```

| A | B | (A·B)' | Y = ((A·B)')' |
|---|---|---|---|
| 0 | 0 | 1 | **0** |
| 0 | 1 | 1 | **0** |
| 1 | 0 | 1 | **0** |
| 1 | 1 | 0 | **1** |

এটাই AND gate ✅

---

### ৩. OR Gate (NAND দিয়ে)

**তিনটি NAND লাগে:** আগে A ও B আলাদাভাবে NOT করো, তারপর NAND করো।

```
A ──┬──┐
    │  │D○── A' ──┐
    └──┘          │
                  │D○── Y = A + B
B ──┬──┐          │
    │  │D○── B' ──┘
    └──┘
```

**Proof (De Morgan's Theorem ব্যবহার করে):**
```
Y = (A' · B')'
  = (A')' + (B')'      ← De Morgan: (X·Y)' = X' + Y'
  = A + B  ✅
```

| A | B | A' | B' | Y = (A'·B')' |
|---|---|---|---|---|
| 0 | 0 | 1 | 1 | **0** |
| 0 | 1 | 1 | 0 | **1** |
| 1 | 0 | 0 | 1 | **1** |
| 1 | 1 | 0 | 0 | **1** |

এটাই OR gate ✅

---

## সারসংক্ষেপ ছক

| Gate | NAND দিয়ে বানানো | NAND সংখ্যা | Boolean Proof |
|---|---|---|---|
| **NOT** | দুই input জুড়ে দাও | **1** | (A·A)' = A' |
| **AND** | NAND + NOT | **2** | ((A·B)')' = A·B |
| **OR** | A', B' তারপর NAND | **3** | (A'·B')' = A+B |

---

## Conclusion

NAND gate দিয়ে **NOT, AND, OR** তিনটিই বানানো গেল। যেহেতু এই তিনটি দিয়ে যেকোনো logic circuit তৈরি করা যায়, তাই **NAND একটি Universal Gate** ∎

**For Details Check ICT BOOK of HSC**

---

## পরীক্ষার টিপস ✍️

- আগে **Universal Gate-এর সংজ্ঞা** লিখবে, তারপর proof দেবে।
- **তিনটি gate-এরই diagram ও truth table** আঁকবে (NOT, AND, OR)। একটা বাদ গেলে proof অসম্পূর্ণ।
- OR-এর proof-এ **De Morgan's Theorem** অবশ্যই লিখবে: **(A·B)' = A' + B'**
- **NAND সংখ্যা মনে রাখবে:** NOT = 1, AND = 2, OR = 3।
- Extra নম্বরের জন্য লিখবে: **NOR-ও Universal Gate** (একই পদ্ধতিতে প্রমাণ করা যায়)।
- NAND-কে বেশি ব্যবহার করা হয় কারণ এটি **কম জায়গা নেয় ও সস্তা** (CMOS technology-তে বানানো সহজ)।
