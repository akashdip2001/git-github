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
<h5> You can install Git Bash using Chocolatey, a package manager for Windows. If you haven't installed Chocolatey yet, you can do so by running the following command in PowerShell with administrative privileges: </h5>

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

<h5>Push Changes to a Remote Repository:Once you've committed your changes locally, you can use the git push command to push those changes to a remote repository. The syntax for git push is:</h5>

```php
git push <remote_name> <branch_name>
```
<h5>For example, if you want to push your changes to the main branch of the remote repository named origin, you would use:</h5>

```css
git push origin main
```
<h5>Replace origin with the name of your remote repository, and main with the name of the branch you're pushing to.If it's your first time pushing to the remote repository, you may need to specify the -u flag to set up tracking. This tells Git to remember the remote branch so that you can use git push without specifying the remote and branch in the future:</h5>

```css
git push -u origin main
```
<h5>After the initial setup, you can simply use git push to push changes to the remote repository:</h5>

```perl
git push
```     

---
# init command

<h4><code>init</code> - used tu creat a new repo <h4>

```
..
mkdir <New File Name>
cd <The new file name>
git init
```
<h4><code>..</code> Back to main Folder</h4>
<h4><code>mkdir..</code> Creat a new Folder & enter with <code>cd</code></h4>
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
---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

<h1>🦖 Creat a repo on Github (Without .Readme) & All file in Local <br>=> Upload all files <br>=> Github </h1>
<h5><code>Without .Readme</code> Because oterWise clone and downlod in Local => Then <code>git init</code> all Local folders => push </h5>

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

<img src="source/git-branches-merge.png">

<h1> 🦖 Branch Commands</h1>

<h5>To check the branch</h5>
<h4><code>git branch</code></h4> <br>
<h5>ReName</h5>
<h4><code>git branch -M main</code></h4> <br>
<h5>navigate => one Branch to another</h5>
<h4><code>git checkout <-branch name-></code></h4> <br>
<h5>To creat new branch</h5
<h4><code>git checkout -b <- new branch name -></code></h4> ><br>
<h5>To Delete branch</h5>
<h4><code>git branch -d <- branch name -></code></h4> <br>


Then

```
git status

git add .
git commint -m "..."
git status

git push otigin <-btanch Name->
```

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

<h1> 🦖 Merging Code</h1>

<h3>Way 1</h3>

```
git diff <-branch name- Example: main>   ----to compare commits, branches, files & more
git merge <-branch name- Example: main>
```
<h3>Way 2</h3>

<h4>Creat a PR <code>Pull Request</code></h4>

```
git pull origin main    ---- Downlod and match all from Github to Local 
```
