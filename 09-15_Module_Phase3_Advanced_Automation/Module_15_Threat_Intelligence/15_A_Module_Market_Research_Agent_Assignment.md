📘 Module 15 — Market Research Multi-Agent System (n8n)
📌 S — Scenario
Nord Bank-এর Security Team একটা নতুন Threat সম্পর্কে জানতে চাইলে, একজন Analyst-কে Manually একাধিক Source (Security Blog, CVE Database, News) খুঁজে, তথ্য একসাথে করে, তারপর একটা Report লিখতে হয় — পুরো Process-এ কয়েক ঘণ্টা লাগে।
🚨 Challenge

একাধিক Source থেকে তথ্য সংগ্রহ করা Time-Consuming
তথ্য সংগ্রহ, বিশ্লেষণ, এবং Report লেখা — তিনটা ভিন্ন ধরনের কাজ, একজন মানুষের সব কাজ Manually করতে সময় লাগে
নতুন Threat দ্রুত ছড়ায়, কিন্তু Manual Research-এর গতি সেই সাথে তাল মেলাতে পারে না

✅ Solution
n8n দিয়ে একটা Multi-Agent Research System তৈরি করা যায়, যেখানে আলাদা আলাদা Agent Data Collect করবে, Analyze করবে, এবং Report Generate করবে — একসাথে, Coordinated ভাবে।
🎯 T — Task
আজকের Learning Objective হলো Multi-Agent Research System-এর Basic Component বুঝা।
ছোট ছোট ধাপ:

Data Collection Agent কী করে তা বুঝা
Data Analysis Agent কী করে তা বুঝা
Report Generation Agent কী করে তা বুঝা

👀 O — Output
Concept→Simple ExplanationData Collection Agent→একাধিক Source থেকে Raw তথ্য সংগ্রহ করাData Analysis Agent→সংগৃহীত তথ্য থেকে গুরুত্বপূর্ণ Pattern/Insight বের করাReport Generation Agent→Analysis-এর ভিত্তিতে একটা Readable Report তৈরি করা
🤔 R — Reason
Multi-Agent Research System ব্যবহার করার কারণ:

একাধিক Source থেকে Data সংগ্রহ সমান্তরালে (Parallel) হতে পারে, একটার পর একটা Manually না করে
Collection, Analysis, Reporting — কাজগুলো আলাদা থাকায় প্রতিটা Agent নিজের কাজে Optimize করা যায়

Main flaw এখানে সরাসরি বলা দরকার: Data Collection Agent যদি ভুল বা Low-Quality Source থেকে তথ্য টানে (যেমন Unverified Blog, Outdated Advisory), Analysis Agent সেই ভুল Data-কেই সঠিক ধরে নিয়ে বিশ্লেষণ করবে। এই System-এ কোনো নিজস্ব "Fact-Checking" ক্ষমতা নেই — এটা শুধু Source-এর Volume ও Speed বাড়ায়, Source-এর Reliability যাচাই করে না। ফলে "দ্রুত Report" পাওয়া যাবে, কিন্তু সেটা "সঠিক Report" তার Guarantee নেই।
📊 Simple Diagram
[Multiple Sources: Blog, CVE DB, News]
                │
      [Data Collection Agent]
                │
      [Data Analysis Agent] — Pattern/Insight বের করা
                │
      [Report Generation Agent] — Final Report
🏦 Real-World Use Case
Loan Approval System-এ একাধিক Approver-এর কাজ auto করার মতোই এখানেও একাধিক Agent সমান্তরালে কাজ করে — তবে Loan Approval-এর প্রতিটা Step-এ একটা Verifiable Rule থাকে (যেমন Credit Score Threshold), যেখানে Threat Research-এ Source-এর Truthfulness যাচাই করার কোনো Automatic Rule নেই। এই পার্থক্যটা বোঝা জরুরি — সব Multi-Agent System একই রকম Reliable না।
🧠 Memory Tip
Fast ≠ Accurate — Multi-Agent System Speed বাড়ায়, কিন্তু Source Verification আলাদা করে যোগ না করলে Accuracy বাড়ে না।

✋ Y — Your Turn
নিজের ভাষায় লিখুন (Copy না করে):

Data Collection Agent কোন Source থেকে তথ্য নেবে তার একটা "Trusted Source List" যদি বানাতে হয়, সেখানে কী কী Criteria দিয়ে একটা Source-কে "Trusted" বলে ধরবেন?
যদি দুইটা ভিন্ন Source একই Topic-এ পরস্পরবিরোধী তথ্য দেয় (একটা বলছে Threat Critical, আরেকটা বলছে Low), Analysis Agent-কে কীভাবে এই Conflict Handle করতে বলবেন?