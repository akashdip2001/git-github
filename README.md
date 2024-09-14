# Git & GitHub: Essential Commands

![Git & GitHub](source/git-github.png){: style="float: right; width: 400px; alt: Mechanical Engineering"}

- 🔭 I’m currently working on [**my website**](https://akashdip2001.github.io/linktree/)

---

<a href="https://www.youtube.com/c/akashaot" target="_blank">
  <img src="https://user-images.githubusercontent.com/81384987/209952974-0163b04e-ccae-4be5-844a-075ef85c43d2.png" alt="akash aot" height="30" width="40" />
  &nbsp;My YouTube Channel
</a>

---

## Install Git & VS Code

### Just copy & paste the code into your PowerShell - Done ✔️

You can install Git Bash using Chocolatey, a package manager for Windows. If you haven't installed Chocolatey yet, run the following command in PowerShell with administrative privileges:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; `
[System.Net.ServicePointManager]::SecurityProtocol = `
[System.Net.ServicePointManager]::SecurityProtocol -bor 3072; `
iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

Then, install Git and VS Code:

```powershell
choco install git.install
choco install vscode
```

---

## Check Git Installation

```bash
git --version
```

---

## Configuring Git (Terminal)

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --list
```

![Git Configuration](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

# 🦖 Clone an Existing Repository Locally, Edit, and Push

---

## Clone and Check Status

```bash
git clone https://github.com/username/repository.git
```

```bash
git status
```

### Status Indicators

- <span style="color: red;">**Untracked**</span>: New files that Git doesn't track
- <span style="color: red;">**Modified**</span>: Changed files
- <span style="color: red;">**Staged**</span>: Files ready to be committed
- <span style="color: red;">**Unmodified**</span>: Unchanged files

---

## Add and Commit (Local)

```bash
git add filename.txt
git add .
```

*Use `git add .` to add all changes.*

```bash
git commit -m "Add new feature"
```

---

## Push (Upload to Remote Repository on GitHub)

### Push Changes to a Remote Repository

Once you've committed your changes locally, use the `git push` command to push those changes to a remote repository.

**Syntax:**

```bash
git push <remote_name> <branch_name>
```

**Example:**

```bash
git push origin main
```

*Replace `origin` with the name of your remote repository, and `main` with the name of the branch you're pushing to.*

If it's your first time pushing to the remote repository, you may need to set up tracking:

```bash
git push -u origin main
```

*After the initial setup, simply use `git push` for future pushes.*

```bash
git push
```

---

## Initialize a New Repository

**`init`** - Used to create a new repository

```bash
mkdir <NewFolderName>
cd <NewFolderName>
git init
```

*Use `cd ..` to navigate back to the main folder.*

*`mkdir` creates a new folder and `cd` enters it. Then, create or edit files within the folder.*

```bash
git status
git add .
git commit -m "Initial commit"
git status
```

```bash
git push origin main
```

![Git Initialization](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

# 🦖 Creating a Repository on GitHub (Without README) & Uploading Local Files

**Without a README**: This allows you to clone the repository locally, initialize Git, and push all local files.

<img src='source/new repo.png'>

```bash
git remote add origin https://github.com/username/repository.git
git remote -v
```

*Use `git remote -v` to verify the remote connection.*

## Check the Branch

```bash
git branch
```

*If you're on the `master` branch, rename it to `main`.*

### Rename the Branch to `main`

```bash
git branch -M main
git push -u origin main
```

*The `-u` flag sets up tracking for future pushes, allowing you to use `git push` without specifying the remote and branch.*

## Push Any Changes Locally

```bash
git status
git add .
git commit -m "Add new file or update"
git push
```

![Git Push](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

![Git Branches Merge](source/git-branches-merge.png)

# 🦖 Branch Commands

### Check the Branch

```bash
git branch
```

### Rename a Branch

```bash
git branch -M main
```

### Navigate Between Branches

```bash
git checkout <branch-name>
```

### Create a New Branch

```bash
git checkout -b <new-branch-name>
```

### Delete a Branch

```bash
git branch -d <branch-name>
```

### After Making Changes

```bash
git status
git add .
git commit -m "Your commit message"
git push origin <branch-name>
```

![Branch Operations](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

# 🦖 Merging Code

## Method 1: Using Git Commands

```bash
git diff <branch-name>   # Compare commits, branches, files & more
git merge <branch-name>
```

## Method 2: Creating a Pull Request (PR)

```bash
git pull origin main    # Download and synchronize with GitHub
```

![Merge Operations](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

---

| [📄 Documentation](https://docs.chaicode.com/git-and-github/) |
| --- |
