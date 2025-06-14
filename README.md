## What is Type Inference in TypeScript? Why is it helpful?

**টাইপ ইনফারেন্স** মানে হলো এক কথায় টাইপস্ক্রীপ্ট নিজ থেকে ভ্যারিয়েবল টাইপটা বুঝে ফেলে। আমাদের নিজ থেকে টাইপ ডিফাইন করে দিতে হয় না, যদিও টাইপ ডিফাইন করে দেওয়াই উত্তম।

### টাইপ ইনফারেন্স কিভাবে কাজ করে?  
ছোট একটা উদাহরণ দিয়ে বোঝানোর চেষ্টা করি:

```ts
const name = "Farsi";
```
এখানে আমি name এটা কি টাইপের হবে সেটা উল্লেখ করে দেইনি, উল্লেখ করে না দেওয়া সত্ত্বেও টাইপস্ক্রীপ্ট বুঝে নিবে এটা স্ট্রিং টাইপের ভ্যারিয়েবল।

**টাইপ ইনফারেন্স ব্যবহারের সুবিধা হলো:**
1. আমার কোডে কোনো ভুল করলে সেটা ধরে দিবে (লাল দাগ শো হবে )
2. সব সময় টাইপ ডিফাইন করার প্রয়োজন হয়না বলে কোড ছোট হয় । ( বড় অ্যাপ্লিকেশন এর ক্ষেত্রে ডিফাইন করা ভালো)

## Explain the difference between any, unknown, and never types in TypeScript.

**Any , Unknown,Never তিনটি টাইপের মধ্যে পার্থক্য গুলো তুলে ধরা হলো:** 

**Any Type:** এটি এমন এক ধরনের টাইপ যেখানে আমরা চাইলেই যেকোনো ধরনের টাইপের মান এসাইন করতে পারি। এটি সম্পূর্নরূপে টাইপক্রিপ্ট  কম্পাইলারকে টাইপ চেক করা বন্ধ করে দে। এটি টাইপক্রিপ্ট এর টাইপ সেফটি হারিয়ে ফেলে।

**কখন ব্যবহার করা হয়:** যখন আমাদের টাইপ চেকিং প্রয়োজন পড়ে না এবং ডায়নামিক ডাটা রাখলে ইউজ করা হয়। 

**Unknown Type:** এটি প্রায় any type এর মতন কিন্তু unknown type ইউজ করলে টাইপ সেফটি দেওয়া যায়। এখানে চাইলেই any type এর মতন ডাটা রাখা যায় কিন্তু ব্যবহার করার সময় টাইপ কি চেক করা লাগবে। ভ্যালু কি আসবে জানিনা কিন্তু কি আসবে সেটা চেক করে টাইপ সেফটি দেওয়া যায়।

**Never Type:**  এটি এমন একটি টাইপ, যা কখনো কোনো ভ্যালু রিটার্ন করে না।যখন কোনো ফাংশন ভ্যালু রিটার্ন করে না (error throw করে ) সেক্ষেত্রে never type ইউজ করতে পারি। অর্থাৎ never type এমন একটি মানকে প্রকাশ করে যা কখনো ঘটবে না ।
**কখন ব্যবহার করা হয়:** যখন  এমন ফাংশন তৈরি করা হয় যা কখনোই কোন মান রিটার্ন করে না, উদাহরণস্বরূপ, throw error বা infinite loops
