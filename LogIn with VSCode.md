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

---
---

# 🎯 install a new IDE, and try to push code in another repo, in my GitHub (edge browser)

<img width="1920" height="1080" alt="Screenshot (641)" src="https://github.com/user-attachments/assets/568f51d2-76a0-4785-86a5-60160ffd168b" />

I basically want **WebStorm** to push to your GitHub account (`akashdip2001`) using a **Personal Access Token (PAT)**, without interfering with my brother’s VS Code setup (`arkadip2007` login with Brave browser).

I already did this for IntelliJ IDEA, WebStorm will work almost the same because they share the same JetBrains settings style.
We just need to make sure **WebStorm is using your GitHub account, not your brother’s**.

---

## **Step-by-Step: Set up WebStorm with Personal Access Token**

### ✅ 1 & 2. **Just click the `repo` logo at left side and click Login, and the Edge open and clock `Login`.** or you use Access Tocken  ...

<details>
  <summary style="opacity: 0.85;"><b>Login with Access Tocken</b></summary><br>
  
### **1. Generate a Personal Access Token (if you don’t already have one)**

1. Log in to [GitHub](https://github.com/) with your `akashdip2001` account.
2. Go to **Settings → Developer settings → Personal access tokens → Tokens (classic)**.
3. Click **Generate new token → Generate new token (classic)**.
4. Set:

   * **Note:** "WebStorm Access"
   * **Expiration:** Choose 90 days or "No expiration" if you want permanent.
   * **Scopes:**

     * ✅ `repo` (Full control of private repositories)
     * ✅ `workflow` (optional, for GitHub Actions)
5. Click **Generate token** and copy it somewhere safe.

---

### **2. Configure WebStorm to Use Your GitHub Account**

1. Open **WebStorm**.
2. Go to **File → Settings → Version Control → GitHub** (or on Mac: `WebStorm → Preferences`).
3. Click the **`+`** button → **Log In via Token**.
4. Paste your **Personal Access Token**.
5. Press **Log In**.

---

</details>

### **3. Make Sure the Repo Uses Your Account**

1. Open the project in WebStorm.
2. Go to **File → Settings → Version Control → Git**.
3. Check the **Path to Git executable** is correct (usually `C:\Program Files\Git\bin\git.exe`).
4. Open the terminal in WebStorm and run:

   ```bash
   git config user.name "akashdip2001"
   git config user.email "your-email@example.com"
   ```

   *(Use the same email as your GitHub account.)*
5. Check the remote URL:

   ```bash
   git remote -v
   ```
   
<img width="1828" height="486" alt="Screenshot (643)" src="https://github.com/user-attachments/assets/b842ce28-0769-4246-b4a0-6d11114898fd" />

   If it shows your brother’s username, change it:

   ```bash
   git remote set-url origin https://github.com/akashdip2001/YourRepoName.git
   ```

---

### **4. Test Push**

1. Make a small change.
2. Commit.
3. Click **Push** in WebStorm.
4. It should push without asking for credentials.

---

## ❌ Problem Not solve, Access Denide.

### change the local git account.

```bash
git config user.name "akashdip2001"
git config user.email "your-email@example.com"
```

**inside your project folder** (without the `--global` flag), it will only set your Git identity for **that specific repository**, not for all repos or for VS Code.

<img width="1920" height="1080" alt="Screenshot (645)" src="https://github.com/user-attachments/assets/66f50297-8192-41e3-91c8-a380ef438d53" />

---

## ❌⚠️ Problem not solve

I see what’s happening — you updated your `user.name` and `user.email`, but the push is **still using your brother’s GitHub login** (Arkadip2007) because your Git credentials are cached in Windows Credential Manager.

The `403` means GitHub sees that:

1. You’re trying to push to `akashdip2001/JavaScript.git`
2. But your stored credentials are for **Arkadip2007**
3. That account doesn’t have permission, so GitHub rejects it.

---

### ✅ **Fix: Force WebStorm to Ask for Your PAT**

#### 1️⃣ Remove old credentials

* Open **Windows Credential Manager**
  (Press `Win + S` → search “Credential Manager” → Open → Click **Windows Credentials**)
* Find anything that starts with:

  ```
  git:https://github.com
  ```

  or

  ```
  github.com
  ```
* Remove them all.

<p align="center">
  <img src="https://github.com/user-attachments/assets/78683364-911f-4bd9-977f-330da064d1ee" width="33%" /> 
  <img src="https://github.com/user-attachments/assets/44a85edd-504a-4225-af21-f6837b7db071" width="33%" /> 
  <img src="https://github.com/user-attachments/assets/e3a22a74-0380-4663-8be0-7c7ed1dc731e" width="33%" />
</p>

---

#### 2️⃣ Update remote URL to use HTTPS

Run this in WebStorm terminal:

```bash
git remote set-url origin https://github.com/akashdip2001/JavaScript.git
```

---

#### 3️⃣ Push & Enter PAT

Now try:

```bash
git push
```

It will ask for **Username** and **Password**:

* **Username** → `akashdip2001`
* **Password** → paste your **Personal Access Token** (from GitHub)

<p align="center">
  <img src="https://github.com/user-attachments/assets/a7aad503-ec17-40d5-b061-29756e9bf16a" width="24.5%" /> 
  <img src="https://github.com/user-attachments/assets/613d5733-6f9c-4df9-bccb-594896ecc800" width="24.5%" /> 
  <img src="https://github.com/user-attachments/assets/894fd3da-2696-4814-88cf-d42c9b4bd5a0" width="24.5%" />
  <img src="https://github.com/user-attachments/assets/6d9a6e29-ae14-4b9c-9faf-2795af6b9644" width="24.5%" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/17ecfe6a-7545-4805-a268-0b6fad1e58f1" width="47%" /> 
  <img src="https://github.com/user-attachments/assets/e07b63c9-b732-4adc-ac64-9792ee923efb" width="47%" /> 
</p>

---
---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

</br>
</br>
<div style="display: flex; align-items: center; gap: 10px;" align="center">

 ---
 
# Back to Normal

---

</div>

</br>
</br>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## for Linux

You earlier had **multiple Git accounts** configured on the same machine (with SSH keys and Git config switching, like in the doc you linked), but now you only want to use your **single account (`akashdip2001`)** on this computer.

That means you can **clean up old configs and set everything to one account**. Here’s how you can fix it step by step:

---

### 1. Reset Git global config to your account

```bash
git config --global user.name "akashdip2001"
git config --global user.email "your_email@example.com"
```

👉 Replace `your_email@example.com` with the email linked to your GitHub account.

---

### 2. Clean up SSH keys (if you had multiple before)

* Check what keys you currently have:

```bash
ls -al ~/.ssh
```

If you see multiple like `id_rsa`, `id_rsa_work`, `id_rsa_personal`, etc., and you only want one account:

* Keep the key you want to use (say `id_ed25519` or `id_rsa`)
* Remove old ones:

```bash
rm ~/.ssh/id_rsa_work ~/.ssh/id_rsa_personal
```

---

### 3. Reset SSH config

Open:

```bash
nano ~/.ssh/config
```

Clean it up so it only has one GitHub setup, e.g.:

```
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519
```

Save and exit.

---

### 4. Test your connection

```bash
ssh -T git@github.com
```

It should say something like:

```
Hi akashdip2001! You've successfully authenticated, but GitHub does not provide shell access.
```

---

### 5. Verify per-project Git config (optional)

Sometimes repos override global config. Run inside any repo:

```bash
git config --get user.name
git config --get user.email
```

If they’re different, reset them:

```bash
git config user.name "akashdip2001"
git config user.email "your_email@example.com"
```

---

✅ After this, your computer will only use **`akashdip2001` GitHub account everywhere**.

---
---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## for Windows

Opened an **Administrator CMD**, here’s a complete, copy-pasteable Windows workflow (commands + what they do) to make this machine use **only your `akashdip2001` GitHub account** with the single SSH key you already have (`id_rsa_akashdip`). Follow the steps in order.

# 1) Quick check: list your `~/.ssh` folder

```cmd
dir "%USERPROFILE%\.ssh" /A
```

<img width="100%" alt="Screenshot (815)" src="https://github.com/user-attachments/assets/eb3689ba-50ab-418c-a853-6e7bd4bb3c9f" />

The folder contains `id_rsa_akashdip` and `id_rsa_akashdip.pub`.

---

# 2) Ensure Git uses your account (global config)

(You already set these; running again is harmless.)

```cmd
git config --global user.name "akashdip2001"
git config --global user.email "akashdip.mahapatra.21@aot.edu.in"
```

---

# 3) Create / edit SSH config (so ssh uses this key for github.com)

This puts the right identity in the SSH client config so GitHub always gets your `id_rsa_akashdip` key.

```cmd
notepad "%USERPROFILE%\.ssh\config"
```

In Notepad, paste exactly (then Save → Close):

```
Host github.com
  HostName github.com
  User git
  IdentityFile C:/Users/akash/.ssh/id_rsa_akashdip
  IdentitiesOnly yes
```

(Using forward slashes for the path is fine for OpenSSH on Windows.)

<img width="100%" alt="Screenshot (816)" src="https://github.com/user-attachments/assets/a1a8e4d8-168f-4221-b916-a1d76e6f2936" />

---

# 4) Make sure the ssh-agent service will run and start it (you are admin so these work)

```cmd
sc config ssh-agent start=auto
sc start ssh-agent
```

If `sc start` says it’s already running, that’s fine.

---

# 5) Add your private key to the agent

```cmd
ssh-add "%USERPROFILE%\.ssh\id_rsa_akashdip"
```

* If the key has a passphrase you’ll be prompted for it.
* To see what keys the agent currently has: `ssh-add -l`

---

# 6) (Optional) Fix file permissions on your private key (keeps key private)

```cmd
icacls "%USERPROFILE%\.ssh\id_rsa_akashdip" /inheritance:r
icacls "%USERPROFILE%\.ssh\id_rsa_akashdip" /grant:r "%USERNAME%:R"
```

This removes inherited ACLs and grants you read access only.

---

# 7) Add the **public** key to your GitHub account

Open the public key, copy all text:

```cmd
notepad "%USERPROFILE%\.ssh\id_rsa_akashdip.pub"
```

<img width="100%" alt="Screenshot (818)" src="https://github.com/user-attachments/assets/63acf95e-4678-4d6f-90ca-44c23c35c88f" />

Then in your browser:

<img width="100%" alt="Screenshot (817)" src="https://github.com/user-attachments/assets/6e65e447-32a3-4e07-bf7b-526023d5e138" />

* Go to github.com → **Settings** (click your avatar) → **SSH and GPG keys** → **New SSH key**
* Paste the key, title it like `akashdip-laptop`, Save.

---

# 8) Test the SSH connection (verbose debug if needed)

First a normal test:

```cmd
ssh -T git@github.com
```

Expected success message:

```
Hi akashdip2001! You've successfully authenticated, but GitHub does not provide shell access.
```

<details>
  <summary style="opacity: 0.85;"><b>If it still fails ‼️</b></summary><br>
  
If it still fails, run verbose to see which key ssh is offering:

```cmd
ssh -vT git@github.com
```

Look for lines like:

* `debug1: identity file C:\\Users\\akash\\.ssh\\id_rsa_akashdip type 0`
* `Offering public key: C:\\Users\\akash\\.ssh\\id_rsa_akashdip`
* If it ends with `Hi akashdip2001!` you’re good. If it ends with `Permission denied (publickey)`, read troubleshooting below.

---

# 9) Make sure your repo remotes use SSH (not HTTPS)

Inside any repo:

```cmd
git remote -v
```

If you see `https://github.com/...` and you prefer SSH, switch to SSH:

```cmd
git remote set-url origin git@github.com:akashdip2001/REPO_NAME.git
```

(replace `REPO_NAME.git` with the repo name)

You can make Git automatically rewrite https → ssh for all repos (optional):

```cmd
git config --global url."git@github.com:".insteadOf "https://github.com/"
```

---

# Troubleshooting checklist (if `ssh -T` still fails)

1. **Did you paste the public key into GitHub?** — check SSH keys page.
2. **Is ssh-agent actually running and did you `ssh-add` your key?**

   * `ssh-add -l` should list the fingerprint.
3. **Is your `config` correct?** `notepad "%USERPROFILE%\.ssh\config"` — confirm `IdentityFile` path exactly matches your file name.
4. **Verbose debug**: `ssh -vT git@github.com` — look for which key is being offered. If it never offers your `id_rsa_akashdip`, `IdentitiesOnly yes` + correct IdentityFile helps force it.
5. **Remove old GitHub host key if host key changed**:

   ```cmd
   ssh-keygen -R github.com
   ```

   Then retry `ssh -T git@github.com` (it will add a new `known_hosts` entry).
6. **Double-check the GitHub user for the key**: the `Hi <username>!` message will show the account associated with the key.

</details>

---
