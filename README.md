# git-github
All important commands useng in git-github

<img align="right" alt="Mechanical Engineering" width="400" src="source/git-github.png"> 

<br>

- 🔭 I’m currently working on [**my web-site**](https://akashdip2001.github.io/linktree/)

<br>
<br>
<a href="https://www.youtube.com/c/akash aot" target="blank"><img align="center" src="https://user-images.githubusercontent.com/81384987/209952974-0163b04e-ccae-4be5-844a-075ef85c43d2.png" alt="akash aot" height="30" width="40" />&nbsp;My YouTube Channel</a>
<br>
<br>

---
---
# install git & vsCode
<h3> jast copy & past the code into your PowerShell - Done ✔️  </h3>
<h4> You can install Git Bash using Chocolatey, a package manager for Windows. If you haven't installed Chocolatey yet, you can do so by running the following command in PowerShell with administrative privileges: </h4>

```less
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
```
choco install git.install
choco install vscode
```

---
# check Git install
```
git --version
```
---
# Configuring git (Terminal)
```arduino
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --list
```
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

<h1>🦖 Clone a Existing file in Local => Edit => Push</h1>
---

# clone and status
```bash
git clone https://github.com/username/repository.git
```
```lua
git status
```
<h4>
<span style='color: red;'>untracked</span> <br>
new files that git doesn't track<br>
<br>
<span style='color: red;'>modified</span> <br>
changed<br>
<br>
<span style='color: red;'>staged</span> <br>
file is ready to be committed<br>
<br>
<span style='color: red;'>unmodified</span> <br>
unchanged</h4>

---
# add and commit (in Local)
```csharp
git add filename.txt
git add .
```
<h4><code>git add .</code> for add all changes</h4>

```sql
git commit -m "Add new feature"
```

---
# Push (uplode Remote <code>in Github</code>)

<h4>Push Changes to a Remote Repository:Once you've committed your changes locally, you can use the git push command to push those changes to a remote repository. The syntax for git push is:</h4>

```php
git push <remote_name> <branch_name>
```
<h4>For example, if you want to push your changes to the main branch of the remote repository named origin, you would use:</h4>

```css
git push origin main
```
<h4>Replace origin with the name of your remote repository, and main with the name of the branch you're pushing to.If it's your first time pushing to the remote repository, you may need to specify the -u flag to set up tracking. This tells Git to remember the remote branch so that you can use git push without specifying the remote and branch in the future:</h4>

```css
git push -u origin main
```
<h4>After the initial setup, you can simply use git push to push changes to the remote repository:</h4>

```perl
git push
```     

---
# init command
<h4><code>init</code> - used tu creat a new repo <h4>

```csharp
..
mkdir <New File Name>
cd <The new file name>
git init
```
<code>..</code> Back to main Folder
<code>mkdir..</code> Creat a new Folder & enter with <code>cd</code>
<h4>Then creat or edit anything in the folder</h4>

```
git status

git add .
git commit -m "Initial commit"
git status
```
```css
git push origin main
```
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

<h1>Creat a repo on Github (Without .Readme) & All file in Local => Upload all files => Github </h1>
<h4><code>Without .Readme</code> Because oterWise clone and downlod in Local => Then <code>git init</code> all Local folders => push </h4>

<img src='source/new repo.png'>

```
git remote add origin https://github.com/username/repository.git
git remote -v
```
<h4><code>git remote -v</code> to Verify the Remote Connection</h4>

# Check the Branch

```
git branch
```
<h4>if U are in <code>*master</code> branch => main</h4>
<h3>Rename the Branch => main</h3>

```
git branch -M main

git push -u origin main
```
<h3><code>-u</code> mean Next every push in the Same Branch => So Next time only <code>git push</code></h3>

# Next any change in Local

```
git status
git add .
git commit -m "Add new file or anything"
git push
```

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

# Extra

It seems like there's a typo in the command. The correct command is `git branch`, which is used to manage branches in a Git repository.

Here's how you can use the `git branch` command:

1. **List Branches:**

   To list all branches in your repository, you can simply run:
   ```
   git branch
   ```
   This command will display a list of all branches in your repository, with an asterisk (`*`) next to the branch you're currently on.

2. **Create a New Branch:**

   To create a new branch, you use the `git branch` command followed by the name of the new branch. For example:
   ```
   git branch new-feature
   ```
   This command creates a new branch named `new-feature` based on the current branch. However, it doesn't switch to the new branch. To switch to the new branch, you would use `git checkout`.

3. **Switch Branches:**

   To switch to a different branch, you use the `git checkout` command followed by the name of the branch you want to switch to. For example:
   ```
   git checkout new-feature
   ```
   This command switches to the `new-feature` branch.

4. **Create and Switch to a New Branch:**

   You can combine branch creation and switching into a single command using the `-b` flag with `git checkout`. For example:
   ```
   git checkout -b new-feature
   ```
   This command creates a new branch named `new-feature` and switches to it in one step.

5. **Delete a Branch:**

   To delete a branch, you use the `-d` flag with `git branch` followed by the name of the branch you want to delete. For example:
   ```
   git branch -d new-feature
   ```
   This command deletes the `new-feature` branch.

These are some common uses of the `git branch` command for managing branches in your Git repository. Branching is a powerful feature in Git that allows you to work on different features or experiments simultaneously without affecting the main codebase.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">
