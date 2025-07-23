# Git multi-account setup

If you facing a **common Git multi-account configuration problem** on a **single laptop**, where:

* **Primary GitHub Account** (used in IntelliJ IDEA, logged in via Microsoft Edge)
* **Secondary GitHub Account** (used in VS Code, logged in via Brave)
* **Global Git config** supports only one user at a time (per default setup)

To resolve this and use **two separate GitHub accounts with different IDEs on one machine**, you need to:

---

## ✅ Solution (Fix in 3 Steps)
### 🔧 Step 1: Manually Create the .ssh Folder

> In PowerShell, run:

```bash
mkdir ~/.ssh
```

> This creates the hidden .ssh folder inside your user directory (C:\Users\akash).

---

Great update — thanks!

From the latest messages, we can clearly see:

* The folder `.ssh` **already exists** ✅
* But your command `ssh-keygen -f ~/.ssh/...` **still failed**, saying:

  ```
  Saving key "~/.ssh/id_rsa_akashdip" failed: No such file or directory
  ```

---

## ✅ Generate `SSH Keys` for Both Accounts

On Windows, PowerShell doesn't always expand `~` correctly in all commands.

### 🔄 Try this instead (use full path):

#### 🔷 For Primary (akashdip2001):

```powershell
ssh-keygen -t rsa -C "akashdipXXXXXXX@gmail.com" -f "C:\Users\akash\.ssh\id_rsa_akashdip"
```

#### 🔶 For Secondary (Arkadip2007):

```powershell
ssh-keygen -t rsa -C "arkadipXXXXXXX@gmail.com" -f "C:\Users\akash\.ssh\id_rsa_arkadip"
```

📌 Now it should successfully save the keys.

---

### ✅ Then copy public key with:

```powershell
type C:\Users\akash\.ssh\id_rsa_akashdip.pub
```

> Copy the whole line it prints (starts with `ssh-rsa ...`) and paste it into **GitHub → SSH Keys**.

## Steps in GitHub

- Copy the output.
- Go to GitHub → Logged in as akashdip2001
- Go to Settings → SSH and GPG keys → New SSH key
- Title: Laptop SSH
- Paste the key → Save.

### ✅ Do same with another account.

---

## Go to 

```
C:\Users\akash\.ssh
```
- And create the `config` file with `No` extention.
-  And pest it.

```go
# Primary GitHub account
Host github-akashdip
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_akashdip

# Secondary GitHub account
Host github-arkadip
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_arkadip
```
  
<img width="1920" height="1080" alt="Screenshot (113)" src="https://github.com/user-attachments/assets/3c7c08f1-1d89-46f6-a7d5-4ca6277f18d9" />

---

# 🔄 Last Step: Change Remote URL in Each Project

## ✅ In IntelliJ (Primary project)

Go to your project folder and run:

```bash
git remote set-url origin git@github-akashdip:userName/your-repo-name.git
git config user.name "useName"
git config user.email "akashdipXXXXXX@google.in"
```

## ✅ In VS Code (Secondary project)

Go to your project folder and run:

```bash
git remote set-url origin git@github-arkadip:UserName/your-repo-name.git
git config user.name "userName"
git config user.email "arkadipXXXXX@gmail.com"
```

📌 Replace `your-repo-name.git` with the actual repo name.

