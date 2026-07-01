📘 Module 05 — Mockoon Banking API Simulation
Section A: Building Your First n8n Workflow

📌 S — Scenario

Nord Bank-এর Automation Engineer প্রথমবার n8n খুলেছে। Interface দেখে মনে হচ্ছে অনেক কিছু আছে — Node, Canvas, Execution। কোথা থেকে শুরু করতে হবে এবং কীভাবে একটি সহজ Workflow তৈরি করতে হয় তা স্পষ্ট নয়।

🎯 T — Task

n8n-এর Visual Builder বোঝা হবে এবং প্রথম Workflow তৈরির ধারণা পাওয়া হবে:

- n8n Interface-এর তিনটি প্রধান অংশ
- Node কী এবং কীভাবে Connect করতে হয়
- Workflow চালানো এবং Save করার পদ্ধতি

👀 O — Output

এই Module শেষে থাকবে:

- n8n Interface সম্পর্কে স্পষ্ট ধারণা
- Node যুক্ত করা ও Connect করার প্রক্রিয়া বোঝা
- একটি সহজ Workflow তৈরির আত্মবিশ্বাস

🤔 R — Reason

Concept Explanation

n8n Interface-এর তিনটি প্রধান অংশ:

| অংশ | → | Simple Explanation |
|---|---|---|
| Node Palette (বাম দিকে) | → | সব Available Node-এর তালিকা — HTTP Request, Email, IF, Function ইত্যাদি |
| Canvas (মাঝখানে) | → | Workflow তৈরি করার জায়গা — এখানে Node রেখে Connect করতে হয় |
| Properties Panel (ডান দিকে) | → | Selected Node-এর Settings পরিবর্তন করার জায়গা |

Node কী

Node → n8n Workflow-এর একটি Block, যা একটি নির্দিষ্ট কাজ করে। যেমন HTTP Request Node শুধু API Call করে, Email Node শুধু Email পাঠায়।

Workflow তৈরির প্রক্রিয়া:

| ধাপ | → | Simple Explanation |
|---|---|---|
| Node Drag করা | → | Palette থেকে Node টেনে Canvas-এ রাখা |
| Node Connect করা | → | একটি Node-এর Output-এ Click করে আরেকটির Input-এ যুক্ত করা |
| Parameter Configure করা | → | Properties Panel-এ URL, Method, Email Address ইত্যাদি দেওয়া |

Workflow চালানোর ধরন:

| Type | → | Simple Explanation |
|---|---|---|
| Manual Trigger | → | নিজে Button Press করে চালানো — Testing-এর জন্য |
| Schedule Trigger | → | নির্দিষ্ট সময়ে Automatic চালানো — যেমন প্রতিদিন রাত ২টায় |
| Webhook Trigger | → | কোনো Event ঘটলে Automatic চালানো — যেমন নতুন Transaction হলে |

কেন এই ধারণা প্রয়োজন?

n8n-এর Interface বোঝা ছাড়া Complex Banking Workflow তৈরি সম্ভব নয়। এই তিনটি অংশ এবং Node-এর ধারণা হলো বাকি সব Module-এর ভিত্তি।

🏦 Real-World Use Case

Nord Bank-এর NOC Team একটি n8n Workflow তৈরি করেছে যেখানে Schedule Trigger প্রতি ৫ মিনিটে চালু হয়, HTTP Request Node Mockoon API থেকে Device Status আনে, এবং IF Node দেখে কোনো Device Offline আছে কিনা। Offline থাকলে Email Node Alert পাঠায়।

🧠 Memory Tip

n8n Workflow মনে রাখার সহজ উপায়:
**Trigger → Action → Action → Action**
(কখন শুরু হবে → কী করবে → কী করবে → কী করবে)

✋ Y — Your Turn

নিজের ভাষায় ৩-৪ লাইনে ব্যাখ্যা করুন (Example কপি না করে):

একটি Banking Scenario চিন্তা করুন যেখানে Manual Trigger ব্যবহার করা উচিত, এবং আরেকটি যেখানে Schedule Trigger বেশি উপযুক্ত। কেন এই পার্থক্য করলেন তা ব্যাখ্যা করুন।

🎯 Deliverable: First Workflow Quiz সম্পন্ন করা

---
ℹ️ Note: এই Default Mode-এ শুধু Concept আলোচনা করা হয়েছে। n8n Interface-এ Hands-on Practice, Node Configuration, এবং First Workflow Build করার জন্য /lab Mode ব্যবহার করতে পারেন।