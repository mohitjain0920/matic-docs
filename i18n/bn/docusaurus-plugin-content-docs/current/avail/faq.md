---
id: faq
title: FAQ
sidebar_label: FAQ
description: Polygon Avail সম্পর্কে প্রায়শই জিজ্ঞাসিত প্রশ্নাবলী
keywords:
  - docs
  - polygon
  - avail
  - availability
  - client
  - consensus
  - faq
image: https://wiki.polygon.technology/img/thumbnail/polygon-avail.png
slug: faq
---

# প্রায়শই জিজ্ঞাসিত প্রশ্নাবলী {#frequently-asked-questions}

:::tip

যদি আপনি এই পৃষ্ঠায় আপনার প্রশ্ন পাবেন না, তাহলে দয়া করে **[<ins>Polygon Avail</ins>](https://discord.gg/jXbK2DDeNt)** Discord-এ আপনার প্রশ্ন জমা দিন।

:::

## একটি হালকা ক্লায়েন্ট কী? {#what-is-a-light-client}

লাইট ক্লায়েন্ট ব্যবহারকারীদের বিকেন্দ্রীকরণ এবং নিরাপত্তা বজায় রাখার সময় পূর্ণ ব্লকচেইন সিঙ্ক না করে একটি ব্লকচেইন নেটওয়ার্কের সাথে ইন্টারঅ্যাক্ট করতে অনুমতি দেয়। সাধারণত, তারা ব্লকচেইন হেডার ডাউনলোড করে, কিন্তু প্রতিটি ব্লকের বিষয়বস্তু নয়। অধিগ্রহণ (DA) হালকা ক্লায়েন্ট অতিরিক্তভাবে যাচাই করে যে ডাটা প্রাপ্যতা স্যাম্পলিং করে ব্লক বিষয়বস্তু পাওয়া যাবে, একটি কৌশল যেখানে একটি ব্লকের ছোট র্যান্ডম বিভাগ ডাউনলোড করা আছে।

## একটি হালকা ক্লায়েন্টের একটি জনপ্রিয় ব্যবহার কী? {#what-is-a-popular-use-case-of-a-light-client}

অনেক use-cases রয়েছে যা আজ একটি সম্পূর্ণ নোড বজায় রাখার জন্য একটি on নির্ভর করে, যেমন একটি ব্লকচেইনের শেষ ব্যবহারকারীরা সরাসরি ব্লকচেইনের সাথে যোগাযোগ করে না, বরং intermediary মাধ্যমে লাইট clients ে এখন পর্যন্ত এই আর্কিটেকচারের জন্য উপযুক্ত প্রতিস্থাপন until  কারণ তাদের ডাটা ছিল ডেটা উপলভ্যতার নিশ্চয়তার অভাব ছিল। লাভ এই সমস্যাটি সমাধান করে, এইভাবে মধ্যস্থ. ে ছাড়া ব্লকচেইন নেটওয়ার্কে সরাসরি অংশগ্রহন করতে আরও বেশি অ্যাপ্লিকেশন সক্ষম করে। যদিও Avail পূর্ণ নোড সমর্থন করে না, তবে আমরা আশা করি যে বেশিরভাগ অ্যাপ্লিকেশন একটি চালানোর প্রয়োজন হবে না, বা কয়েক জন রান করতে হবে।

## ডেটা উপলভ্যতা নমুনা কী? {#what-is-data-availability-sampling}

অন্যান্য হালকা ক্লায়েন্টদের মতো হালকা ক্লায়েন্টদের পাবেন , শুধুমাত্র ব্লকচেইনের হেডার ডাউনলোড করুন। যাইহোক, তারা অতিরিক্ত ডাটা প্রাপ্যতা স্যাম্পলিং সম্পাদন করে: একটি কৌশল যা এলোমেলোভাবে ব্লক ডেটার ছোট বিভাগে নমুনা করে এবং যাচাই করে যে তারা সঠিক আছে। যখন ইসরার কোডিং এবং কেট পলিনোমিয়াল কমিটমেন্টে মিলিত When তখন এগিয়েছে ক্লায়েন্ট জালিয়াতি প্রুফে নির্ভর না করে শক্তিশালী (প্রায় 100%) গ্যারান্টি প্রদান করতে সক্ষম এবং শুধুমাত্র একটি ছোট ধ্রুবক সংখ্যার প্রশ্নের সাথে।

## ডেটা উপলভ্যতার নিশ্চয়তা বাড়ানোর জন্য ইরেজার কোডিং কীভাবে ব্যবহার করা হয়? {#how-is-erasure-coding-used-to-increase-data-availability-guarantees}

Erasure কোডিং একটি কৌশল যা একাধিক "শার্ড" এর উপর তথ্য ছড়িয়ে দেয় এমন একটি পদ্ধতিতে ডেটা এনকোড করে, যেমন যে এই of কিছু সংখ্যক ক্ষতি সহ্য করা যেতে পারে। অর্থাৎ এই তথ্যটি অন্যান্য shards. থেকে পুনর্নির্মাণ করা যেতে পারে। ব্লকচেইনে প্রয়োগ করা Applied , এর মানে হল যে আমরা প্রতিটি ব্লকের আকার কার্যকরভাবে বাড়িয়ে দেই, কিন্তু আমরা একটি malicious িক অভিনেতাকে অপ্রয়োজনীয় শর্ট আকারের অবধি একটি ব্লকের যে কোন অংশ লুকিয়ে রাখতে সক্ষম being ।

যেহেতু একটি malicious া অভিনেতা একটি একক লেনদেন লুকিয়ে রাখার জন্য ব্লকের একটি বড় অংশ লুকিয়ে রাখতে হবে, তাই এটি আরও বেশি সম্ভাবনা দেয় যে র্যান্ডম স্যাম্পলিং ডাটাতে বড় ফাঁক ধরবে। কার্যকরীভাবে, কোডিং মুছে ফেলুন ডেটা availibility স্যাম্পলিং কৌশল আরও শক্তিশালী করে তোলে।

## Kate কমিটমেন্ট কী? {#what-are-kate-commitments}

অনিকেত কেট, গ্রেগরি এম জাভেরুচা এবং ইয়ান গোল্ডবার্গ 2010 সালে Kate কমিটমেন্ট চালু করে, ফলে
সংক্ষিপ্তভাবে পলিনমিয়ালে কমিট করা সম্ভব হয়। সম্প্রতি, পলিনমিয়াল কমিটমেন্টের জনপ্রিয়তা অনেক বেড়ে যায়
এবং PLONK-এর মতো শূন্য জ্ঞান নির্মাণের কমিটমেন্ট হিসাবে প্রাথমিকভাবে ব্যবহার করা হচ্ছে।

আমাদের নির্মাণে আমরা নিম্নলিখিত কারণে Kate কমিটমেন্ট ব্যবহার করি:

- এটা আমাদেরকে মানগুলোকে ব্লক হেডারের ভিতরের রাখার জন্য সংক্ষিপ্ত পদ্ধতিতে কমিট করার সুবিধা প্রদান করে।
- সংক্ষিপ্ত ওপেনিং সম্ভব, যা হালকা ক্লায়েন্টকে উপলভ্যতা যাচাই করতে সহায়তা করে।
- ক্রিপ্টোগ্রাফিক বাইন্ডিং প্রপার্টি ভুল কমিটমেন্টকে কম্পিউটেশনালি কঠিন করে তোলার মাধ্যমে জালিয়াতির প্রমাণ এড়াতে
আমাদেরকে সাহায্য করে।

ভবিষ্যতে আমরা অন্যান্য পলিনমিয়াল কমিটমেন্ট স্কিম ব্যবহার করতে পারি, যদি তা আমাদের ভালো বাউন্ড বা গ্যারান্টি প্রদান করে।

## যেহেতু Avail একাধিক অ্যাপ্লিকেশন দ্বারা ব্যবহার করা হয়, তাই এর মানে কি চেইনকে অন্যান্য চেইন থেকে লেনদেন ডাউনলোড করতে হবে? {#since-avail-is-used-by-multiple-applications-does-that-mean-chains-have-to-download-transactions-from-other-chains}

না। অ্যাওয়ে হেডার একটি সূচক ধারণ করে যা একটি প্রদত্ত অ্যাপ্লিকেশন নির্ধারণ এবং একটি ব্লকের শুধুমাত্র বিভাগে ডাউনলোড করতে পারে যা সেই অ্যাপ্লিকেশনের জন্য ডেটা ধারণ করে। সুতরাং, তারা একই সময়ে বা ব্লক মাপের মাধ্যমে Avail ব্যবহার করে অন্যান্য চেইনে মূলত অপ্রভাবিত হয়।

একমাত্র ব্যতিক্রম হল ডেটা উপলভ্যতার নমুনা। তথ্য পাওয়া গেছে তা যাচাই করার জন্য (এবং erasure coding প্রকৃতির কারণে), ক্লায়েন্ট at ব্লকের ছোট অংশ নমুনা করে, যার মধ্যে রয়েছে সম্ভাব্য বিভাগে অন্যান্য অ্যাপ্লিকেশনের জন্য ডেটা ধারণ করে।