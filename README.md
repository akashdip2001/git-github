# git-github
All important commands useng in git-github

<img align="right" alt="Mechanical Engineering" width="400" src="source/git-github.png"> 

# kali-all-commands
[![YouTube](https://yt3.ggpht.com/7tPHyFi7-QyTnhpc484ZzTuRp0fZSY-CUuykvzuKdKYIwt0fmw98SWMqwRy_7pZ6LQzEYJlvXA=s88-c-k-c0x00ffffff-no-rj-mo)](https://www.youtube.com/channel/UCxvmp634YDc41xCWOdvWqoQ)
<br>
- 🔭 I’m currently working on [**my web-site**](https://akashdip2001.github.io/linktree/)

<br>
<br>
<a href="https://www.youtube.com/c/akash aot" target="blank"><img align="center" src="https://user-images.githubusercontent.com/81384987/209952974-0163b04e-ccae-4be5-844a-075ef85c43d2.png" alt="akash aot" height="30" width="40" />My YouTube Channel</a>
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
