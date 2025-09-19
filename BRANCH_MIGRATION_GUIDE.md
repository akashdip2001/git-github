# Git Branch Migration Guide: Master to Main

This document provides a comprehensive guide for migrating a Git repository from the `master` branch to the `main` branch, including all commands used, errors encountered, and their solutions.

## 📋 Overview

This guide covers the complete process of:
- Creating a new `main` branch from existing `master` branch
- Pushing the new branch to GitHub
- Handling conflicts with existing remote branches
- Deleting the old `master` branch (both locally and remotely)
- Setting up the new default branch

---

## 🚀 Step-by-Step Process

### Step 1: Check Current Repository Status

**Command:**
```powershell
git status
```

**Purpose:** Verify current branch and ensure working directory is clean.

**Expected Output:**
```
On branch master
nothing to commit, working tree clean
```

### Step 2: Create New Main Branch

**Command:**
```powershell
git checkout -b main
```

**Purpose:** Create and switch to a new `main` branch from the current `master` branch.

**Expected Output:**
```
Switched to a new branch 'main'
```

**What this does:**
- Creates a new branch called `main`
- Copies all commits from `master` to `main`
- Switches your working directory to the new `main` branch

### Step 3: Push Main Branch to GitHub (First Attempt)

**Command:**
```powershell
git push -u origin main
```

**Purpose:** Push the new `main` branch to GitHub and set it as upstream.

**⚠️ Error Encountered:**
```
To https://github.com/akashdip2001/ParkerHub.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/akashdip2001/ParkerHub.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
```

**Why this happened:** GitHub automatically created a `main` branch with initial content (README) when the repository was created, causing a conflict.

### Step 4: Investigate Remote Branches

**Command:**
```powershell
git fetch origin
```

**Purpose:** Fetch all remote branches to understand the current state.

**Output:**
```
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 896 bytes | 21.00 KiB/s, done.
From https://github.com/akashdip2001/ParkerHub
 * [new branch]      main       -> origin/main
```

**Command:**
```powershell
git branch -a
```

**Purpose:** List all branches (local and remote).

**Output:**
```
* main
  master
  remotes/origin/main
  remotes/origin/master
```

**Analysis:** Both `master` and `main` branches exist on the remote, with `main` containing different content.

### Step 5: Force Push to Override Remote Main

**Command:**
```powershell
git push --force origin main
```

**Purpose:** Override the GitHub-created `main` branch with our local content.

**⚠️ Warning:** Use `--force` carefully as it overwrites remote history.

**Expected Output:**
```
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/akashdip2001/ParkerHub.git
 + d1a6e66...51273f9 main -> main (forced update)
```

**✅ Success:** The force push successfully updated the remote `main` branch with our content.

### Step 6: Delete Remote Master Branch

**Command:**
```powershell
git push origin --delete master
```

**Purpose:** Remove the `master` branch from the GitHub repository.

**Expected Output:**
```
remote: 
remote: GitHub found 25 vulnerabilities on akashdip2001/ParkerHub's default branch (2 critical, 10 high, 13 moderate). 
To find out more, visit:                                                                                               
remote:      https://github.com/akashdip2001/ParkerHub/security/dependabot
remote:
To https://github.com/akashdip2001/ParkerHub.git
 - [deleted]         master
```

**Note:** The security warning is informational and doesn't affect the branch deletion.

### Step 7: Delete Local Master Branch

**Command:**
```powershell
git branch -d master
```

**Purpose:** Remove the local `master` branch since we're now using `main`.

**Expected Output:**
```
Deleted branch master (was 51273f9).
```

### Step 8: Verify Final State

**Command:**
```powershell
git branch -a
```

**Purpose:** Confirm that only the `main` branch exists.

**Expected Output:**
```
* main
  remotes/origin/main
```

**✅ Success:** Only the `main` branch exists both locally and remotely.

---

## 🛠️ Complete Command Sequence

Here's the complete sequence of commands for future reference:

```powershell
# 1. Check current status
git status

# 2. Create and switch to main branch
git checkout -b main

# 3. Fetch remote information
git fetch origin

# 4. Check all branches
git branch -a

# 5. Force push main branch (if conflicts exist)
git push --force origin main

# 6. Delete remote master branch
git push origin --delete master

# 7. Delete local master branch
git branch -d master

# 8. Verify final state
git branch -a
```

---

## ⚠️ Important Notes and Best Practices

### When to Use Force Push
- **Use `--force` only when:** You need to override a remote branch that has conflicting content
- **Never use `--force` when:** Working with shared repositories where others might have pulled the branch
- **Alternative:** Use `--force-with-lease` for safer force pushing

### Error Prevention
1. **Always fetch first:** Run `git fetch origin` before pushing to understand remote state
2. **Check branch status:** Use `git branch -a` to see all branches
3. **Coordinate with team:** Ensure no one else is working on the branches you're deleting

### GitHub Web Interface Tasks
Some tasks require GitHub web interface:
1. **Changing default branch:** Repository Settings → General → Default branch
2. **Branch protection rules:** May need to be updated for the new `main` branch

---

## 🔧 Alternative Approaches

### Method 1: Rename Branch (if no conflicts)
```powershell
# Rename local branch
git branch -m master main

# Push new branch and set upstream
git push -u origin main

# Delete remote master
git push origin --delete master
```

### Method 2: Using GitHub CLI (if installed)
```powershell
# Create main branch
git checkout -b main
git push -u origin main

# Change default branch via CLI
gh repo edit --default-branch main

# Delete master branch
git push origin --delete master
git branch -d master
```

---

## 🐛 Common Errors and Solutions

### Error 1: "Updates were rejected"
**Cause:** Remote branch has different content
**Solution:** Use `git fetch origin` to understand the conflict, then either:
- Merge the changes: `git pull origin main`
- Force push: `git push --force origin main`

### Error 2: "Cannot delete the currently checked out branch"
**Cause:** Trying to delete the branch you're currently on
**Solution:** Switch to another branch first: `git checkout main`

### Error 3: "Remote branch doesn't exist"
**Cause:** Trying to delete a branch that's already been deleted
**Solution:** Check existing branches: `git branch -r`

### Error 4: Permission denied
**Cause:** Insufficient permissions to delete branches
**Solution:** Ensure you have admin/maintainer access to the repository

---

## 📊 Verification Checklist

After completing the migration, verify:

- [ ] Local repository is on `main` branch
- [ ] Remote repository shows `main` as default branch
- [ ] No `master` branch exists locally (`git branch`)
- [ ] No `master` branch exists remotely (`git branch -r`)
- [ ] New commits can be pushed to `main` branch
- [ ] Repository settings show `main` as default branch

---

## 🔗 Additional Resources

- [GitHub: Renaming the default branch](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-branches-in-your-repository/changing-the-default-branch)
- [Git Documentation: git-branch](https://git-scm.com/docs/git-branch)
- [Git Documentation: git-push](https://git-scm.com/docs/git-push)

---

## 📝 Command Quick Reference

| Task | Command |
|------|---------|
| Create branch | `git checkout -b <branch-name>` |
| Push new branch | `git push -u origin <branch-name>` |
| Force push | `git push --force origin <branch-name>` |
| Delete remote branch | `git push origin --delete <branch-name>` |
| Delete local branch | `git branch -d <branch-name>` |
| List all branches | `git branch -a` |
| Check current branch | `git branch` or `git status` |

---

**Created:** September 19, 2025  
**Migration:** master → main  