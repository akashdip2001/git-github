<img align="right" alt="python_logo" width="400" src="source/git&github.png"> 

# Git & GitHub: Essential Commands


| 🔭 [**my website**](https://akashdip2001.github.io/linktree/) | [Git docs.](https://docs.chaicode.com/git-and-github/) | [<img src="https://user-images.githubusercontent.com/81384987/209952974-0163b04e-ccae-4be5-844a-075ef85c43d2.png" height="15" width="20"/> My YouTube Channel](https://www.youtube.com/c/akashaot) |
| --- | --- | --- |

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

<img align="right" alt="python_logo" width="400" src="source/git_status.svg"> 

```bash
git --version
```
```bash
#check where oyu are?
pwd
```
```bash
#All files & folders
ls
```
```bash
#The folder tracked by git or not ?
git status
```

| [docs](https://docs.chaicode.com/terminology/) |
| --- |

---

## Configuring Git (Terminal)

```bash
git config --global user.name "Your Name"
```
```bash
git config --global user.email "your.email@example.com"
```
```bash
git config --list
```

![Git Configuration](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

# 🦖 Create an Repository Locally, Edit, and Push from GitHub

<img align="right" alt="python_logo" width="500" src="source/gitflow.svg"> 

```yaml
Main Folder
│
│── Folder 01
└── Folder 02: I want to track this folder
```
```bash
cd Folder 02
```
```bash
git status
```
```bash
git init
```
```yaml
Py Projects
Main Folder
│
│── Folder 01
└── Folder 02
     │
     └── .git: ⚠️
```
## ⚠️ Not showing .git Folder ?
#### Open Vs code -> Settings -> Exclud -> Remove Git from here.

<details>	
 <summary><b>image Guide <img src="source/img_logo.png" width="20"/></b></summary><br>
<div style='display:flex; align-items:center; gap: 10px;' align='center'>
<p align="center">
  <img src="https://github.com/user-attachments/assets/862d7cd6-ed5a-48e0-b9a2-ddecef5db0f9" alt="Image 1" width="45%" style="margin-right: 10px;"/>
  <img src="https://github.com/user-attachments/assets/d8789b6b-d46e-40ae-aea7-90ee92b7a9ba" alt="Image 2" width="45%" style="margin-right: 10px;"/>
</p>
</div>
</details>


# Or, 🦖 Clone an Existing Repository Locally, Edit, and Push from GitHub

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

```yaml
Py Projects
Main Folder
│
│── Folder 01
└── Folder 02
     │
     │── .git:
     │── file 01
     └── file 02
```
```bash
# git add filename_01.txt filename_02.txt
git add .
```
<details>	
 <summary><b>image Guide <img src="source/img_logo.png" width="20"/></b></summary>
<img src="https://github.com/user-attachments/assets/cbd1509f-39e9-4d95-a78b-910b1cc84229">
<img src="https://github.com/user-attachments/assets/d448aaf0-2d6c-4b0d-b50f-91442960867f">
</details>
     
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

[📄 Documentation](https://docs.chaicode.com/git-and-github/)


