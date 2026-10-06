# First Format — Topic + প্রশ্নের বাংলা অনুবাদ

**Topic:** Data Communication & Networking → Channel Capacity → Shannon Capacity Formula

### প্রশ্নের বাংলা অনুবাদ

একটি telephone line-এর bandwidth সাধারণত **3000 Hz (300 Hz থেকে 3300 Hz)**, যা data communication-এর জন্য ব্যবহৃত হয়। এই channel-এর **SNR = 3162**।

প্রশ্ন: এই channel-এর **maximum capacity কত হবে?**

---

# Second Format — Answer Only for Exam

Using Shannon’s Capacity Formula:

$$
C = B \log_2(1+SNR)
$$

Given,

$$
B = 3000 \text{ Hz}
$$

$$
SNR = 3162
$$

Therefore,

$$
C = 3000 \log_2(1+3162)
$$

$$
C = 3000 \log_2(3163)
$$

$$
C \approx 3000 \times 11.627
$$

$$
\boxed{C \approx 34881 \text{ bps}}
$$

So, the channel capacity is approximately:

$$
\boxed{34.9\text{ kbps}}
$$

### বাংলা অনুবাদ

Shannon formula অনুযায়ী channel-এর সর্বোচ্চ capacity প্রায়:

$$
\boxed{34881 \text{ bps}}
$$

অথবা প্রায়:

$$
\boxed{34.9 \text{ kbps}}
$$

---

# Third Format — Basic Topic-wise Explanation in Bangla

## 1. Channel Capacity কী?

**Channel Capacity** হলো একটি communication channel দিয়ে theoretically সর্বোচ্চ কত bit per second data reliably পাঠানো সম্ভব।

এর unit:

$$
bps = bits\ per\ second
$$

যেমন:

```text
Capacity = 34,881 bps
```

মানে theoretically প্রতি second-এ প্রায় **34,881 bit** পাঠানো সম্ভব।

---

## 2. Bandwidth কী?

Bandwidth হলো channel যে frequency range support করে।

Question-এ:

$$
300\text{ Hz থেকে }3300\text{ Hz}
$$

তাই bandwidth:

$$
B = 3300 - 300
$$

$$
B = 3000\text{ Hz}
$$

অর্থাৎ:

$$
\boxed{B=3000\text{ Hz}}
$$

---

## 3. SNR কী?

**SNR = Signal-to-Noise Ratio**

এটি বোঝায় signal কতটা শক্তিশালী noise-এর তুলনায়।

Formula:

$$
SNR=\frac{Signal\ Power}{Noise\ Power}
$$

এখানে:

$$
SNR=3162
$$

SNR যত বেশি হবে, সাধারণত channel তত বেশি data carry করতে পারবে।

---

## 4. Shannon Capacity Formula

Noise আছে এমন communication channel-এর maximum theoretical capacity বের করতে Shannon formula ব্যবহার করা হয়:

$$
\boxed{C=B\log_2(1+SNR)}
$$

যেখানে:

* \(C\) = Channel Capacity in bps
* \(B\) = Bandwidth in Hz
* \(SNR\) = Signal-to-Noise Ratio

---

## 5. এখন Value বসাই

Given:

$$
B=3000
$$

$$
SNR=3162
$$

তাই:

$$
C=3000\log_2(1+3162)
$$

প্রথমে:

$$
1+3162=3163
$$

তাই:

$$
C=3000\log_2(3163)
$$

এখন:

$$
\log_2(3163)\approx11.627
$$

তাই:

$$
C=3000\times11.627
$$

$$
C\approx34881\text{ bps}
$$

অর্থাৎ:

$$
\boxed{C\approx34.9\text{ kbps}}
$$

---

## 6. 1 কেন যোগ করা হয়?

Shannon formula নিজেই:

$$
C=B\log_2(1+SNR)
$$

তাই SNR সরাসরি `3162` বসিয়ে:

$$
\log_2(3162)
$$

করলে technically ভুল হবে।

Correct:

$$
\boxed{\log_2(1+3162)=\log_2(3163)}
$$

---

## 7. SNR যদি dB-তে দেওয়া থাকত?

এখানে SNR সরাসরি ratio হিসেবে দেওয়া:

$$
SNR=3162
$$

তাই conversion প্রয়োজন নেই।

কিন্তু যদি দেওয়া থাকত:

$$
SNR_{dB}=35dB
$$

তখন আগে ratio বের করতে হতো:

$$
SNR=10^{SNR_{dB}/10}
$$

যেমন:

$$
10^{35/10}=10^{3.5}\approx3162
$$

অর্থাৎ এই প্রশ্নের `3162` প্রায় **35 dB SNR**-এর সমান।

---

## Govt Job Exam Shortcut

মনে রাখুন:

> **Noisy Channel → Shannon Formula**

$$
\boxed{C=B\log_2(1+SNR)}
$$

এই প্রশ্নে:

$$
3000 \times \log_2(3163)
$$

$$
\boxed{\approx34.9\text{ kbps}}
$$

**Final Answer: \(\boxed{34.9\text{ kbps}}\)**
