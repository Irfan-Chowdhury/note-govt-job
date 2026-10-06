<h1 align="center">TOPIC 09 - Machine Learning & Data Preprocessing</h1> <br>

# 01. Compare and contrast the three fundamental paradigms of Machine Learning: Supervised Learning, Unsupervised Learning, and Reinforcement Learning.

## Machine Learning-এর তিন Paradigm (Exam Short Note)

## মূল ধারণা

Machine Learning-এ computer **data থেকে নিজে শেখে**। শেখার পদ্ধতি অনুযায়ী তিন ভাগ:

```
                  Machine Learning
                         │
      ┌──────────────────┼──────────────────┐
      ▼                  ▼                  ▼
 Supervised         Unsupervised       Reinforcement
 (শিক্ষকসহ শেখা)     (নিজে নিজে শেখা)    (ভুল করে শেখা)
```

---

## ১. Supervised Learning

**সংজ্ঞা:** **Labeled data** (input + সঠিক উত্তর) দিয়ে model-কে শেখানো হয়। Model input থেকে output predict করা শেখে।

**উদাহরণ:** ১০,০০০টি email দেওয়া আছে, প্রতিটিতে লেখা "Spam" বা "Not Spam"। Model শিখে নতুন email spam কিনা বলে দেয়।

```
Input (X) ──► [Model] ──► Prediction
                 ▲            │
                 │            ▼
          Error ◄──── Compare with সঠিক Label (Y)
```

**ধরন:**
- **Classification:** Category predict (Spam/Not Spam, রোগ আছে/নেই)
- **Regression:** Number predict (বাড়ির দাম, তাপমাত্রা)

**Algorithm:** Linear Regression, Decision Tree, SVM, KNN, Neural Network

---

## ২. Unsupervised Learning

**সংজ্ঞা:** **Unlabeled data** (শুধু input, কোনো সঠিক উত্তর নেই) থেকে model নিজে **pattern বা group** খুঁজে বের করে।

**উদাহরণ:** একটি দোকানের গ্রাহকদের কেনাকাটার data আছে, কিন্তু কোনো label নেই। Model নিজেই গ্রাহকদের গ্রুপে ভাগ করে (যেমন: "বেশি খরচকারী", "ছাড়ের অপেক্ষাকারী")।

```
Before:  · ·  ·  · ·    ·  ·       After:  (● ●  ● ● ●)   (▲  ▲)
          ·  ·    ·   ·  ·                   Group 1       Group 2
        (এলোমেলো data)                      (model নিজে ভাগ করেছে)
```

**ধরন:**
- **Clustering:** Group তৈরি (K-Means)
- **Dimensionality Reduction:** Feature কমানো (PCA)
- **Association:** "যে X কেনে, সে Y-ও কেনে"

---

## ৩. Reinforcement Learning (RL)

**সংজ্ঞা:** একটি **Agent** একটি **Environment**-এ কাজ (action) করে এবং বিনিময়ে **Reward (পুরস্কার)** বা **Penalty (শাস্তি)** পায়। Trial and error করে সে এমন strategy শেখে, যাতে **মোট reward সর্বোচ্চ** হয়।

**উদাহরণ:** কুকুরকে ট্রেনিং দেওয়া। সঠিক কাজ করলে বিস্কুট (reward), ভুল করলে কিছু না। কয়েকবার পর কুকুর শিখে যায় কী করতে হবে।

```
        ┌─────── Action ───────┐
        │                      ▼
     [Agent]             [Environment]
        ▲                      │
        └── Reward + State ◄───┘
```

**Real-life Example:** Chess/Go খেলা AI (AlphaGo), self-driving car, robot হাঁটা শেখা।

**মূল শব্দ:** Agent, Environment, State, Action, Reward, Policy

---

## তুলনামূলক ছক (Comparison)

| বিষয় | Supervised | Unsupervised | Reinforcement |
|---|---|---|---|
| **Data ধরন** | Labeled | Unlabeled | কোনো fixed data নেই, interaction থেকে আসে |
| **Feedback** | সরাসরি (সঠিক উত্তর) | কোনো feedback নেই | Reward / Penalty |
| **লক্ষ্য** | Output predict করা | Hidden pattern খোঁজা | Reward maximize করা |
| **শেখার ধরন** | শিক্ষকের কাছে শেখা | নিজে আবিষ্কার | Trial and Error |
| **সমস্যার ধরন** | Classification, Regression | Clustering, Association | Decision making, Control |
| **উদাহরণ** | Spam detection | Customer segmentation | Game-playing AI |
| **Algorithm** | Decision Tree, SVM | K-Means, PCA | Q-Learning |
| **Evaluation** | সহজ (accuracy) | কঠিন (সঠিক উত্তর নেই) | Total reward |

---

## Contrast: এক লাইনে পার্থক্য

```
Supervised     → "এটা বিড়াল, এটা কুকুর" শিখিয়ে দেওয়া হয়েছে
Unsupervised   → ছবিগুলো দেখে নিজে বুঝে নাও কোনগুলো একই রকম
Reinforcement  → চেষ্টা করো, ঠিক হলে পুরস্কার, ভুল হলে শাস্তি
```

## মিল (Similarity)

- তিনটিই **data/experience থেকে শেখে**
- তিনটিরই লক্ষ্য **performance উন্নত করা**
- তিনটিতেই **model/algorithm** ব্যবহার হয়

---

## পরীক্ষার টিপস ✍️

- মূল পার্থক্য লিখবে: **"Supervised-এ label আছে, Unsupervised-এ নেই, Reinforcement-এ reward আছে"**
- তিনটির জন্য **আলাদা আলাদা example** দেবে (Spam, Customer grouping, Game AI)
- **Comparison table অবশ্যই আঁকবে**, এতে সবচেয়ে বেশি নম্বর
- Supervised-এর দুই ধরন (**Classification, Regression**) আর Unsupervised-এর **Clustering** মনে রাখবে
- RL-এর **Agent-Environment loop diagram** এঁকে দেখাবে
- Extra নম্বরের জন্য mention করবে: **Semi-supervised Learning** (কিছু labeled + বেশি unlabeled data)


<h2 align="center">─────── ✧ END ✧ ───────</h2> <br>

# 02. Suppose your dataset has missing values and noise. How would you preprocess it?

## Missing Values ও Noise: Data Preprocessing (Exam Short Note)

## মূল ধারণা

Real-world data কখনো পরিষ্কার থাকে না। **"Garbage In, Garbage Out"**: data খারাপ হলে model-ও খারাপ হবে। তাই training-এর আগে data **clean** করতে হয়।

- **Missing Value:** কিছু ঘরে data নেই (blank / NaN)
- **Noise:** ভুল বা অস্বাভাবিক data (যেমন বয়স = 250, বা sensor-এর ভুল reading)

---

## Preprocessing Pipeline (Diagram)

```
Raw Data
   │
   ▼
┌──────────────────────┐
│ ১. Data Inspection    │  ← কোথায় missing/noise আছে খুঁজে বের করো
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│ ২. Missing Value      │  ← Delete অথবা Impute
│    Handling           │
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│ ৩. Noise Handling     │  ← Outlier detect, Smoothing
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│ ৪. Scaling/Encoding   │  ← Normalize, categorical → number
└──────────┬───────────┘
           ▼
     Clean Data ✅ → Model Training
```

---

## ধাপ ১: Data Inspection

আগে সমস্যা কতটা তা বুঝতে হবে।

- প্রতি column-এ **কতগুলো value missing** (শতকরা হিসাব)
- **Summary statistics** (min, max, mean) দেখে অস্বাভাবিক মান ধরা
- **Box plot / Histogram** দিয়ে outlier দেখা

---

## ধাপ ২: Missing Value Handling

### পদ্ধতি ক: Deletion (মুছে ফেলা)

| ধরন | কখন ব্যবহার |
|---|---|
| **Row delete** | Missing খুব কম (< ৫%), data অনেক বেশি |
| **Column delete** | কোনো column-এর **৫০-৬০%+** missing |

**অসুবিধা:** তথ্য হারিয়ে যায়।

### পদ্ধতি খ: Imputation (ভরাট করা)

| পদ্ধতি | কখন | উদাহরণ |
|---|---|---|
| **Mean** | Numeric, outlier নেই | গড় বেতন দিয়ে ভরা |
| **Median** | Numeric, outlier আছে | বাড়ির দামে median ভালো |
| **Mode** | Categorical | সবচেয়ে বেশি আসা শহরের নাম |
| **Forward/Backward Fill** | Time-series | আগের দিনের তাপমাত্রা বসানো |
| **KNN Imputation** | সম্পর্কযুক্ত feature | কাছাকাছি similar row-এর মান |
| **Regression Imputation** | অন্য column থেকে predict সম্ভব | বয়স থেকে বেতন predict |

**Example:**

```
Age: [25, 30, NaN, 28, 35]

Mean   = (25+30+28+35)/4 = 29.5
Median = (28+30)/2       = 29

Imputed: [25, 30, 29.5, 28, 35]
```

> 💡 **Tip:** Imputation-এর আগে একটি নতুন column (`age_missing = 0/1`) রাখলে model জানতে পারে কোন মান আসল আর কোনটি ভরাট করা।

---

## ধাপ ৩: Noise Handling

### Outlier Detection

**IQR Method:**
```
Q1 = ২৫তম percentile,  Q3 = ৭৫তম percentile
IQR = Q3 - Q1

Lower limit = Q1 - 1.5 × IQR
Upper limit = Q3 + 1.5 × IQR

এই সীমার বাইরে হলে → Outlier
```

**Z-Score Method:**
```
Z = (x - mean) / std

|Z| > 3 হলে → Outlier
```

**Example:** `[10, 12, 11, 13, 250]`: 250 স্পষ্টতই outlier, কারণ বাকি সব ১০-১৩-এর মধ্যে।

### Outlier/Noise কমানোর উপায়

| পদ্ধতি | বর্ণনা |
|---|---|
| **Remove** | যদি স্পষ্ট ভুল হয় (বয়স = 250) |
| **Capping (Winsorization)** | সীমার বাইরের মান সীমায় বসিয়ে দাও |
| **Binning / Smoothing** | Data-কে bin-এ ভাগ করে bin-এর গড় বসানো |
| **Moving Average** | Time-series-এ আশেপাশের মানের গড় |
| **Transformation** | Log transform দিয়ে বড় মানের প্রভাব কমানো |
| **Robust Model** | Random Forest-এর মতো noise-সহনশীল model |

**Binning Example:**

```
Sorted data: [4, 8, 15, 21, 21, 24, 25, 28, 34]

Bin 1: [4, 8, 15]   → গড় 9  → [9, 9, 9]
Bin 2: [21, 21, 24] → গড় 22 → [22, 22, 22]
Bin 3: [25, 28, 34] → গড় 29 → [29, 29, 29]
```

---

## ধাপ ৪: Scaling ও Encoding

| কাজ | পদ্ধতি |
|---|---|
| **Min-Max Scaling** | `x' = (x - min)/(max - min)` → 0 থেকে 1-এর মধ্যে |
| **Standardization** | `x' = (x - mean)/std` |
| **Categorical Encoding** | One-Hot / Label Encoding |

---

## ⚠️ গুরুত্বপূর্ণ সতর্কতা: Data Leakage

**আগে Train/Test split করো, তারপর** preprocessing-এর মান (mean, median) **শুধু training data থেকে** হিসাব করো, এবং সেই মান test data-তেও বসাও। নাহলে test data-র তথ্য model আগেই "দেখে ফেলে", ফলে accuracy কৃত্রিমভাবে বেশি দেখায়।

```
Data ──► Train/Test Split ──► Train থেকে mean বের করো
                                   │
                    ┌──────────────┴──────────────┐
                    ▼                             ▼
             Train-এ বসাও                  Test-এ বসাও (একই মান)
```

---

## সারসংক্ষেপ ছক

| সমস্যা | সমাধান |
|---|---|
| Missing (কম) | Row delete |
| Missing (বেশি column) | Column delete |
| Missing (numeric) | Mean / Median |
| Missing (categorical) | Mode |
| Missing (time-series) | Forward fill / Interpolation |
| Outlier (ভুল data) | Remove |
| Outlier (সত্যি কিন্তু চরম) | Capping / Log transform |
| Noise (ছোট ওঠানামা) | Binning / Moving average |

---

## পরীক্ষার টিপস ✍️

- আগে **Missing ও Noise-এর সংজ্ঞা** লিখবে, তারপর পদ্ধতি
- **Pipeline diagram** আঁকবে (Inspection → Missing → Noise → Scaling)
- **Mean vs Median**-এর পার্থক্য লিখবে: **Outlier থাকলে Median ভালো**
- **IQR formula** (`Q1 - 1.5×IQR`, `Q3 + 1.5×IQR`) মুখস্থ রাখবে
- **Data Leakage** mention করলে extra নম্বর পাওয়া যায়
- ছোট একটি numeric example দিয়ে imputation দেখাবে (`[25, 30, NaN, 28, 35]`)