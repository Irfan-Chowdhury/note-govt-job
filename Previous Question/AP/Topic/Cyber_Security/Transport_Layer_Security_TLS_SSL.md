### First Format — Exam Answer

**Topic:** Cyber Security → Transport Layer Security (TLS/SSL) → Public Key Cryptography

**Answer:**
If an attacker steals a website’s **private key**, the attacker may **impersonate the website**, perform **Man-in-the-Middle (MITM) attacks**, and potentially decrypt TLS traffic. However, previously captured sessions using **Forward Secrecy (ECDHE/DHE)** cannot normally be decrypted using the stolen private key alone.

---

### Second Format — Basic Explanation in Bangla

#### 1. TLS কী?

**TLS (Transport Layer Security)** হলো এমন একটি security protocol যা browser এবং web server-এর মধ্যে data-কে **encrypted** করে পাঠায়।

যেমন:

`User/Browser → HTTPS/TLS → Website Server`

আপনি যখন `https://` website ব্যবহার করেন, তখন সাধারণত TLS ব্যবহার হয়।

এর প্রধান কাজ:

* **Confidentiality** → অন্য কেউ data পড়তে পারবে না
* **Authentication** → সঠিক website-এর সাথেই communication হচ্ছে কিনা যাচাই করা
* **Integrity** → মাঝপথে data পরিবর্তন হয়েছে কিনা নিশ্চিত করা

---

#### 2. Public Key এবং Private Key

TLS certificate-এ সাধারণত একটি **Public Key** থাকে এবং server-এর কাছে গোপনে থাকে **Private Key**।

সহজভাবে:

```text
Public Key  → সবাই জানতে পারে
Private Key → শুধু Website/Server-এর কাছে থাকা উচিত
```

Private key হলো অত্যন্ত sensitive।

---

#### 3. Attacker Private Key চুরি করলে কী করতে পারে?

ধরুন,

```text
Real Website
     ↓
Private Key
     ↓
Attacker stole it
```

তাহলে attacker কয়েকটি গুরুত্বপূর্ণ attack করতে পারে।

**① Website Impersonation**

Attacker website-এর পরিচয় নকল করার চেষ্টা করতে পারে।

অর্থাৎ attacker নিজেকে legitimate server হিসেবে উপস্থাপন করতে পারে।

```text
User
 ↓
Fake Server (Attacker)
 ↓
Uses stolen Private Key
```

এটি **Server Impersonation**-এর ঝুঁকি তৈরি করে।
আক্রমণকারী কোনো website-এর private key চুরি করে এবং সেই key ব্যবহার করে আসল website-এর মতো পরিচয় দেওয়ার চেষ্টা করলে সেটিকে impersonation বলা হয়।

---

**② Man-in-the-Middle (MITM) Attack**

Attacker যদি user এবং server-এর communication-এর মাঝখানে থাকতে পারে, তাহলে সে traffic intercept করার চেষ্টা করতে পারে।

```text
User
  ↓
Attacker
  ↓
Real Website
```

এটিই **Man-in-the-Middle Attack**।

Private key compromised হলে এই ধরনের attack-এর ঝুঁকি অনেক বেড়ে যায়।

---

**③ Encrypted Data Decryption — কিছু ক্ষেত্রে**

পুরনো TLS configuration-এ যদি **RSA key exchange** ব্যবহার করা হয়ে থাকে এবং attacker আগের encrypted traffic capture করে রাখে, stolen private key দিয়ে সেই traffic decrypt করা সম্ভব হতে পারে।

কিন্তু modern TLS-এ সাধারণত **DHE/ECDHE** ব্যবহার করা হয়।

এগুলো **Forward Secrecy** দেয়।

তাই:

```text
ECDHE/DHE + Forward Secrecy
        ↓
Private key stolen
        ↓
Old recorded sessions normally remain secure
```

অর্থাৎ **private key চুরি হলেই সব পুরনো HTTPS traffic decrypt করা যাবে—এটা সবসময় সত্য নয়।**

---

### Forward Secrecy কী?

Forward Secrecy-এর মূল ধারণা:

> Server-এর long-term private key ভবিষ্যতে চুরি হলেও আগের session-এর encryption key recover করা যাবে না।

Modern TLS-এর জন্য এটি খুব গুরুত্বপূর্ণ।

---

### Govt Job Exam-এর জন্য মনে রাখুন

**Private Key compromised →**

**Impersonation + MITM + possible decryption**

Shortcut:

> **Private Key = Identity + Security Secret**

Private key চুরি হলে website-এর **identity/authentication** এবং কিছু ক্ষেত্রে **confidentiality** দুটোই ঝুঁকিতে পড়ে।
