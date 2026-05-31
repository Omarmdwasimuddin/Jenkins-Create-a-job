# 🔧 Jenkins — Create a job

> **লক্ষ্য:** Jenkins-এ প্রথম Freestyle Job তৈরি করা এবং Console Output দেখা।

---

## 📋 ধাপসমূহ (Overview)

| ধাপ | কাজ |
|-----|-----|
| ১ | নতুন Job তৈরি করা |
| ২ | Build Step যোগ করা |
| ৩ | Build চালানো |
| ৪ | Console Output দেখা |
| ৫ | Build History দেখা |

---

## ধাপ ১ — নতুন Job তৈরি করা

### ✅ করণীয়:

1. Jenkins Dashboard-এ যাও
2. **`Create a job`** বাটনে ক্লিক করো

   > 📌 অথবা বাম পাশের মেনু থেকে **"New Item"** সিলেক্ট করো

3. **Item name** দাও:
   ```
   Hello World
   ```

4. Project type হিসেবে **`Freestyle project`** সিলেক্ট করো

   ```
   ○  Freestyle project   ← এটা সিলেক্ট করো
   ○  Pipeline
   ○  Multi-configuration project
   ```

5. **`OK`** বাটনে ক্লিক করো

---

## ধাপ ২ — Build Step যোগ করা

### ✅ করণীয়:

1. Configuration পেজে নিচে স্ক্রল করে **`Build Steps`** সেকশনে যাও

2. **`Add build step`** বাটনে ক্লিক করো

3. ড্রপডাউন থেকে **`Execute Windows batch command`** সিলেক্ট করো

   ```
   ┌─────────────────────────────────────┐
   │  Execute Windows batch command       │
   └─────────────────────────────────────┘
   ```

4. **Command** বক্সে নিচের কমান্ডটি লেখো:

   ```batch
   echo Hello, World from jenkins!
   ```

5. **`Save`** বাটনে ক্লিক করো

---

## ধাপ ৩ — Build চালানো

### ✅ করণীয়:

1. Job পেজে বাম পাশের মেনু থেকে **`Build Now`** বাটনে ক্লিক করো

   ```
   📌 Build Now   ← ক্লিক করো
   ```

2. নিচে **Build History** সেকশনে একটি নতুন build দেখা যাবে

3. Build সফল হলে **🟢 সবুজ বৃত্ত** দেখাবে — সেটাতে ক্লিক করো

   ```
   Build History
   ─────────────
   🟢  #1   (এখানে ক্লিক করো)
   ```

---

## ধাপ ৪ — Console Output দেখা

### ✅ করণীয়:

1. Build নম্বরে ক্লিক করার পর বাম পাশে **`Console Output`** অপশনে ক্লিক করো

2. নিচের মতো Output দেখা যাবে:

   ```
   ┌──────────────────────────────────────────────────┐
   │  Console Output                                   │
   ├──────────────────────────────────────────────────┤
   │  Started by user admin                            │
   │  Building in workspace C:\...                     │
   │                                                   │
   │  C:\...> echo Hello, World from jenkins!          │
   │  Hello, World from jenkins!                       │
   │                                                   │
   │  Finished: SUCCESS ✅                             │
   └──────────────────────────────────────────────────┘
   ```

> 🎉 **"Hello, World from jenkins!"** দেখা গেলে — Build সফল হয়েছে!

---

## ধাপ ৫ — Build History দেখা

### ✅ করণীয়:

1. উপরের **`Jenkins`** লোগো বা Home আইকনে ক্লিক করো — Dashboard-এ ফিরে যাও

2. **`Build History`** সেকশনে সমস্ত আগের Build-এর তালিকা দেখা যাবে

   ```
   Build History
   ─────────────────────────────────
   🟢  Hello World » #1    (সফল)
   ```

---

## 🗺️ পুরো Flow একনজরে

```
Dashboard
   │
   ▼
Create a job
   │
   ▼
Item Name: "Hello World"
   │
   ▼
Freestyle Project → OK
   │
   ▼
Build Steps → Add build step
   │
   ▼
Execute Windows batch command
   │
   ▼
Command: echo Hello, World from jenkins!
   │
   ▼
Save
   │
   ▼
Build Now
   │
   ▼
🟢 Build #1 (সবুজ বৃত্ত) → Console Output
   │
   ▼
"Hello, World from jenkins!" ✅
   │
   ▼
Jenkins → Build History
```

---

## ⚠️ সাধারণ সমস্যা ও সমাধান

| সমস্যা | কারণ | সমাধান |
|--------|------|--------|
| 🔴 Build ব্যর্থ হয়েছে | Command ভুল লেখা | `echo Hello, World from jenkins!` সঠিকভাবে লেখো |
| Build দেখা যাচ্ছে না | Page Refresh দরকার | Browser Refresh করো (F5) |
| Console Output খালি | Build শেষ হয়নি | কিছুক্ষণ অপেক্ষা করো |

---

## 📝 মূল বিষয় (Key Takeaways)

- ✅ Jenkins-এ **Freestyle project** দিয়ে সহজে Job তৈরি করা যায়
- ✅ **Execute Windows batch command** দিয়ে যেকোনো CMD কমান্ড চালানো যায়
- ✅ **Console Output** দেখে Build সফল হয়েছে কিনা বোঝা যায়
- ✅ **Build History** থেকে সব আগের Build ট্র্যাক করা যায়

---

*📌 এই Tutorial টি Jenkins-এর প্রথম ধাপ। এরপর Pipeline, Plugins, এবং Automated Testing শেখা যাবে।*
