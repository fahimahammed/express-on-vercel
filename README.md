
# Deploy an Express API on Vercel.

১। Express API  Vercel-এ ডিপ্লয় করার জন্য প্রথমে <a href='https://vercel.com/'>Vercel</a> এ একটি একাউন্ট খুলতে হবে। এখানে sign up করতে GitHub, GitLab or Bitbucket একাউন্ট অবশ্যই ব্যবহার করবেন। 

২। আপনার Express API টি export করুন। index.js file এর শেষে নিচের লাইনটি লিখে দিন। তাহলে export হয়ে যাবে। 
```bash
module.exports = app;
```

৩। আপনার প্রজেক্টে `vercel.json` নামে একটি ফাইল তৈরী করুন এবং সেখানের নিচের কোড গুলো লিখে দিন। 

<img src='https://i.ibb.co/RDmv2zd/a.png' alt="Click on New Project Button"/>

```bash
{
    "version": 2,
    "builds": [
      {
        "src": "index.js",
        "use": "@now/node"
      }
    ],
    "routes": [
      {
        "src": "/(.*)",
        "dest": "index.js"
      }
    ]
}
```

৪। আপনার গিঠাহাবে প্রজেক্টটি পুশ করে দিন। 

৫। তারপর <a href='https://vercel.com/dashboard'>Vercel Dashboard</a>  এই লিঙ্কে গিয়ে `New Project` বাটনে ক্লিক করুন।

<img src='https://i.ibb.co/c1FN0k9/image.jpg' alt="Click on New Project Button"/>


৬। New Project Button এ ক্লিক করার পর নিচের ছবির মতো একটি অপশন দেখতে পাবেন। সেখান থেকে রিপোজিটোরি সিলেক্ট করুন এবং `Import` বাটনে ক্লিক করুন।

<img src='https://i.ibb.co/KNYHhCN/rrrr.png' alt="Click on Import Button"/>

৭। Import বাটনে এ ক্লিক করার পর নিচের ছবির মতো একটি অপশন দেখতে পাবেন। এখানে `Environment Variable` এ ক্লিক করে Environment Variable সেট করে দিন। 

<img src='https://i.ibb.co/VY28hRF/Inked444-LI.jpg' alt="Click on Environment Variable Button"/>

৮। Environment Variable সেট করা হয়ে গেলে `Deploy` বাটনে ক্লিক করে দিন। 
<img src='https://i.ibb.co/PFbCTWr/6666.png' alt="Click on Environment Variable Button"/>

৯। ডিপ্লয় হয়ে গেলে `Go to Dashboard` বাটনে ক্লিক করুন এবং সেখানে আপনার ডিপ্লয় করে প্রজেক্টি দেখতে পাবেন।

<img src='https://i.ibb.co/wc3kzyZ/image.png' alt="Click on Go to Dashboard Button"/>


১০। আপনার প্রজেক্টের উপর ক্লিক করে Visit বাটনে ক্লিক করলে base url টি পেয়ে যাবেন। 
<img src='https://i.ibb.co/Dp7ynvx/image.png' alt="Click on Environment Variable Button"/>

ধন্যবাদ।.
- <a href="https://github.com/fahimahammed/express-on-vercel/blob/main/deploy_in_vercel.md">Vercel</a>
