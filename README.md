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

**Done! 🎉** Now, both you and your teammate can work directly on the **main** branch without issues. 🚀
