### 1️⃣ Git Setup
```bash
git --version
git config --get user.name
git config --get user.email
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

2️⃣ Initialize New Repository
git init
git remote add origin <repository-url>

3️⃣ File Operations
touch index.html       # নতুন ফাইল তৈরি
ls -la                 # Hidden files/folders দেখা
cat filename           # ফাইলের content দেখা


4️⃣ Stage & Commit
git status
git add -A
git reset             # Unstage করা
git commit -m "Initial commit"

5️⃣ Branch Management
git branch            # Branch list
git branch branchName # নতুন branch
git checkout branchName           # Switch branch
git checkout -b branchName        # Create + switch
git branch -f master main         # master কে main-এর মতো বানানো
git merge master                  # master merge into main
git cherry-pick <commit-id>       # Specific commit transfer

6️⃣ Push & Pull
git pull
git push origin main
git push origin master --force

7️⃣ Reset / Delete Files
git reset --hard          # Last commit এ ফিরে যাওয়া
git rm filename -f        # Permanently file delete
rm -rf folderName         # Folder delete

1️⃣ Short commit ID & One-line log
git log --oneline

শুধু last 5 commit দেখাতে:
git log --oneline -5

একটি branch specific log দেখতে:
git log --oneline main

3️⃣ Extra: Graph সহ দেখানো
git log --oneline --graph --decorate

এতে branch structure এবং commit history সুন্দরভাবে দেখাবে।

💡 Tip:
যখন git cherry-pick বা git reset করতে হবে, short commit ID ব্যবহার করুন।
git log --oneline সব সময় fast এবং readable।


🎗️main branch-এর সব code/content যেন একদম same ভাবে master branch-এ চলে আসে।
এই কাজটা করার সবচেয়ে safe এবং সঠিক উপায়
git checkout master
git merge main
git push origin master

এর মানে:
আগে master এ যাবে
main এর কোড master এ মিশাবে
GitHub-এ আপডেট পাঠাবে ✅


🔁 Option 1: main → master (সবচেয়ে সহজ ও safe)
1️⃣ আগে master branch-এ যাও
git checkout master

2️⃣ এখন main branch-এর code master-এ merge করো
git merge main


👉 যদি কোনো conflict না থাকে, তাহলে main-এর সব code এখন master-এ চলে যাবে ✅

3️⃣ এখন remote (GitHub)-এ push করো
git push origin master


