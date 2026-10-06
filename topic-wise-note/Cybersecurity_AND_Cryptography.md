<h1 align="center">TOPIC - Cybersecurity & Cryptography</h1> <br>
 
 # Question: Difference between spoofing and sniffing.

 # Spoofing বনাম Sniffing

## সংজ্ঞা

**Spoofing:** আক্রমণকারী **নিজের পরিচয় গোপন করে অন্য কারো (বিশ্বস্ত device/user/website) পরিচয় ধারণ করে** সিস্টেমকে ধোঁকা দেয়। এটি একটি **active attack**।

**Sniffing:** আক্রমণকারী network দিয়ে **চলাচল করা data packet চুপিচুপি ধরে পড়ে** (capture ও analyze করে)। এটি সাধারণত একটি **passive attack**।

---

## Diagram

```
        Spoofing                              Sniffing

 Attacker (নকল পরিচয়)                  Sender ───────────► Receiver
    │ "আমি তোমার Bank"                          │ data
    ▼                                          ▼
  Victim ── বিশ্বাস করে                    [Attacker] ← packet ধরে পড়ে
  তথ্য/টাকা পাঠায়                          (কেউ টের পায় না)
```

**Example:**
- **Spoofing:** নকল ব্যাংকের email/website বানিয়ে ব্যবহারকারীর password নেওয়া।
- **Sniffing:** Public Wi-Fi-তে অন্যের unencrypted login data ধরে ফেলা।

---

## তুলনামূলক ছক

| বিষয় | **Spoofing** | **Sniffing** |
|---|---|---|
| **মূল কাজ** | ভুয়া পরিচয় ধারণ (impersonation) | Data চুরি করে পড়া (eavesdropping) |
| **Attack-এর ধরন** | **Active** (সক্রিয়ভাবে কিছু পাঠায়) | **Passive** (শুধু শোনে/ধরে) |
| **Data পরিবর্তন করে?** | হ্যাঁ, নকল data পাঠায় | না, শুধু পড়ে |
| **লক্ষ্য** | বিশ্বাস ভাঙা, অনুমতি আদায় | তথ্য সংগ্রহ (password, message) |
| **Security-র কোন দিক ভাঙে** | **Authentication** ও Integrity | **Confidentiality** |
| **ধরা সহজ?** | তুলনামূলক সহজ | কঠিন (কোনো চিহ্ন থাকে না) |
| **ধরন/Example** | IP, Email, DNS, ARP, MAC Spoofing | Packet sniffing (Wireshark), Wi-Fi sniffing |
| **প্রতিরোধ** | Packet filtering, SPF/DKIM, MFA | **Encryption (HTTPS, VPN, SSL/TLS)** |

---

## মনে রাখার মতো তথ্য

- Spoofing = **নকল পরিচয়**, Sniffing = **চুপিচুপি শোনা**
- Spoofing ভাঙে **Authentication**, Sniffing ভাঙে **Confidentiality**
- Spoofing-এর ধরন: **IP, Email, DNS, ARP, MAC, Caller ID**
- Sniffing-এর জনপ্রিয় tool: **Wireshark, tcpdump**
- Sniffing ঠেকানোর সবচেয়ে ভালো উপায় **Encryption (HTTPS, VPN)**
- দুটি একসাথে ব্যবহার হয়ে **Man-in-the-Middle (MITM)** attack হতে পারে

---

## পরীক্ষার টিপস ✍️

- মূল পার্থক্য এক লাইনে লিখবে: **"Spoofing-এ পরিচয় নকল করা হয়, Sniffing-এ data চুরি করে পড়া হয়"**
- **Active বনাম Passive** পার্থক্য অবশ্যই লিখবে
- ছোট diagram এঁকে দুটির পার্থক্য দেখাবে
- প্রতিটির **একটি করে real example** দেবে
- Extra নম্বরের জন্য **প্রতিরোধের উপায়** লিখবে (Encryption, MFA)


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


# Q-02: Attacker steals private key of website that uses transport layer security and remains undetected. What can be done with a private key?

# Stolen TLS Private Key: Attacker কী করতে পারে?

## মূল ধারণা

TLS-এ website-এর **Public Key** সবাই জানে (certificate-এ থাকে), কিন্তু **Private Key** শুধু server-এর কাছে গোপন থাকার কথা। এই private key-ই **server-এর পরিচয়ের প্রমাণ**। এটি চুরি হলে attacker **server-এর মতো আচরণ** করতে পারে, আর কেউ টের পায় না।

---

## Attacker যা যা করতে পারে

### ১. Server Impersonation (নকল server বানানো)

Certificate (public) + চুরি করা private key দিয়ে attacker একটি **ভুয়া server** চালাতে পারে। Browser-এ **সবুজ lock 🔒 ও valid certificate** দেখাবে, তাই user সন্দেহ করবে না।

### ২. Man-in-the-Middle (MITM) Attack

DNS Spoofing বা ARP Spoofing দিয়ে user-কে নিজের server-এ টেনে এনে attacker **দুই পক্ষের মাঝখানে বসে** data পড়ে, বদলায় ও forward করে।

```
User ──────► [Attacker: নকল Server] ──────► আসল Server
       🔒 valid             (private key আছে)
       certificate দেখায়    password, cookie পড়ে ফেলে
```

### ৩. Past Traffic Decrypt করা (শর্তসাপেক্ষ)

- যদি **RSA key exchange** ব্যবহার হয়ে থাকে, তাহলে attacker আগে থেকে **রেকর্ড করা পুরনো traffic**-ও decrypt করতে পারবে, কারণ session key server-এর public key দিয়ে encrypt হয়েছিল।
- যদি **Forward Secrecy (ECDHE/DHE)** থাকে, তাহলে **পুরনো session নিরাপদ**, কারণ প্রতি session-এর key আলাদা ও temporary।

### ৪. Sensitive তথ্য চুরি

Login credential, **session cookie**, credit card, personal data পড়া বা বদলানো।

### ৫. Server-এর হয়ে Digital Signature দেওয়া

Handshake-এ server-এর পরিচয় যাচাইয়ের signature attacker নিজেই বানাতে পারে।

---

## যা করতে পারে না

- Server-এর **database বা files**-এ সরাসরি ঢুকতে পারে না
- **Forward Secrecy** থাকলে পুরনো session decrypt করতে পারে না
- অন্য domain-এর জন্য **নতুন certificate বানাতে** পারে না (এর জন্য CA-র private key লাগে)

---

## প্রতিরোধ ও সমাধান

| কাজ | বর্ণনা |
|---|---|
| **Certificate Revoke** | CRL বা OCSP দিয়ে চুরি হওয়া certificate বাতিল করা |
| **নতুন Key Pair** | নতুন private-public key বানিয়ে নতুন certificate নেওয়া |
| **Forward Secrecy** | ECDHE ব্যবহার, যাতে পুরনো session নিরাপদ থাকে |
| **HSM** | Private key **Hardware Security Module**-এ রাখা, যাতে বের করা না যায় |
| **Short-lived Certificate** | অল্প মেয়াদের certificate, ক্ষতির সময় কম |
| **Certificate Transparency Log** | নকল/অস্বাভাবিক certificate monitor করা |

---

## মনে রাখার মতো তথ্য

- **Private key চুরি = server-এর পরিচয় চুরি**
- TLS-এ private key দিয়ে **signature দেওয়া** আর (RSA exchange-এ) **session key decrypt** করা হয়
- **RSA key exchange → Forward Secrecy নেই**, **ECDHE/DHE → Forward Secrecy আছে**
- Revoke করার দুই উপায়: **CRL** (Certificate Revocation List) ও **OCSP** (Online Certificate Status Protocol)
- Revoke না করা পর্যন্ত certificate-এর মেয়াদ শেষ হওয়া অবধি attack চলতে পারে
- Private key কখনো **public certificate-এ থাকে না**
- Violated security goals: **Confidentiality, Authentication, Integrity**

---

## পরীক্ষার টিপস ✍️

- মূল উত্তর এক লাইনে: **"Private key দিয়ে attacker server-এর ছদ্মবেশ ধরে MITM করতে পারে এবং (RSA হলে) পুরনো traffic-ও decrypt করতে পারে"**
- **Forward Secrecy-র কথা অবশ্যই লিখবে**, এটিই সবচেয়ে বেশি নম্বরের পয়েন্ট
- একটি **MITM diagram** এঁকে দেখাবে
- শেষে **প্রতিরোধ** (Revoke, নতুন key, HSM) লিখবে
- "Undetected" শব্দটির কারণ বলবে: **Valid certificate ও সঠিক signature থাকায় browser কিছু ধরতে পারে না**

<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


# Q-3: Preserving confidentiality, integrity, and availability of data is a restatement of the concern over falsification, masquerade, and denial of service. Explain how the first three concepts relate to the last four.

# CIA Triad বনাম Threats

## প্রশ্নের একটি নোট

প্রশ্নে "last four" বলা হলেও **তিনটি** threat লেখা আছে: falsification, masquerade, denial of service। চতুর্থটি সাধারণত **unauthorized disclosure (তথ্য ফাঁস/eavesdropping)**। আমি চারটিই ধরে উত্তর দিলাম।

---

## মূল ধারণা

**CIA Triad হলো সুরক্ষার লক্ষ্য (goal), আর চারটি threat হলো সেই লক্ষ্য ভাঙার উপায় (attack)।** একই কথা দুই দিক থেকে বলা হয়েছে: লক্ষ্য রক্ষা করা মানেই সংশ্লিষ্ট attack ঠেকানো।

| Security Goal | যে Threat এটি ভাঙে | কীভাবে |
|---|---|---|
| **Confidentiality** (গোপনীয়তা) | **Unauthorized Disclosure** | অনুমতি ছাড়া তথ্য পড়া বা ফাঁস করা (যেমন Sniffing) |
| **Integrity** (অখণ্ডতা) | **Falsification** | Data অনুমতি ছাড়া বদলানো বা জাল করা |
| **Availability** (প্রাপ্যতা) | **Denial of Service (DoS)** | বৈধ user-কে service পেতে না দেওয়া |
| **Confidentiality + Integrity** (এবং Authentication) | **Masquerade** | বৈধ user সেজে ঢুকে তথ্য পড়া ও বদলানো |

---

## বিস্তারিত সম্পর্ক

### ১. Confidentiality ↔ Unauthorized Disclosure
শুধু **অনুমোদিত ব্যক্তি** তথ্য দেখতে পারবে। কেউ অনুমতি ছাড়া দেখে ফেললে confidentiality ভাঙে।
**Example:** Public Wi-Fi-তে অন্যের password ধরে ফেলা।

### ২. Integrity ↔ Falsification
Data **সঠিক ও অপরিবর্তিত** থাকতে হবে। কেউ জাল বা বদলে দিলে integrity ভাঙে।
**Example:** ব্যাংক হিসাবে ১,০০০ টাকাকে ১০,০০,০০০ করে দেওয়া।

### ৩. Availability ↔ Denial of Service
**প্রয়োজনের সময় data/service পাওয়া** যেতে হবে। DoS-এ server-কে অতিরিক্ত request দিয়ে অচল করা হয়।
**Example:** ১০ লাখ ভুয়া request পাঠিয়ে একটি website বন্ধ করে দেওয়া।

### ৪. Masquerade: দুটি goal একসাথে ভাঙে
Masquerade-এ attacker **অন্য কারো পরিচয় নিয়ে** system-এ ঢোকে। ঢোকার পর সে:
- তথ্য **পড়তে** পারে → **Confidentiality** ভাঙে
- তথ্য **বদলাতে** পারে → **Integrity** ভাঙে

তাই masquerade হলো এমন একটি **পথ (means)**, যা দিয়ে অন্য attack করা হয়। এটি সরাসরি **Authentication** ব্যর্থ হওয়ার ফল।

---

## Diagram

```
   Security Goals (CIA)                 Threats (Attack)

   ┌─ Confidentiality ◄────── ✗ ──────  Unauthorized Disclosure
   │                                         ▲
   │                                         │ (পথ)
   │                                    Masquerade (ছদ্মবেশ)
   │                                         │ (পথ)
   │                                         ▼
   ├─ Integrity ◄──────────── ✗ ──────  Falsification
   │
   └─ Availability ◄───────── ✗ ──────  Denial of Service
```

---

## মনে রাখার মতো তথ্য

- **CIA = Confidentiality, Integrity, Availability**
- **Goal ও Threat জোড়া:** C ↔ Disclosure, I ↔ Falsification, A ↔ DoS
- **Masquerade** একা কোনো এক goal ভাঙে না, এটি **C ও I** দুটোকেই আক্রমণের পথ খুলে দেয়
- Masquerade ঠেকায় **Authentication** (password, MFA, biometric)
- Disclosure ঠেকায় **Encryption**, Falsification ঠেকায় **Hash/Digital Signature**, DoS ঠেকায় **Firewall, Redundancy, Load balancing**
- Threat-এর ধরন: Disclosure, Falsification, Masquerade = **তথ্যের উপর আক্রমণ**; DoS = **সেবার উপর আক্রমণ**

---

## পরীক্ষার টিপস ✍️

- মূল কথা আগে লিখবে: **"CIA হলো লক্ষ্য, আর চারটি threat হলো সেই লক্ষ্য ভাঙার উপায়"**
- **একটি জোড়া মিলানোর ছক** অবশ্যই আঁকবে (Goal → Threat → Example)
- **Masquerade**-এর ব্যাখ্যায় লিখবে যে এটি **একসাথে C ও I ভাঙে**, এতে বাড়তি নম্বর পাওয়া যায়
- প্রতিটির জন্য **একটি ছোট real example** দেবে
- প্রতিরোধের উপায়ও সংক্ষেপে লিখবে (Encryption, Hash, Authentication, Firewall)


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


# Q-02: Compare between TCP and UDP: their connection, reliability, speed. One real-life use case of UDP.