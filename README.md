# Documentation-Cheet-sheet-details
## GitHub Copilot in VS Code cheat sheet : https://code.visualstudio.com/docs/copilot/copilot-vscode-features





# **🌍 Collaborating on the Same Project in VS Code Using Git & GitHub**
If you and your team want to work on the **same project** using **Git and GitHub**, follow these steps:

---

## **✅ 1️⃣ Set Up Git & GitHub Locally**
Before collaborating, ensure **Git is installed** on your system:

```sh
git --version
```
If Git is **not installed**, download it from **[Git Website](https://git-scm.com/downloads)**.

### **🔗 Link Git to Your GitHub Account**
Run these commands to set up your Git identity:

```sh
git config --global user.name "Your GitHub Username"
git config --global user.email "your-email@example.com"
```

---

## **✅ 2️⃣ Clone the Project from GitHub**
If the project is already on GitHub, **clone it** to your local system:

```sh
git clone https://github.com/username/repository.git
```
📌 Replace `username/repository` with the **actual GitHub repository link**.

Go inside the project folder:

```sh
cd repository
```

---

## **✅ 3️⃣ Work on the Project in VS Code**
Open the **project folder** in **VS Code**:

```sh
code .
```

Make changes to the files and **save** them.

---

## **✅ 4️⃣ Create a New Branch (Recommended for Collaboration)**
Instead of working directly on the `main` branch, **create a new branch**:

```sh
git checkout -b feature-branch
```
📌 Replace `feature-branch` with a meaningful name (e.g., `add-login-page`).

---

## **✅ 5️⃣ Add, Commit & Push Changes**
After making changes, follow these steps:

1️⃣ **Check which files changed**:  
```sh
git status
```

2️⃣ **Add changed files to Git**:  
```sh
git add .
```

3️⃣ **Commit the changes**:  
```sh
git commit -m "Added new feature"
```

4️⃣ **Push changes to GitHub**:  
```sh
git push origin feature-branch
```

---

## **✅ 6️⃣ Create a Pull Request (PR)**
1. Go to your repository on **GitHub**.  
2. Click **"Pull Requests"** → **"New Pull Request"**.  
3. Select **your branch** and compare it with `main`.  
4. Click **"Create Pull Request"** and add a description.  
5. Your team can review and merge the changes.

---

## **✅ 7️⃣ Keep Your Local Project Updated**
If someone else **makes changes** in the repository, update your local code:

```sh
git pull origin main
```
Or, if you're on a feature branch:

```sh
git pull origin feature-branch
```

---

## **✅ 8️⃣ Resolving Merge Conflicts (If Any)**
If you face merge conflicts, Git will highlight them in the files.  
1. Open the file in **VS Code**.  
2. Manually resolve the conflicting code.  
3. Add the fixed file to Git:  
   ```sh
   git add .
   ```
4. Commit the resolved changes:  
   ```sh
   git commit -m "Resolved merge conflict"
   ```
5. Push the updated code:  
   ```sh
   git push origin feature-branch
   ```

---
If both developers want to work directly on the **main** branch in GitHub, follow these steps to avoid conflicts and maintain a smooth workflow:  

---
## **✅ 2️⃣ Always Pull the Latest Code Before Working**
Before making any changes, **sync** your local main branch with the latest version from GitHub:

```sh
git pull origin main
```
This ensures that you have the most recent updates made by other team members.

---


## **✅ 5️⃣ Handling Merge Conflicts (If Any)**
If someone else has already made changes to `main`, your push might be rejected.  
In that case, **sync** your local branch before pushing:

```sh
git pull origin main --rebase
```
- If there are conflicts, Git will highlight them.  
- Open the conflicting files in **VS Code**, manually fix the conflicts, and **save** the files.  
- Then, **add the fixed files**:  
  ```sh
  git add .
  ```  
- **Commit the resolved changes**:  
  ```sh
  git commit -m "Resolved merge conflict"
  ```  
- **Push the updated code**:  
  ```sh
  git push origin main
  ```

---

## **🚀 Best Practices for Working on the Main Branch**
1️⃣ **Always pull (`git pull origin main`) before making changes.**  
2️⃣ **Communicate with your team** to avoid working on the same file at the same time.  
3️⃣ **Use clear commit messages** to track changes easily.  
4️⃣ **If many changes are expected, use feature branches** to avoid conflicts.  

---
### Workflow Summary:
- **Clone the repository:** You’ve already done this with `git clone`.
- **Pull latest changes:** Run `git pull origin main` before making your own changes to make sure you have the most up-to-date code.
- **Make changes:** Modify the code and save your changes.
- **Commit and push:** After making changes, `git add .`, `git commit`, and `git push origin main`.

---

### What if There Are Conflicts?
- If someone else has already pushed changes to `main` while you were working, Git might report a **merge conflict**.
- In this case, you will need to resolve the conflicts manually in VS Code (or another editor) before pushing your changes.

---

**No need for a pull request** unless you are working on a separate feature branch and want to merge those changes into the `main` branch!

**Done! 🎉** Now, both you and your teammate can work directly on the **main** branch without issues. 🚀


# Steps for Your Teammate to Add You as a Collaborator to a Public Repository:

1. **Go to the Repository**:
   - Your teammate needs to navigate to the **GitHub repository** they want to grant you access to.

2. **Open the Settings**:
   - On the right side of the repository page, your teammate should click on the **Settings** tab (this option is only visible to repository owners and collaborators).

3. **Navigate to the Collaborators & Teams Section**:
   - In the settings menu, on the left-hand side, your teammate should scroll down and find the **Manage Access** section.
   - They need to click on **Collaborators & teams**.

4. **Invite a Collaborator**:
   - Under the **Collaborators** section, there is an **Invite a collaborator** button. Your teammate should click it.
   
5. **Add Your GitHub Username**:
   - In the invite field, your teammate will enter your **GitHub username**.
   - Once your username appears in the search results, they can click on your profile and send you an invitation.

6. **Accept the Invitation**:
   - You will receive an email notification and a notification on GitHub asking you to accept the collaboration invitation.
   - Once you accept the invitation, you will have **write access** to the repository, meaning you can push changes directly to it.

### After Being Added as a Collaborator:
- Once you’ve accepted the invitation, you can directly **push changes** to the repository without the need to fork it.
- You can follow these Git commands to add, commit, and push your changes:
   ```sh
   git add .
   git commit -m "Your commit message"
   git push origin main  # or the appropriate branch you're working on
   ```

---

### Summary:
- Your teammate needs to add you as a collaborator in the **repository settings**.
- You’ll receive an invitation to accept, after which you’ll have **write access** to the repository and can push directly to it.




Yes! To ensure a smooth collaboration while both of you are working on the **main** branch, follow this workflow:  

---

### **✅ Steps for Both of You to Push Updates Without Conflicts**  

### **1️⃣ Pull the Latest Changes Before Making Any Updates**
Before you start making changes, **always pull the latest version** of the `main` branch to avoid conflicts:  
```sh
git pull origin main
```
This ensures your local copy is **up to date** with your teammate’s changes.  

---

### **2️⃣ Make Your Changes Locally**  
After pulling, update your file (**`eda.py`**) and save your changes.

---

### **3️⃣ Add & Commit Your Changes**  
Once you’re done, stage and commit your changes:  
```sh
git add eda.py  # Add only the modified file
git commit -m "Updated EDA script with new analysis"
```

---

### **4️⃣ Pull Again Before Pushing**
Before pushing, **pull again** to check if your teammate has pushed anything new:  
```sh
git pull origin main
```
- If no new updates: You can **push safely**.  
- If there are updates: Git will **merge** them automatically, or you may need to manually resolve conflicts.  

---

### **5️⃣ Push Your Changes**
If everything looks good, push your changes to GitHub:  
```sh
git push origin main
```
This updates the repository with your changes.

---

### **💡 What If There’s a Merge Conflict?**  
If both of you edited the **same part** of a file, Git will show a **merge conflict** after pulling.  
To fix it:
1. Open the conflicting file in VS Code.
2. Git will show conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
3. Manually **choose which changes to keep**.
4. Stage the fixed file:
   ```sh
   git add eda.py
   ```
5. Commit the resolved changes:
   ```sh
   git commit -m "Resolved merge conflict in eda.py"
   ```
6. Push again:
   ```sh
   git push origin main
   ```

---

### **🎯 Summary**
✅ **Always pull before making changes**  
✅ **Pull again before pushing**  
✅ **Resolve conflicts if necessary**  
✅ **Push your updates after merging the latest changes**  

This process ensures **no conflicts** and a smooth workflow! 🚀 Let me know if you have any doubts. 😊

