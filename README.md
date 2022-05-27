# Deploy an Express API on Vercel.

১। Express API  Vercel-এ ডিপ্লয় করার জন্য প্রথমে Vercel ( `https://vercel.com/` ) এ একটি একাউন্ট খুলতে হবে। এখানে sign up করতে GitHub, GitLab or Bitbucket একাউন্ট অবশ্যই ব্যবহার করবেন। 

২। আপনার Express API টি export করুন। index.js file এর শেষে নিচের লাইনটি লিখে দিন। তাহলে export হয়ে যাবে। 
```bash
module.exports = app;
```

৩। আপনার প্রজেক্টে `vercel.json` নামে একটি ফাইল তৈরী করুন এবং সেখানের নিচের কোড গুলো লিখে দিন। 
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

৪। তারপর https://vercel.com/dashboard এই লিঙ্কে গিয়ে `New Project` বাটনে ক্লিক করুন। 
<img src='https://i.ibb.co/c1FN0k9/image.jpg' alt="Click on New Project Button"/>