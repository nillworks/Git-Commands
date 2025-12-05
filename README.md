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

