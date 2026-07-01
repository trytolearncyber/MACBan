📘 Module 04 — Banking API Integration Architecture
Section A: Understanding APIs and Webhooks

📌 S — Scenario

Nord Bank-এর Automation Engineer n8n দিয়ে Core Banking System-এর সাথে যোগাযোগ করতে চায় — যেমন Account Balance চেক করা বা নতুন Transaction পাঠানো। কিন্তু "API কীভাবে কাজ করে" এবং "Webhook কী" তা স্পষ্ট না থাকলে সঠিকভাবে Integration ডিজাইন করা যাবে না।

🎯 T — Task

আজকে শেখা হবে:

- REST API-এর মূল ধারণা
- Webhook কী এবং এটি API থেকে কীভাবে আলাদা
- API Authentication-এর সাধারণ পদ্ধতি
- Postman দিয়ে API Test করার ধারণা

👀 O — Output

এই Module শেষে থাকবে:

- API এবং Webhook-এর মধ্যে পার্থক্য স্পষ্টভাবে বোঝা
- HTTP Method ও Status Code-এর সাধারণ ধারণা
- API Authentication Method-গুলোর পরিচিতি

🤔 R — Reason

Concept Explanation

API → দুটি System-এর মধ্যে Data আদান-প্রদানের পদ্ধতি। একটি System আরেকটি System-কে "Request" পাঠায়, এবং উত্তরে "Response" পায়।

REST API Basics

| Element | → | Simple Explanation |
|---|---|---|
| HTTP Methods | → | GET (Data আনা), POST (নতুন Data পাঠানো), PUT (Update করা), DELETE (মুছে ফেলা) |
| Status Codes | → | Server-এর উত্তর কেমন হলো তা বোঝানোর সংখ্যা — 200 (সফল), 401 (Authentication বাকি), 404 (পাওয়া যায়নি), 500 (Server-এ সমস্যা) |
| JSON Format | → | Data পাঠানো-আনার জন্য একটি সহজ, Structured Text Format |

Webhook কী

Webhook → কোনো Event ঘটলে System নিজে থেকেই Notification পাঠায়। 

API আর Webhook-এর মূল পার্থক্য:

| Concept | → | Simple Explanation |
|---|---|---|
| API (Pull) | → | তুমি গিয়ে জিজ্ঞাসা করো — "Balance কত?" |
| Webhook (Push) | → | System নিজে থেকে বলে দেয় — "Transaction হয়ে গেছে!" |

API Authentication Methods

| Method | → | Simple Explanation |
|---|---|---|
| API Keys | → | একটি Fixed Secret Code দিয়ে Identity প্রমাণ করা |
| OAuth2 | → | Temporary Token-এর মাধ্যমে Secure Access দেওয়া |
| Certificate-based | → | Digital Certificate দিয়ে দুই System একে অপরকে চেনে |

কেন এই বিষয়গুলো গুরুত্বপূর্ণ?

Banking System-এ ভুল Authentication ব্যবহার করলে Sensitive Data Leak হতে পারে। তাই API ও Webhook-এর সঠিক ব্যবহার Banking Integration-এর ভিত্তি।

🏦 Real-World Use Case

Nord Bank-এ Balance Inquiry করার জন্য Core Banking System-এর REST API ব্যবহার করতে হয় (Pull পদ্ধতি)। আবার যখন কোনো ATM Transaction হয়, তখন Customer-কে SMS Notification পাঠাতে Webhook ব্যবহার করা হয় (Push পদ্ধতি) — System নিজে থেকেই জানিয়ে দেয়।

🧠 Memory Tip

**API = তুমি জিজ্ঞাসা করো** (Pull)
**Webhook = System নিজে বলে** (Push)

✋ Y — Your Turn

নিজের ভাষায় ৩-৪ লাইনে ব্যাখ্যা করুন (Example কপি না করে):

একটি Banking Scenario চিন্তা করুন যেখানে Webhook ব্যবহার করা উচিত, এবং আরেকটি Scenario যেখানে সাধারণ API (GET Request) ব্যবহার করা উচিত। কেন এই পার্থক্য করলেন তা ব্যাখ্যা করুন।

🎯 Deliverable: API Quiz সম্পন্ন করা

---
ℹ️ Note: এই Default Mode-এ শুধু Concept আলোচনা করা হয়েছে। Postman দিয়ে Actual API Testing, Authentication Configuration, এবং Code-এর জন্য `/answer` বা `/lab` Mode ব্যবহার করতে পারেন।