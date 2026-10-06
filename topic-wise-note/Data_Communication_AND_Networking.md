<h1 align="center">TOPIC - Data_Communication_AND_Networking</h1> <br>

# Question: In order to prevent that, the company decided to add end-to-end encryption techniques. Which layer of the OSI model is suitable to work in, considering parameters like development time, software maintainability, and development cost? Give reasons for your concepts.

# End-to-End Encryption: কোন OSI Layer উপযুক্ত?

## উত্তর: **Application Layer (Layer 7)**

**কারণ:** End-to-end encryption মানে data **sender-এর application-এই encrypt** হবে এবং শুধু **receiver-এর application-এই decrypt** হবে। মাঝের কোনো router, server বা network device plaintext দেখতে পাবে না। এই শর্ত একমাত্র Application layer-ই সবচেয়ে সহজে পূরণ করে।

---

## Diagram

```
Sender App                                              Receiver App
┌──────────┐                                            ┌──────────┐
│ Encrypt  │ ══► Network ══► Router ══► Server ══►      │ Decrypt  │
│ (L7)     │      (সবখানে ciphertext, কেউ পড়তে পারে না) │ (L7)     │
└──────────┘                                            └──────────┘
```

---

## তিনটি Parameter অনুযায়ী যুক্তি

| Parameter | Application Layer কেন ভালো |
|---|---|
| **Development Time** | OS, kernel বা hardware বদলাতে হয় না। শুধু application code-এ ready-made library (OpenSSL, libsodium) যোগ করলেই হয়, তাই দ্রুত শেষ হয় |
| **Software Maintainability** | Encryption logic application-এর ভেতরেই থাকে, তাই update ও bug fix একজায়গায় করা যায়। Network device বা OS-এর উপর নির্ভরতা নেই |
| **Development Cost** | নতুন hardware, special driver বা network equipment কিনতে হয় না। বিদ্যমান team ও software stack দিয়েই কাজ হয় |

**অতিরিক্ত সুবিধা:**
- **True end-to-end:** Server বা middleman-ও plaintext দেখতে পায় না
- **Flexible:** শুধু sensitive field (যেমন password, card number) encrypt করা যায়
- Network, OS বা device বদলালেও encryption একই থাকে

---

## অন্য Layer কেন কম উপযুক্ত?

| Layer | সমস্যা |
|---|---|
| **Physical / Data Link (L1-L2)** | শুধু **hop-by-hop** (link-to-link)। প্রতিটি router-এ decrypt হয়, তাই end-to-end নয়। Hardware বদলাতে হয়, খরচ বেশি |
| **Network (L3), যেমন IPsec** | **Host-to-host** সুরক্ষা, application-to-application নয়। OS/kernel-level configuration লাগে, maintain করা কঠিন |
| **Transport (L4), যেমন TLS** | সহজ ও জনপ্রিয়, কিন্তু সাধারণত **server-এ এসে শেষ হয়ে যায়**। Server plaintext দেখতে পারে, তাই user-to-user end-to-end নয় |

---

## একটি গুরুত্বপূর্ণ ব্যতিক্রম

যদি লক্ষ্য শুধু **client ও company-র server-এর মধ্যে** data সুরক্ষিত রাখা হয়, তাহলে **Transport layer (TLS/HTTPS)** সবচেয়ে সস্তা ও দ্রুত সমাধান, কারণ প্রায় কোনো code না বদলেই চালু করা যায়। কিন্তু প্রশ্নে **end-to-end** বলা আছে, তাই Application layer-ই সঠিক উত্তর।

**Trade-off:** Application layer-এ প্রতিটি application-এ আলাদাভাবে encryption বানাতে হয়। আর key management-এর দায়িত্বও developer-এর।

---

## মনে রাখার মতো তথ্য

- **OSI-র ৭ layer:** Physical, Data Link, Network, Transport, Session, Presentation, Application
- **Data Link:** hop-by-hop encryption | **Network:** host-to-host (IPsec) | **Transport:** TLS/SSL | **Application:** true end-to-end
- **End-to-End Encryption (E2EE):** শুধু sender ও receiver data পড়তে পারে, মাঝের কেউ নয়
- Application layer E2EE-এর উদাহরণ: **WhatsApp, Signal** (Signal Protocol), **PGP** email
- TLS **encryption in transit** দেয়, কিন্তু server-এ decrypt হয়
- Encryption যত **নিচের layer-এ**, তত বেশি **application-transparent**, কিন্তু **কম end-to-end**

---

## পরীক্ষার টিপস ✍️

- উত্তর শুরুতেই লিখবে: **"Application Layer (Layer 7)"** এবং এক লাইনে কারণ
- **তিনটি parameter (time, maintainability, cost)** আলাদা আলাদা করে ব্যাখ্যা করবে, প্রশ্নে এটাই চাওয়া হয়েছে
- **অন্য layer কেন নয়** তা ছোট ছকে দেখাবে, এতে যুক্তি শক্ত হয়
- শেষে **Transport layer (TLS)-এর কথা ও তার সীমাবদ্ধতা** (server-এ decrypt হয়) mention করলে extra নম্বর পাওয়া যায়
- একটি ছোট diagram এঁকে **ciphertext মাঝপথে সর্বত্র** দেখাবে

<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


# Q-02: Compare between TCP and UDP: their connection, reliability, speed. One real-life use case of UDP.

# TCP বনাম UDP

## সংজ্ঞা

- **TCP (Transmission Control Protocol):** **Connection-oriented ও reliable** protocol। Data পাঠানোর আগে connection তৈরি করে এবং সব data সঠিকভাবে পৌঁছেছে কিনা নিশ্চিত করে।
- **UDP (User Datagram Protocol):** **Connectionless ও unreliable** protocol। কোনো connection ছাড়াই data সরাসরি পাঠিয়ে দেয়, পৌঁছালো কিনা দেখে না।

**তুলনা:** TCP হলো **রেজিস্ট্রি চিঠি** (প্রাপ্তি নিশ্চিত হয়), UDP হলো **সাধারণ postcard** (ফেলে দিলাম, পৌঁছালো কিনা জানি না)।

---

## Diagram

```
        TCP                                    UDP
  Client        Server                   Client        Server
    │── SYN ────►│                          │── Data ────►│
    │◄─ SYN+ACK ─│  3-way                   │── Data ────►│  কোনো handshake নেই
    │── ACK ────►│  handshake               │── Data ──✗  │  হারালে আর পাঠায় না
    │── Data ───►│                          │
    │◄─── ACK ───│  প্রতি data-র ACK
```

---

## তুলনামূলক ছক

| বিষয় | **TCP** | **UDP** |
|---|---|---|
| **Connection** | Connection-oriented (**3-way handshake**) | Connectionless (handshake নেই) |
| **Reliability** | Reliable (ACK, retransmission, error control) | Unreliable (data হারালে ফেরত পাঠায় না) |
| **Speed** | ধীর (overhead বেশি) | **দ্রুত** (overhead কম) |
| **Data order** | Order বজায় রাখে (sequence number) | Order নিশ্চিত নয় |
| **Header size** | 20-60 byte | **8 byte** |
| **Flow/Congestion control** | আছে | নেই |
| **Data পাঠানোর ধরন** | Byte stream | Datagram (আলাদা packet) |
| **ব্যবহার** | Web (HTTP/HTTPS), Email, File transfer (FTP) | Video call, Live streaming, Online game, DNS |

**কেন TCP ধীর?** Handshake, acknowledgment, retransmission ও ordering করতে অতিরিক্ত সময় ও header লাগে। **কেন UDP দ্রুত?** এসব কিছুই করে না, শুধু data পাঠায়।

---

## UDP-র Real-Life Use Case: Live Video Call (Zoom / Google Meet)

Video call-এ **গতি আসল গুরুত্বের**, নিখুঁত data নয়। একটি frame হারিয়ে গেলে ছবি এক মুহূর্ত ঝাপসা হয়, কিন্তু call চলতে থাকে। TCP ব্যবহার করলে হারানো packet আবার পাঠাতে গিয়ে **delay ও freezing** হতো, আর পুরনো frame এসে লাভও নেই কারণ কথোপকথন ততক্ষণে এগিয়ে গেছে।

অন্যান্য উদাহরণ: **Online gaming, Live streaming, VoIP, DNS query**।

---

## মনে রাখার মতো তথ্য

- TCP = **Reliable, Connection-oriented, ধীর** | UDP = **Unreliable, Connectionless, দ্রুত**
- Handshake: **SYN → SYN-ACK → ACK** (3-way)
- TCP header **20 byte (min)**, UDP header **8 byte**
- দুটিই **Transport Layer (Layer 4)**-এর protocol
- **TCP-র protocol:** HTTP, HTTPS, FTP, SMTP, SSH | **UDP-র protocol:** DNS, DHCP, TFTP, SNMP, VoIP
- TCP-তে আছে **Flow control, Congestion control, Error recovery**; UDP-তে নেই
- UDP-তে **broadcast ও multicast** সম্ভব, TCP-তে নয়

---

## পরীক্ষার টিপস ✍️

- আগে **দুটির সংজ্ঞা** লিখবে, তারপর **তুলনার ছক**
- প্রশ্নে চাওয়া তিনটি বিষয়ই (**connection, reliability, speed**) আলাদা row-তে দেবে
- **3-way handshake diagram** এঁকে দিলে নম্বর বেশি পাওয়া যায়
- UDP-র use case-এ লিখবে **কেন TCP নয়** (delay এড়াতে), শুধু নাম লিখলে পূর্ণ নম্বর মেলে না
- মূল পার্থক্য এক লাইনে: **"TCP নির্ভরযোগ্য কিন্তু ধীর, UDP দ্রুত কিন্তু অনির্ভরযোগ্য"**


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>

# #Q-03 : Write down the functionality of OSI model.

## সংজ্ঞা

**OSI (Open Systems Interconnection) Model** হলো **ISO** কর্তৃক তৈরি একটি **৭ স্তরের (7-layer) reference model**, যা বর্ণনা করে **network-এ data কীভাবে এক device থেকে অন্য device-এ পৌঁছায়**। এটি পুরো communication প্রক্রিয়াকে ছোট ছোট স্তরে ভাগ করে, যাতে প্রতিটি স্তর **নির্দিষ্ট একটি কাজ** করে।

---

## Diagram

```
 Sender                                        Receiver
┌─────────────────┐                        ┌─────────────────┐
│ 7 Application   │ ◄──────────────────►   │ 7 Application   │
│ 6 Presentation  │                        │ 6 Presentation  │
│ 5 Session       │   Data উপর থেকে নিচে    │ 5 Session       │
│ 4 Transport     │   (Encapsulation)      │ 4 Transport     │
│ 3 Network       │         │              │ 3 Network       │
│ 2 Data Link     │         ▼              │ 2 Data Link     │
│ 1 Physical      │ ═══ Physical Medium ═══│ 1 Physical      │
└─────────────────┘   নিচ থেকে উপরে        └─────────────────┘
                      (Decapsulation)
```

---

## প্রতিটি Layer-এর Functionality

| Layer | নাম | প্রধান কাজ | PDU | উদাহরণ |
|---|---|---|---|---|
| **7** | **Application** | User-কে network service দেয় (email, web, file transfer) | Data | HTTP, FTP, SMTP, DNS |
| **6** | **Presentation** | Data-র **format, encryption, compression**; data translate করে | Data | SSL/TLS, JPEG, ASCII |
| **5** | **Session** | **Session শুরু, পরিচালনা ও শেষ** করে; synchronization | Data | NetBIOS, RPC |
| **4** | **Transport** | **End-to-end delivery**, segmentation, error ও flow control | Segment | TCP, UDP |
| **3** | **Network** | **Logical addressing (IP)** ও **routing**, সেরা path বাছাই | Packet | IP, ICMP, Router |
| **2** | **Data Link** | **Physical addressing (MAC)**, framing, error detection | Frame | Ethernet, Switch |
| **1** | **Physical** | **Bit (0/1)-কে signal-এ** রূপান্তর করে মাধ্যমে পাঠায় | Bit | Cable, Hub, Wi-Fi |

---

## OSI Model-এর সামগ্রিক Functionality

- **Standardization:** বিভিন্ন কোম্পানির device ও software-এর মধ্যে **common নিয়ম** দেয়, ফলে সব system একসাথে কাজ করতে পারে (interoperability)
- **Layering (কাজ ভাগ):** জটিল communication-কে সহজ ধাপে ভাগ করে
- **Encapsulation ও Decapsulation:** প্রতি layer data-র সাথে নিজের **header** যোগ করে (sender-এ) এবং সরায় (receiver-এ)
- **Troubleshooting সহজ:** সমস্যা কোন layer-এ তা খুঁজে বের করা যায়
- **Independence:** একটি layer বদলালে অন্য layer-এর উপর প্রভাব পড়ে না

---

## মনে রাখার মতো তথ্য

- **৭ layer (উপর থেকে নিচে):** Application, Presentation, Session, Transport, Network, Data Link, Physical
- **মুখস্থ কৌশল:** **"All People Seem To Need Data Processing"**
- **PDU ক্রম:** Data → Segment → Packet → Frame → Bit
- **Addressing:** Network layer = **IP (logical)**, Data Link layer = **MAC (physical)**
- **Device:** Router = **Layer 3**, Switch = **Layer 2**, Hub = **Layer 1**
- **Encryption ও compression** হয় **Presentation layer**-এ
- OSI **ISO** তৈরি করেছে (১৯৮৪), আর বাস্তবে বেশি ব্যবহৃত হয় **TCP/IP model (৪ layer)**
- OSI একটি **reference/theoretical model**, TCP/IP হলো **practical model**

---

## পরীক্ষার টিপস ✍️

- আগে **সংজ্ঞা** লিখবে, তারপর **৭ layer-এর diagram** আঁকবে
- **Layer ছক**-এ নাম, কাজ, PDU ও উদাহরণ অবশ্যই দেবে
- Layer-এর **ক্রম** (উপর থেকে নিচে বা নিচ থেকে উপরে) ঠিক রাখবে
- **Encapsulation-Decapsulation**-এর কথা mention করলে extra নম্বর পাওয়া যায়
- মুখস্থ করতে **"All People Seem To Need Data Processing"** ব্যবহার করবে (A-P-S-T-N-D-P)



<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>





# #Q-4: Explain the logic of a "Checksum". How is it used to verify data integrity during file transfer?

## সংজ্ঞা

**Checksum** হলো data থেকে হিসাব করে বের করা একটি **ছোট মান (fixed-size value)**, যা data-র **"আঙুলের ছাপ"-এর মতো কাজ করে**। Data-র একটি bit বদলালেও সাধারণত checksum-এর মান বদলে যায়, তাই transfer-এর সময় **accidental error ধরা যায়**।

---

## মূল Logic

1. **Sender** data থেকে checksum হিসাব করে এবং data-র সাথে পাঠায়।
2. **Receiver** পাওয়া data থেকে আবার নিজে checksum হিসাব করে।
3. দুটি মান **মিললে** data ঠিক আছে ✅, **না মিললে** data নষ্ট হয়েছে ❌ (আবার পাঠাতে হবে)।

```
Sender                                         Receiver
┌──────────┐   Data + Checksum    ┌──────────────────────┐
│ Data     │ ───────────────────► │ পাওয়া Data          │
│   ↓      │                      │   ↓                  │
│ Checksum │                      │ নতুন Checksum হিসাব  │
│ হিসাব    │                      │   ↓                  │
└──────────┘                      │ পাঠানোটির সাথে মেলাও │
                                  │  মিলল → OK ✅        │
                                  │  মিলল না → Error ❌  │
                                  └──────────────────────┘
```

---

## Example: Simple Checksum (Sum mod 256)

**Data (byte):** `25, 40, 60, 75`

```
Checksum = (25 + 40 + 60 + 75) mod 256 = 200 mod 256 = 200
পাঠানো হলো: 25, 40, 60, 75 | 200
```

**Case 1: সঠিকভাবে পৌঁছালো**
```
Receiver হিসাব: 25 + 40 + 60 + 75 = 200 → 200 == 200 ✅ সঠিক
```

**Case 2: পথে একটি byte নষ্ট হলো (60 → 61)**
```
Receiver হিসাব: 25 + 40 + 61 + 75 = 201 → 201 ≠ 200 ❌ Error ধরা পড়লো
```

---

## File Transfer-এ Integrity যাচাই

বড় file (যেমন Linux ISO, software) download করলে ওয়েবসাইট file-এর সাথে একটি **hash (checksum)** দেয়, সাধারণত **SHA-256**। নিয়ম:

1. File **download** করো
2. নিজের computer-এ checksum **হিসাব** করো
3. ওয়েবসাইটের দেওয়া মানের সাথে **মিলাও**

```bash
sha256sum ubuntu.iso
# আউটপুট: a3f5c9...e21b  ubuntu.iso
```

মিললে file **অক্ষত**, না মিললে **corrupt** (network error-এ নষ্ট) বা **বদলানো** (tampered), তাই আবার download করতে হবে।

**ব্যবহারের জায়গা:** TCP/UDP/IP header-এর error detection, file download verification, backup যাচাই, ZIP/CRC।

---

## সীমাবদ্ধতা

| সমস্যা | ব্যাখ্যা |
|---|---|
| **শুধু error detect করে, ঠিক করে না** | ভুল ধরলে আবার পাঠাতে হয় |
| **Simple checksum-এ কিছু error ধরা পড়ে না** | যেমন byte-এর **জায়গা বদল** (25,40 → 40,25): sum একই থাকে |
| **ইচ্ছাকৃত পরিবর্তন ঠেকায় না** | হ্যাকার data বদলে নতুন checksum বসিয়ে দিতে পারে |

**সমাধান:** নিরাপত্তার জন্য **cryptographic hash (SHA-256)**, **HMAC** বা **Digital Signature** ব্যবহার করা হয়।

---

## মনে রাখার মতো তথ্য

- Checksum **Data Integrity** যাচাই করে (CIA-র **I**)
- Receiver-এর হিসাব ও পাঠানো মান **মিললে OK, না মিললে Error**
- **Internet Checksum:** 16-bit, **1's complement sum**, IP/TCP/UDP header-এ ব্যবহৃত হয়
- **Checksum** সাধারণত accidental error-এর জন্য, **Hash (SHA-256)** নিরাপত্তার জন্য
- জনপ্রিয় ধরন: **Parity bit, CRC, MD5, SHA-1, SHA-256**
- **MD5 ও SHA-1** এখন নিরাপদ নয় (collision সম্ভব), তাই **SHA-256** ব্যবহার করা উচিত
- Checksum **error detection** দেয়, **error correction** নয়
- Checksum-এর আকার data যত বড়ই হোক **fixed** থাকে

---

## পরীক্ষার টিপস ✍️

- আগে **সংজ্ঞা**, তারপর **Sender-Receiver diagram** আঁকবে
- **একটি সংখ্যাসহ example** দিয়ে দেখাবে কীভাবে error ধরা পড়ে (সঠিক ও ভুল দুই case)
- File transfer অংশে **`sha256sum` ও hash মেলানোর ধাপ** লিখবে
- **সীমাবদ্ধতা** লিখলে extra নম্বর: শুধু accidental error ধরে, ইচ্ছাকৃত tampering নয়
- মূল কথা এক লাইনে: **"Checksum হলো data-র একটি সারাংশ-মান, যা মিলিয়ে দেখলে বোঝা যায় data পথে বদলেছে কিনা"**


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


# #Q-05: CRC is a redundancy error technique used to determine the error. Suppose the original data is 11100 and the divisor is 1001.