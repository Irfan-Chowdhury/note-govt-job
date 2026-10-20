# Previous Year Question

1. Define a Virtual machine with a neat diagram, explain the working of VM. What is the benifits of a VM? [BB-AME-2023]
2. What is the challenges in optimizing energy efficiency of data center? Explain. [BB-AME-2023]
3. Server rack diagram for horizontal and vertical scaling. [prakritik gas-2023]
4. What is DMZ? [Maddhapara Granite Mining Company Limited-2023]
5. How virtualization help physical server. [pubali bank-2023]
6. Difference SAS anta Sata. Which one is best for server. [pubali bank-2023]
7. Explain Type 1 and Type 2 hypervisors in virtual machine operating system with figure. [agrani-17]
8. Explain the component of Data Center. [agrani-17]
9. Write short notes on DHCP and SMTP. [BB AME-17]
10. Working process of DNS.
11. Explain Active Directory.
12. Explain the architecture framework of WWW with diagram. Write the steps that occur when an URL is selected in the browser with an example www.psc.gov.bd. [BPSC-2023]
13. What is DCIM in a data center? [BDCCL-2022]
14. What do you mean by TIERing of a data center? Distinguish between different data center TIER standards with illustrative figure. [BDCCL-2022]
15. What do you mean by dynamic capacity provisioning? Why it is essential for a data center. [BDCCL-2022]
16. What is a DMZ in networking? [MGMCL-2022] [BDCCL-2022]
17. What is Cloud computing? Describe advantage and disadvantage. [NPCBL-JET-2022]
18. What is DCIM in a data center. [BDCCL-2022]
19. What are the three types of services provided by the cloud? [BPSC-2021]
20. What is DHCP Server and why it is needed in a computer network. [National Telecommunication monitor center- 2022]
21. Write a short note on: a) DNS b) Cloud Computing. [BPSC-2022]


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>

## Topic-wise Merged & Consolidated Questions

### 1. Virtualization & Hypervisors
1. Define a Virtual Machine (VM) with a neat diagram, explain its working principle, and discuss its benefits and how virtualization helps physical servers.
2. Explain Type 1 and Type 2 hypervisors in a virtual machine operating system with illustrative diagrams.

### 2. Data Center Infrastructure & Management
1. Explain the essential components of a Data Center.
2. What do you mean by TIERing of a data center? Distinguish between different data center TIER standards with an illustrative figure.
3. What is DCIM (Data Center Infrastructure Management) in a data center?
4. What are the challenges in optimizing the energy efficiency of a data center? Explain.
5. What do you mean by dynamic capacity provisioning? Why is it essential for a data center?

### 3. Server Hardware & Architecture
1. Provide a server rack diagram illustrating horizontal and vertical scaling.
2. Differentiate between SAS and SATA drives. Which one is best suited for a server environment?

### 4. Cloud Computing
1. What is Cloud Computing? Describe its key advantages, disadvantages, and provide a short overview.
2. What are the three primary types of cloud computing service models (IaaS, PaaS, SaaS)?

### 5. Network Services, Protocols & Security
1. What is a DMZ (Demilitarized Zone) in computer networking, and what is its purpose?
2. What is a DHCP server, why is it needed in a computer network, and write a short note on DHCP.
3. Explain the working process of DNS (Domain Name System) with a short note.
4. Write a short note on SMTP.
5. Explain Active Directory and its role in network management.
6. Explain the architectural framework of WWW with a diagram. Describe step-by-step what happens when a URL (e.g., www.psc.gov.bd) is entered into a web browser.

<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>


---

# 📚 Topic 01: Virtualization & Hypervisors (ভার্চুয়ালাইজেশন ও হাইপারভাইজর)

> **লক্ষ্য (Target):** সরকারি চাকরির লিখিত (Written) পরীক্ষা ও প্রিলিমিনারি (MCQ) পরীক্ষার সম্পূর্ণ ও কম্প্যাক্ট প্রস্তুতি।

---

## ১. ভার্চুয়ালাইজেশন (Virtualization) কী?

### 📌 মূল সংজ্ঞা (Definition):
**Virtualization** হলো এমন একটি আধুনিক প্রযুক্তি বা কৌশল, যার মাধ্যমে একটি একক ফিজিক্যাল কম্পিউটার বা সার্ভারের হার্ডওয়্যার রিসোর্সকে (যেমন: CPU, RAM, Storage, Network Interface) সফটওয়্যারের সাহায্যে একাধিক লজিক্যাল বা ভার্চুয়াল পরিবেশে বিভক্ত করে ব্যবহার করা যায়। প্রতিটি ভার্চুয়াল পরিবেশ সম্পূর্ণ স্বাধীন কম্পিউটার বা সিস্টেম হিসেবে কাজ করে।

সহজ কথায়:
$$\text{একটি Physical Server} \xrightarrow{\text{Virtualization}} \text{একাধিক Virtual Server বা Machine}$$

### 📌 Virtualization-এর মূল উদ্দেশ্য ও প্রয়োজনীয়তা:
1. **Resource Optimization:** হার্ডওয়্যার রিসোর্সের সর্বোচ্চ ব্যবহার নিশ্চিত করা (ঐতিহ্যবাহী সনাতন সার্ভারে গড়ে মাত্র ১০-১৫% রিসোর্স ব্যবহৃত হতো, যা ভার্চুয়ালাইজেশনের ফলে ৮০-৯০% পর্যন্ত দক্ষতার সাথে ব্যবহার করা সম্ভব)।
2. **Cost Reduction (CAPEX & OPEX):** নতুন ফিজিক্যাল সার্ভার কেনার খরচ (Capital Expenditure) এবং বিদ্যুৎ, কুলিং ও রক্ষণাবেক্ষণ খরচ (Operational Expenditure) উল্লেখযোগ্যভাবে হ্রাস করা।
3. **High Availability & Disaster Recovery:** সার্ভার ব্যাকআপ, মাইগ্রেশন (Live Migration) ও দুর্যোগ পরবর্তী রিকভারি দ্রুত এবং সহজে নিশ্চিত করা।
4. **Isolation & Security:** প্রতিটি ভার্চুয়াল মেশিন সম্পূর্ণ পৃথক (Isolated) থাকে; একটি VM ক্র্যাশ বা হ্যাক হলে পাশের VM কোনোভাবেই ক্ষতিগ্রস্ত হয় না।

---

## ২. ভার্চুয়াল মেশিন (Virtual Machine - VM)

### 📌 সংজ্ঞা (Definition):
**Virtual Machine (VM)** হলো সফটওয়্যারের মাধ্যমে তৈরি করা একটি সম্পূর্ণ কম্পিউটার সিস্টেম (Emulated Computer System)। এটি বাস্তব (Physical) কম্পিউটারের মতোই নিজস্ব Operating System (OS), অ্যাপ্লিকেশন, প্রসেসর (vCPU), মেমরি (vRAM) এবং ভার্চুয়াল স্টোরেজ নিয়ে স্বাধীনভাবে চলে।

* **Host Machine:** মূল ফিজিক্যাল সার্ভার বা হার্ডওয়্যারকে Host বলা হয়।
* **Guest Machine:** Host-এর উপর চালিত প্রতিটি Virtual Machine-কে Guest Machine বলা হয়।
* **Guest OS:** VM-এর ভেতরে ইনস্টল করা নিজস্ব অপারেটিং সিস্টেম (যেমন: Linux, Windows Server)।

---

### 📌 Virtual Machine (VM)-এর আর্কিটেকচার ডায়াগ্রাম (Neat Architecture Diagram):

```
+-------------------------------------------------------------+
|                 Physical Server (Hardware)                  |
|          [ CPU | RAM | Storage / HDD / SSD | NIC ]          |
+-------------------------------------------------------------+
                              ▲
                              │
+-------------------------------------------------------------+
|           Hypervisor / Virtual Machine Monitor (VMM)        |
+-------------------------------------------------------------+
         │                                            │
         ▼                                            ▼
+-----------------------+                    +-----------------------+
|  Virtual Machine 1    |                    |  Virtual Machine 2    |
| +-------------------+ |                    | +-------------------+ |
| |    Application    | |                    | |    Application    | |
| +-------------------+ |                    | +-------------------+ |
| |  Guest OS (Linux) | |                    | | Guest OS (Windows)| |
| +-------------------+ |                    | +-------------------+ |
| | Virtual Hardware  | |                    | | Virtual Hardware  | |
| | (vCPU, vRAM, Disk)| |                    | | (vCPU, vRAM, Disk)| |
| +-------------------+ |                    | +-------------------+ |
+-----------------------+                    +-----------------------+
```

---

### 📌 VM কীভাবে কাজ করে? (Working Principle of VM):

1. **Abstraction Layer সৃষ্টি:** ফিজিক্যাল হার্ডওয়্যারের উপরে **Hypervisor** বা **VMM (Virtual Machine Monitor)** নামক একটি স্তর তৈরি হয়, যা ফিজিক্যাল হার্ডওয়্যারকে সরাসরি কন্ট্রোল করে।
2. **Resource Emulation ও Virtual Hardware তৈরি:** Hypervisor ফিজিক্যাল প্রসেসর, র‍্যাম ও ডিস্ককে ছোট ছোট অংশে ভাগ করে প্রতিটি VM-কে ভার্চুয়াল কম্পোনেন্ট হিসেবে প্রদান করে (vCPU, vRAM, Virtual Disk)।
3. **Guest OS পরিচালনা:** প্রতিটি VM মনে করে সে সরাসরি আসল হার্ডওয়্যারে চলছে। Guest OS কোনো ইনপুট/আউটপুট বা এক্সিকিউশন পাঠালে Hypervisor তা অনুবাদ করে আসল ফিজিক্যাল প্রসেসরে পাঠায় এবং ফলাফল ফিরিয়ে দেয়।
4. **Sandboxing ও Isolation:** হাইপারভাইজরের কারণে প্রতিটি VM একটি বাউন্ডারির (Sandbox) মধ্যে সীমাবদ্ধ থাকে, ফলে মেমোরি ওভারল্যাপিং বা ইন্টারফারেন্সের সুযোগ থাকে না।

---

### 📌 VM ও ভার্চুয়ালাইজেশনের সুবিধা (Benefits of VM & Virtualization):

* **১. Server Consolidation (সার্ভার সংহতকরণ):** আগে ১০টি ভিন্ন সার্ভিসের জন্য ১০টি আলাদা সার্ভার লাগত। এখন ১টি শক্তিশালী সার্ভারে ১০টি VM তৈরি করে সব চালানো যায়।
* **২. খরচ হ্রাস (Cost Saving):** হার্ডওয়্যার ক্রয় খরচ, ডেটাসেন্টারের ফ্লোর স্পেস, ক্যাবলিং, বিদ্যুৎ বিল ও এসি কুলিং খরচ নাটকীয়ভাবে কমে যায়।
* **৩. দ্রুত ডিপ্লয়মেন্ট (Rapid Provisioning):** নতুন ফিজিক্যাল সার্ভার প্রকিউর করতে সপ্তাহ বা মাস লাগলেও একটি নতুন VM মাত্র কয়েক মিনিটেই ইনস্টল বা টেমপ্লেট থেকে ক্লোন করা যায়।
* **৪. Live Migration (জিরো ডাউনটাইম স্থানান্তর):** হার্ডওয়্যার আপগ্রেড বা মেইনটেন্যান্সের সময় চলমান সার্ভিস বন্ধ না করেই সচল VM-কে এক সার্ভার থেকে অন্য সার্ভারে পাঠানো যায় (VMware vMotion প্রযুক্তি)।
* **৫. সহজ ব্যাকআপ ও স্ন্যাপশট (Snapshots & Backups):** VM-কে একটি সিঙ্গেল ফাইলের মতো ব্যাকআপ নেওয়া যায়। সফটওয়্যার আপডেট বা প্যাচিংয়ের পূর্বে Snapshot নিয়ে রাখলে কোনো জটিলতা হলে মুহূর্তেই রোলব্যাক করা যায়।
* **৬. বহু অপারেটিং সিস্টেমের সহাবস্থান:** একই সার্ভারে কোনো দ্বন্দ্ব ছাড়াই একসাথে Windows Server, RedHat Enterprise Linux, Ubuntu ইত্যাদি পাশাপাশি চলতে পারে।

---

### 📌 ভার্চুয়ালাইজেশন কীভাবে ফিজিক্যাল সার্ভারকে সাহায্য করে? (How Virtualization Helps Physical Server):

| সনাতন ফিজিক্যাল সার্ভার (Without Virtualization) | ভার্চুয়ালাইজড সার্ভার (With Virtualization) |
| :--- | :--- |
| **রিসোর্স অপচয়:** সার্ভার মাত্র ১০-১৫% ক্ষমতা ব্যবহার করত (Underutilization)। | **রিসোর্সের পূর্ণ ব্যবহার:** সার্ভার ক্যাপাসিটি ৮০-৯০% পর্যন্ত দক্ষতার সাথে ব্যবহৃত হয়। |
| **একক ব্যর্থতার ঝুঁকি (Single Point of Failure):** ফিজিক্যাল পার্টস নষ্ট হলে সার্ভিস পুরোপুরি বন্ধ হয়ে যেত। | **হাই অ্যাভেইলেবিলিটি (High Availability - HA):** একটি ফিজিক্যাল নোড ফেইল করলে ক্লাস্টারের অন্য নোডে VM স্বয়ংক্রিয়ভাবে রিস্টার্ট নেয়। |
| **বিদ্যুৎ ও স্থানের অপচয়:** অধিক সার্ভারের জন্য বেশি সার্ভার র‍্যাক ও কুলিং সিস্টেম লাগত। | **গ্রিন কম্পিউটিং:** কম ফিজিক্যাল সার্ভার প্রয়োজন হওয়ায় বিদ্যুৎ সাশ্রয় হয় ও কার্বন ফুটপ্রিন্ট কমে। |
| **রক্ষণাবেক্ষণ ডাউনটাইম:** সার্ভার মেরামত করতে গেলে সার্ভিস বন্ধ রাখতে হতো। | **জিরো ডাউনটাইম মেইনটেন্যান্স:** লাইভ মাইগ্রেশনের মাধ্যমে কোনো ইউজার ইন্টারাপশন ছাড়াই হার্ডওয়্যার রিপেয়ার করা যায়। |

---

## ৩. হাইপারভাইজর (Hypervisor / Virtual Machine Monitor - VMM)

### 📌 সংজ্ঞা (Definition):
**Hypervisor** হলো একটি বিশেষ সফটওয়্যার, ফার্মওয়্যার বা ওএস কার্নেল লেয়ার যা ভার্চুয়াল মেশিন তৈরি, রিসোর্স অ্যালোকেশন এবং গেস্ট ওএসগুলোর সমন্বয় নিশ্চিত করে।

এটি প্রধানত **২ প্রকার**:
1. **Type 1 Hypervisor (Bare-Metal Hypervisor)**
2. **Type 2 Hypervisor (Hosted Hypervisor)**

---

### 📌 Type 1 Hypervisor (Bare-Metal Hypervisor):

* এটি কোনো সাধারণ ওএসের ওপর বসে না; বরং **সরাসরি ফিজিক্যাল সার্ভার হার্ডওয়্যারের ওপর (Bare-Metal)** ইনস্টল হয়।
* এটি নিজেই ওএস ও কার্নেলের মতো আচরণ করে এবং সরাসরি হার্ডওয়্যার পরিচালনা করে।
* **ব্যবহার:** এন্টারপ্রাইজ ডেটাসেন্টার, ক্লাউড কম্পিউটিং (AWS, Azure) এবং প্রোডাকশন এনভায়রনমেন্টে ব্যবহৃত হয়।
* **উদাহরণ:** VMware ESXi, Microsoft Hyper-V, Citrix Hypervisor (XenServer), KVM (Kernel-based Virtual Machine)।

```
+-----------------------------------------------------+
|        VM 1 (App + Guest OS)        | VM 2 (App + Guest OS) |
+-----------------------------------------------------+
|      Type 1 Hypervisor (Directly on Hardware)       |
+-----------------------------------------------------+
|                  Physical Hardware                  |
+-----------------------------------------------------+
```

---

### 📌 Type 2 Hypervisor (Hosted Hypervisor):

* এটি সরাসরি হার্ডওয়্যারে বসে না; প্রথমে হার্ডওয়্যারে একটি বেস অপারেটিং সিস্টেম (Host OS - যেমন: Windows 11, Linux, macOS) থাকে, তার ওপর এই হাইপারভাইজর একটি সাধারণ অ্যাপ্লিকেশনের মতো ইনস্টল হয়।
* এটি হোস্ট ওএসের মাধ্যমে পরোক্ষভাবে হার্ডওয়্যার অ্যাক্সেস করে।
* **ব্যবহার:** সফটওয়্যার ডেভেলপমেন্ট, টেস্টিং ল্যাব এবং শিক্ষার্থীদের ব্যক্তিগত পিসিতে শিক্ষার উদ্দেশ্যে।
* **উদাহরণ:** Oracle VM VirtualBox, VMware Workstation, VMware Player, Parallels Desktop।

```
+-----------------------------------------------------+
|        VM 1 (App + Guest OS)        | VM 2 (App + Guest OS) |
+-----------------------------------------------------+
|          Type 2 Hypervisor (Software Layer)         |
+-----------------------------------------------------+
|                 Host Operating System               |
+-----------------------------------------------------+
|                  Physical Hardware                  |
+-----------------------------------------------------+
```

---

### 📌 Type 1 বনাম Type 2 Hypervisor-এর পার্থক্য (Comparison Chart for Written Exam):

| বৈশিষ্ট্য (Criteria) | Type 1 (Bare-Metal Hypervisor) | Type 2 (Hosted Hypervisor) |
| :--- | :--- | :--- |
| **ইনস্টলেশন স্তর** | সরাসরি Physical Hardware-এর ওপর বসে। | Host Operating System-এর ওপর একটি সফটওয়্যার হিসেবে বসে। |
| **পারফরম্যান্স ও গতি** | অত্যন্ত দ্রুত ও উচ্চ ক্ষমতাসম্পন্ন (Overhead খুবই কম)। | তুলনামূলক ধীরগতির (Host OS অতিরিক্ত রিসোর্স ও ওভারহেড নেয়)। |
| **নিরাপত্তা (Security)** | অত্যন্ত নিরাপদ; কারণ কোনো আক্রমণযোগ্য Host OS নেই। | কম নিরাপদ; Host OS ক্ষতিগ্রস্ত হলে সমস্ত VM ঝুঁকিতে পড়ে। |
| **নির্ভরশীলতা** | কোনো বেস অপারেটিং সিস্টেমের প্রয়োজন নেই। | Host OS-এর ওপর সম্পূর্ণ নির্ভরশীল। |
| **মূল ব্যবহার ক্ষেত্র** | Data Center, Enterprise Servers, Cloud Computing। | Testing, Software Development, Personal/Home Lab। |
| **বাস্তব উদাহরণ** | VMware ESXi, MS Hyper-V, KVM, Xen। | Oracle VirtualBox, VMware Workstation, Parallels। |

---

## 🎯 সরকারি চাকরি পরীক্ষার জন্য বুলেট পয়েন্টস (MCQ Quick Recap)

1. **Hypervisor-এর অপর নাম:** Virtual Machine Monitor (VMM)।
2. **Bare-metal Hypervisor কোনটি?** $\rightarrow$ Type 1 Hypervisor (যেমন: VMware ESXi, Citrix XenServer)।
3. **Hosted Hypervisor কোনটি?** $\rightarrow$ Type 2 Hypervisor (যেমন: Oracle VirtualBox, VMware Workstation)।
4. **KVM-এর পূর্ণরূপ:** Kernel-based Virtual Machine (Linux কার্নেলে Type 1 হাইপারভাইজর হিসেবে কাজ করে)।
5. **VDI পূর্ণরূপ:** Virtual Desktop Infrastructure।
6. **VM-এর ভার্চুয়াল ডিস্ক ফরম্যাটসমূহ:** VMware-এর জন্য `.vmdk`, Microsoft Hyper-V-এর জন্য `.vhd` / `.vhdx`।
7. **Live Migration:** ডাউনটাইম ছাড়া একটি ফিজিক্যাল হোস্ট থেকে অন্য হোস্টে VM স্থানান্তর করার প্রযুক্তি (VMware-এ একে **vMotion** বলা হয়)।
8. **Server Consolidation-এর প্রধান উদ্দেশ্য:** হার্ডওয়্যারের অপচয় (Underutilization) রোধ এবং পরিচালনা খরচ (OPEX) কমানো।
