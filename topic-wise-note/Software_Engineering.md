<h1 align="center">TOPIC - Software Engineering</h1> <br>

# Question 01. Assume a banking application wants to add a fingerprint system for their App. Write one functional requirement and one security requirement.

## Banking App-এ Fingerprint System: Requirements (Exam Short Note)

## আগে মূল ধারণা

| | Functional Requirement (FR) | Non-Functional Requirement (NFR) |
|---|---|---|
| **মানে** | System **কী করবে** (feature/behavior) | System **কেমন হবে** (quality/constraint) |
| **প্রশ্ন** | "System কী কাজ করবে?" | "কাজটা কতটা ভালো/নিরাপদ/দ্রুত?" |
| **উদাহরণ** | Login, Fund Transfer | Security, Performance, Usability |

> **Security Requirement** একটি **Non-Functional Requirement (NFR)**।

**ভালো Requirement-এর বৈশিষ্ট্য:** Clear, Specific, **Measurable, Testable**, Unambiguous, Feasible। লেখার সময় **"shall"** শব্দ ব্যবহার করা হয়।

---

## ১. Functional Requirement (FR)

> **FR-01:** The system **shall** allow a registered user to log in to the banking app by scanning their fingerprint using the device's fingerprint sensor, and **shall** grant access to the user's account dashboard if the scanned fingerprint matches the enrolled fingerprint.

**সহজ বাংলায়:** ব্যবহারকারী fingerprint scan করলে এবং তা আগে register করা fingerprint-এর সাথে মিললে app-এর dashboard খুলে যাবে।

**কেন এটি Functional?** কারণ এটি system-এর একটি **নির্দিষ্ট কাজ (login feature)** বর্ণনা করছে।

---

## ২. Security Requirement (Non-Functional)

> **SR-01:** The system **shall** store the user's fingerprint data **only in encrypted form (AES-256)** on the device's secure hardware, **shall not** transmit raw fingerprint data over the network, and **shall** lock fingerprint login for **15 minutes** after **5 consecutive failed attempts**, requiring PIN/password instead.

**সহজ বাংলায়:** Fingerprint data encrypt করে device-এর secure জায়গায় রাখা হবে, network-এ পাঠানো হবে না, আর ৫ বার ভুল হলে ১৫ মিনিটের জন্য fingerprint login বন্ধ হয়ে PIN লাগবে।

**কেন Measurable?** কারণ এতে নির্দিষ্ট সংখ্যা আছে: **AES-256, ৫ বার, ১৫ মিনিট**, যা test করে যাচাই করা যায়।

---

## Diagram: Fingerprint Login Flow

```
   User
    │  ① Fingerprint scan
    ▼
┌─────────────────┐
│ Fingerprint     │
│ Sensor (Device) │
└────────┬────────┘
         │ ② Template তৈরি
         ▼
┌─────────────────────────┐
│ Secure Storage          │  ← SR-01: Encrypted, শুধু device-এ
│ (Match with enrolled)   │
└────────┬────────────────┘
         │
    ┌────┴─────┐
    ▼          ▼
 Match ✅    No Match ❌
    │          │
    ▼          ▼
Dashboard   Failed count +1
(FR-01)     (৫ বার হলে Lock, SR-01)
```

---

## FR vs Security Requirement: নিজের লেখার ছক

| বিষয় | FR-01 | SR-01 |
|---|---|---|
| **ধরন** | Functional | Non-Functional (Security) |
| **বর্ণনা করে** | Login কাজটি | Data-র সুরক্ষা |
| **মূল শব্দ** | allow, grant access | encrypted, shall not transmit, lock |
| **Test-এর উপায়** | সঠিক fingerprint দিলে dashboard খোলে কিনা | ৫ বার ভুলের পর lock হয় কিনা |

---

## আরও কিছু Example (MCQ ও Written-এর জন্য)

**Functional Requirement:**
- User fingerprint **enroll (register)** করতে পারবে
- User fingerprint login বন্ধ করে **PIN-এ ফিরে যেতে** পারবে
- Fingerprint match না হলে **error message** দেখাবে

**Security Requirement:**
- **Biometric data** কখনো server-এ plain text-এ থাকবে না
- Fund transfer-এর আগে **re-authentication** লাগবে
- Session **৫ মিনিট idle** থাকলে auto logout

---

## মনে রাখার মতো তথ্য

- Security = **NFR**, Login/Transfer = **FR**
- NFR-এর অন্য ধরন: **Performance, Usability, Reliability, Portability**
- Security-র তিন মূল স্তম্ভ: **CIA = Confidentiality, Integrity, Availability**
- Biometric ব্যবহার করা হয় **Authentication** (তুমি কে তা প্রমাণ)-এর জন্য, **Authorization** (তুমি কী করতে পারো) নয়
- খারাপ requirement: "System **should be** secure" (অস্পষ্ট, মাপা যায় না)
- ভালো requirement: "**৫ বার** ভুলে **১৫ মিনিট** lock" (নির্দিষ্ট, test করা যায়)

---

## পরীক্ষার টিপস ✍️

- আগে **FR ও NFR-এর পার্থক্য** এক লাইনে লিখবে, এরপর requirement দুটি লিখবে
- দুটোতেই **"shall"** ব্যবহার করবে
- Security requirement-এ **সংখ্যা/মান** (AES-256, ৫ বার, ১৫ মিনিট) দিলে সেটি **measurable** হয়, এতে বেশি নম্বর
- লিখে দেবে কেন FR-টি functional আর SR-টি non-functional, এতে যুক্তি পূর্ণ হয়
- ছোট একটি flow diagram এঁকে দিলে answer আরও শক্তিশালী হয়


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


# Question 02. What is Version Control (e.g., Git)? Explain the specific difference between "Committing" code and "Pushing" code.

# Version Control ও Git: Commit vs Push (Exam Short Note)

## Version Control কী?

**সংজ্ঞা:** Version Control System (VCS) এমন একটি system, যা **source code-এর প্রতিটি পরিবর্তনের history সংরক্ষণ করে**, ফলে দরকার হলে **আগের যেকোনো version-এ ফিরে যাওয়া** যায় এবং **একাধিক developer একসাথে** কাজ করতে পারে।

**উদাহরণ:** Word-এ "Report_final", "Report_final2", "Report_final_FINAL" নামে file বানানোর ঝামেলা VCS নিজেই সামলায়।

### Version Control-এর সুবিধা

- **History tracking:** কে, কখন, কী বদলেছে জানা যায়
- **Backup ও Recovery:** ভুল হলে আগের version-এ ফেরা যায়
- **Collaboration:** অনেকে একসাথে কাজ করতে পারে
- **Branching:** আলাদা branch-এ নতুন feature বানিয়ে পরে merge করা যায়

### VCS-এর ধরন

| ধরন | বর্ণনা | উদাহরণ |
|---|---|---|
| **Local** | শুধু নিজের computer-এ | RCS |
| **Centralized (CVCS)** | একটি central server | SVN, CVS |
| **Distributed (DVCS)** | প্রত্যেকের কাছে **পুরো repository-র কপি** | **Git**, Mercurial |

---

## Git কী?

**Git** একটি **Distributed Version Control System**, যা **Linus Torvalds** ২০০৫ সালে বানান (Linux kernel-এর জন্য)। **GitHub, GitLab, Bitbucket** হলো Git repository **host করার online platform**। Git আর GitHub এক জিনিস নয়।

---

## Git-এর চার জায়গা (Diagram)

```
 তোমার Computer                                    Internet
┌─────────────────────────────────────────────┐   ┌──────────────┐
│                                             │   │              │
│ Working     Staging Area     Local          │   │   Remote     │
│ Directory ─► (Index)   ───► Repository ─────┼──►│  Repository  │
│ (file edit)  (প্রস্তুত)     (history সেভ)    │   │ (GitHub)     │
│                                             │   │              │
└─────────────────────────────────────────────┘   └──────────────┘
      git add          git commit           git push
```

---

## Commit বনাম Push

### Commit (`git commit`)

**সংজ্ঞা:** Staged পরিবর্তনগুলোকে **নিজের computer-এর Local Repository**-তে একটি **snapshot (সংরক্ষিত বিন্দু)** হিসেবে সেভ করা।

- **কোথায় হয়:** শুধু **নিজের computer-এ (local)**
- **Internet লাগে?** **না**
- **অন্যরা দেখতে পায়?** **না**
- প্রতিটি commit-এর একটি unique **hash ID** ও **message** থাকে

### Push (`git push`)

**সংজ্ঞা:** Local Repository-র commit গুলোকে **Remote Repository (যেমন GitHub)**-এ **পাঠিয়ে দেওয়া**।

- **কোথায় হয়:** Local থেকে **Remote-এ**
- **Internet লাগে?** **হ্যাঁ**
- **অন্যরা দেখতে পায়?** **হ্যাঁ**, push-এর পর

---

## তুলনামূলক ছক

| বিষয় | **Commit** | **Push** |
|---|---|---|
| **কাজ** | পরিবর্তন local-এ সেভ করা | Local commit remote-এ পাঠানো |
| **Command** | `git commit -m "message"` | `git push origin main` |
| **কোথায় সেভ হয়** | Local Repository | Remote Repository |
| **Internet** | লাগে না | লাগে |
| **অন্যরা দেখে?** | না | হ্যাঁ |
| **আগে কী লাগে** | `git add` (staging) | অন্তত একটি commit |
| **Offline করা যায়?** | হ্যাঁ | না |
| **এক লাইনে** | নিজের জন্য সেভ | সবার জন্য শেয়ার |

---

## Example (Step by Step)

```bash
# ১. Repository শুরু
git init

# ২. File বানানো/বদলানো হলো
echo "Hello" > index.html

# ৩. Staging Area-তে যোগ করো
git add index.html

# ৪. Local-এ Commit করো
git commit -m "Add index page"

# ৫. Remote-এ Push করো
git push origin main
```

**ঘটনার ক্রম:**

```
index.html বদলাও
      │ git add
      ▼
  Staged ✔
      │ git commit
      ▼
 Local-এ সেভ (এখনো শুধু তোমার কাছে)
      │ git push
      ▼
 GitHub-এ পৌঁছালো (এখন সবাই দেখতে পারবে)
```

**বাস্তব উদাহরণ:** Commit হলো **Word file-এ "Save" করা** (নিজের computer-এ)। Push হলো সেই file **Google Drive-এ upload করে বন্ধুদের শেয়ার করা**।

---

## মনে রাখার মতো তথ্য

- Git = **Distributed VCS**, বানিয়েছেন **Linus Torvalds (২০০৫)**
- Git আর GitHub **আলাদা**: Git হলো tool, GitHub হলো hosting service
- **Commit আগে, Push পরে**: commit ছাড়া push করার কিছু থাকে না
- Commit **offline-এও** করা যায়, Push-এ **internet লাগে**
- Staging Area-র আরেক নাম **Index**
- Push-এর আগে remote-এ নতুন কিছু থাকলে **rejected** হতে পারে, তখন আগে `git pull` করতে হয়

---

## পরীক্ষার টিপস ✍️

- আগে **Version Control-এর সংজ্ঞা ও সুবিধা** লিখবে, তারপর Commit-Push
- মূল পার্থক্য এক লাইনে: **"Commit local-এ সেভ করে, Push সেই commit remote-এ পাঠায়"**
- **তিন ধাপের diagram** (Working → Staging → Local → Remote) অবশ্যই আঁকবে
- **Comparison table** দিলে সবচেয়ে বেশি নম্বর
- `add → commit → push` এই **ক্রম** লিখতে ভুলবে না
- Extra নম্বরের জন্য mention করবে: **Distributed হওয়ায় Git-এ internet ছাড়াও commit করা যায়**, যা SVN-এ সম্ভব নয়


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


# Question 03. Which system did you build for a real-life software project? What problems you faced during that time and how to solve this?


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>

# Question 04. Given the following values, compute function point when all complexity adjustment factor (CAF) and weighting factors are average: User Input = 50; User Output = 40; User Inquiries = 35; User Files = 6; External Interface = 4.

# Function Point (FP) Calculation

## Formula

```
FP = UFP × CAF

UFP = Σ (Count × Weighting Factor)
CAF = 0.65 + 0.01 × ΣFi
```

**Average weighting factor:**

| Component | Average Weight |
|---|---|
| User Input (EI) | **4** |
| User Output (EO) | **5** |
| User Inquiry (EQ) | **4** |
| User Files / Internal Logical File (ILF) | **10** |
| External Interface (EIF) | **7** |

---

## Step 1: Unadjusted Function Point (UFP)

| Component | Count | Weight | Count × Weight |
|---|---|---|---|
| User Input | 50 | 4 | **200** |
| User Output | 40 | 5 | **200** |
| User Inquiry | 35 | 4 | **140** |
| User Files | 6 | 10 | **60** |
| External Interface | 4 | 7 | **28** |
| | | **UFP =** | **628** |

---

## Step 2: Complexity Adjustment Factor (CAF)

"Average" মানে **14টি factor-এর প্রতিটির মান = 3**।

```
ΣFi = 14 × 3 = 42

CAF = 0.65 + 0.01 × 42
    = 0.65 + 0.42
    = 1.07
```

---

## Step 3: Function Point

```
FP = UFP × CAF
   = 628 × 1.07
   = 671.96
   ≈ 672
```

## ✅ Answer: **FP ≈ 672**

---

## মনে রাখার মতো তথ্য

- **৫টি component:** EI, EO, EQ, ILF, EIF। প্রশ্নের "User Files" = **ILF**, "External Interface" = **EIF**
- **Average weight মুখস্থ:** **4, 5, 4, 10, 7** (EI, EO, EQ, ILF, EIF ক্রমে)
- **Simple / Average / Complex weight:**

| Component | Simple | Average | Complex |
|---|---|---|---|
| EI | 3 | 4 | 6 |
| EO | 4 | 5 | 7 |
| EQ | 3 | 4 | 6 |
| ILF | 7 | 10 | 15 |
| EIF | 5 | 7 | 10 |

- **CAF = 0.65 + 0.01 × ΣFi**, মোট **14টি** factor, প্রতিটির মান **0 থেকে 5**
- সব factor average (3) হলে **ΣFi = 42, CAF = 1.07**
- CAF-এর সর্বনিম্ন মান **0.65** (ΣFi = 0), সর্বোচ্চ **1.35** (ΣFi = 70)
- Function Point **language-independent**, অর্থাৎ কোন programming language ব্যবহার হবে তার উপর নির্ভর করে না

---

## পরীক্ষার টিপস ✍️

- আগে **formula লিখবে**, তারপর **table বানিয়ে UFP** বের করবে
- "Average" দেখলে সাথে সাথে **weight (4,5,4,10,7)** আর **ΣFi = 42** লিখবে
- শেষে **FP = 671.96 ≈ 672** লিখবে, আর **unit (FP)** দিতে ভুলবে না
- প্রশ্নে CAF-এর মান আলাদা দেওয়া থাকলে সেটাই ব্যবহার করবে, নিজে হিসাব করবে না

<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>
