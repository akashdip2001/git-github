# Branch Protection Setup Guide

This guide explains exactly which checkboxes to enable when setting up branch protection for your GitHub repository, based on your screenshot.

## 🎯 **Recommended Settings for Personal Projects**

### ✅ **ESSENTIAL (Must Enable)**

#### 1. **Restrict pushes that create files larger than 100 MB**
- ☑️ **Enable this checkbox**
- **Why:** Prevents accidentally uploading huge files that can break your repository
- **Impact:** Low - only blocks genuinely large files

#### 2. **Block force pushes**
- ☑️ **Enable this checkbox** 
- **Why:** Prevents accidental destruction of commit history
- **Impact:** Medium - you can still force push from Settings if needed

### 🔶 **RECOMMENDED (Good to Enable)**

#### 3. **Require a pull request before merging**
- ☑️ **Enable this checkbox**
- **Why:** Forces you to review changes before they go to main branch
- **Impact:** Medium - you'll need to create PRs for changes
- **Sub-options to enable:**
  - ☑️ **Dismiss stale PR approvals when new commits are pushed**
  - ☑️ **Require review from code owners** (if you have CODEOWNERS file)

#### 4. **Require status checks to pass before merging**
- ☑️ **Enable this checkbox** (if you plan to add automated tests)
- **Why:** Ensures tests pass before merging
- **Impact:** Medium - only affects you if you add GitHub Actions/CI

#### 5. **Require branches to be up to date before merging**
- ☑️ **Enable this checkbox**
- **Why:** Prevents merge conflicts
- **Impact:** Low - just keeps things clean

### 🔴 **SKIP FOR PERSONAL PROJECTS**

#### ❌ **Require deployments to succeed**
- **Skip:** Too complex for personal projects

#### ❌ **Require signed commits**
- **Skip:** Not necessary for personal projects (requires GPG setup)

#### ❌ **Require linear history**
- **Skip:** Too restrictive for learning

#### ❌ **Require merge queue**
- **Skip:** Only needed for high-traffic repositories

---

## 🔓 **Bypass Settings (Important!)**

### **Who can bypass these rules?**

Looking at your screenshot, you should configure:

#### ✅ **Repository admin/owner** 
- ☑️ **Check "Include administrators"** if you want rules to apply to you too
- **Recommendation:** ⚠️ **UNCHECK** this for personal projects
- **Why:** You might need to make emergency fixes

#### ✅ **Apps and users with bypass permissions**
- **Leave empty** for personal projects
- **Add specific users/apps** only if you're collaborating

---

## 🎯 **Quick Setup for Beginners**

### **Minimal Protection (Recommended for You):**
```
☑️ Block force pushes
☑️ Restrict pushes that create files larger than 100 MB  
☐ Include administrators (unchecked - so you can bypass)
```

### **Medium Protection (If You Want More Safety):**
```
☑️ Block force pushes
☑️ Restrict pushes that create files larger than 100 MB
☑️ Require a pull request before merging
  └── ☑️ Dismiss stale PR approvals when new commits are pushed
☐ Include administrators (unchecked)
```

---

## 📋 **Step-by-Step Instructions**

### **Based on your screenshot:**

1. **Rule Name:** Leave as "main" (it's correct)

2. **Enforcement Status:** Keep "Disabled" for now (you can enable later)

3. **Bypass List:** Leave empty

4. **Target Branches:** Shows "main" ✅

5. **Branch Rules - Check these boxes:**
   - ☑️ **Block force pushes** (7th checkbox down)
   - ☑️ **Restrict pushes that create files larger than 100 MB** (8th checkbox down)

6. **Leave unchecked for now:**
   - ☐ Require status checks
   - ☐ Require pull request reviews (enable later when comfortable)
   - ☐ Restrict deletions
   - ☐ Require signed commits
   - ☐ Require linear history
   - ☐ Require deployments to succeed
   - ☐ Require merge queue

7. **At the bottom:**
   - ☐ **Include administrators** (UNCHECK this so you can bypass rules)

8. **Click "Create" button**

---

## 🚨 **What Happens After Enabling?**

### **With Minimal Protection:**
- ✅ You can still push directly to main
- ✅ You can still merge branches
- ❌ You cannot force push (safety feature)
- ❌ You cannot upload files >100MB

### **With Medium Protection:**
- ❌ You cannot push directly to main branch
- ✅ You must create Pull Requests for changes
- ✅ You can still bypass rules as admin (if unchecked "Include administrators")

---

## 🛠️ **How to Work with Pull Requests (If Enabled)**

If you enable "Require pull request before merging":

```bash
# 1. Create a new branch for changes
git checkout -b feature/my-new-feature

# 2. Make your changes and commit
git add .
git commit -m "Add new feature"

# 3. Push the branch
git push origin feature/my-new-feature

# 4. Go to GitHub and create Pull Request
# 5. Merge the PR through GitHub interface
# 6. Delete the feature branch and pull main
git checkout main
git pull origin main
git branch -d feature/my-new-feature
```

---

## 💡 **Pro Tips**

### **Start Small:**
1. Begin with just "Block force pushes" 
2. Get comfortable with the workflow
3. Add more protections gradually

### **Emergency Bypass:**
- If you get locked out, go to Settings → Branches
- Temporarily disable the rule
- Make your changes
- Re-enable protection

### **Testing:**
- Create a test repository first
- Try different settings
- See what works for your workflow

---

## 🔄 **Recommended Progression**

### **Week 1-2: Basic Protection**
```
☑️ Block force pushes only
```

### **Week 3-4: Add File Protection**
```
☑️ Block force pushes
☑️ Restrict file size >100MB  
```

### **Month 2: Add PR Workflow**
```
☑️ Block force pushes
☑️ Restrict file size >100MB
☑️ Require pull requests
```

### **Month 3+: Full Protection**
```
☑️ All above +
☑️ Require status checks (when you add tests)
☑️ Require up-to-date branches
```

---

## ⚠️ **Important Notes**

1. **You can change these settings anytime** - they're not permanent
2. **Start conservative** - you can always add more protection later
3. **"Include administrators"** - Keep unchecked for personal projects
4. **Test on a dummy repo first** if you're unsure

---

**Created:** September 20, 2025  
**For Repository:** ParkerHub  
**User Level:** Beginner  
**Purpose:** Safe branch protection setup