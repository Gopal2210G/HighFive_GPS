# HighFive
### Panchayat Management System Project

![image](https://github.com/user-attachments/assets/bd821b80-e13a-49b3-8e35-aced5beceac9)


---

## ✅ Step 1: Set Up the Remote Repository

1. **Check the current remote:**
   ```bash
   git remote -v
   ```
   Ensure the output shows your GitHub repository, like this:
   ```bash
   origin  git@github.com:Lubesh-Sharma/HighFive.git (fetch)
   origin  git@github.com:Lubesh-Sharma/HighFive.git (push)
   ```

2. **If the remote is incorrect, update it:**
   ```bash
   git remote remove origin
   git remote add origin git@github.com:Lubesh-Sharma/HighFive.git
   ```

---

## ✅ Step 2: Create and Switch to a New Branch

1. **Create a new branch and switch to it:**
   ```bash
   git checkout -b "Branch-Name"
   ```

---

## ✅ Step 3: Keep the Main Branch Up-to-Date

1. **Switch to the main branch:**
   ```bash
   git checkout main
   ```

2. **Fetch and merge the latest changes from the remote main branch:**
   ```bash
   git pull origin main
   ```

---

## ✅ Step 4: Rebase Your Branch with the Latest Main

1. **Switch back to your feature branch:**
   ```bash
   git checkout "Branch-Name"
   ```

2. **Rebase your branch with main:**
   ```bash
   git rebase main
   ```

   If conflicts arise, resolve them manually, then continue the rebase:
   ```bash
   git add .
   git rebase --continue
   ```

---

## ✅ Step 5: Make Changes and Commit Them

1. **Stage your changes:**
   ```bash
   git add .
   ```

2. **Commit your changes with a descriptive message:**
   ```bash
   git commit -m "Your feature or fix description"
   ```

---

## ✅ Step 6: Push Your Branch to the Remote

1. **Push your branch to the remote repository:**
   ```bash
   git push -u origin "Branch-Name"
   ```

---

## ✅ Step 7: Check Available Branches

1. **List all local branches:**
   ```bash
   git branch
   ```

2. **List all remote branches:**
   ```bash
   git branch -r
   ```

---

## 📌 **How to Ensure Your Branch is Up-to-Date**

1. **Check the current branch:**
   ```bash
   git branch
   ```
   If you're not on the correct branch, switch to it:
   ```bash
   git checkout "Branch-Name"
   ```

2. **Fetch and merge the latest changes from main:**
   ```bash
   git fetch origin
   git merge origin/main
   ```

   If there are merge conflicts, resolve them manually:
   ```bash
   git add .
   git commit -m "Resolved merge conflicts"
   ```

---

## 🔥 **How to Remove the Last Commit**

### ➤ **If You Have NOT Pushed the Commit Yet:**

1. **Undo the last commit while keeping the changes:**
   ```bash
   git reset --soft HEAD~1
   ```

2. **Check your status to confirm:**
   ```bash
   git status
   ```

   Your changes will remain in the staging area for further modification or re-commit.

### ➤ **If You Have ALREADY Pushed the Commit:**

⚠️ **Be cautious—this rewrites history and may affect others.**

1. **Undo the last commit and keep the changes:**
   ```bash
   git reset --soft HEAD~1
   ```

2. **Force push to update the remote branch:**
   ```bash
   git push origin main --force
   ```

### ➤ **If You Want to Completely Delete the Commit (and Changes):**

1. **Undo the last commit and discard all changes:**
   ```bash
   git reset --hard HEAD~1
   ```

2. **Force push the updated branch:**
   ```bash
   git push origin main --force
   ```

