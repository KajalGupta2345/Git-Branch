# Git Branch

## Introduction

Git Branch ek independent line of development hoti hai. Branches ki help se developers alag-alag features, bug fixes, ya experiments par kaam kar sakte hain bina main code ko affect kiye.

Default branch ka naam aksar:

```bash
main
```

ya

```bash
master
```

hota hai.

---

# Why Use Branches?

Maan lo aap ek project par kaam kar rahe hain.

Project ki current stable version:

```text
main
```

Ab aapko Login Feature banana hai.

Agar directly `main` branch me kaam karenge aur bug aa gaya to stable code affect ho sakta hai.

Isliye ek nayi branch create karte hain:

```text
login-feature
```

Aur us branch par kaam karte hain.

---

# What is HEAD?

Git me `HEAD` current active branch ya current commit ko represent karta hai.

Example:

```text
main (HEAD)
```

Matlab aap abhi `main` branch par kaam kar rahe hain.

---

# View Current Branch

```bash
git branch
```

Example Output:

```text
* main
```

`*` current active branch ko show karta hai.

---

# Create a New Branch

Syntax:

```bash
git branch <branch-name>
```

Example:

```bash
git branch login-feature
```

Ab ek nayi branch create ho gayi.

---

# List All Branches

```bash
git branch
```

Output:

```text
* main
  login-feature
```

---

# Switch Branch

Syntax:

```bash
git switch <branch-name>
```

Example:

```bash
git switch login-feature
```

Output:

```text
Switched to branch 'login-feature'
```

Ab aap `login-feature` branch par hain.

---

# Create and Switch in One Command

```bash
git switch -c login-feature
```

Ye command:

1. Branch create karti hai.
2. Us branch par switch bhi kar deti hai.

---

# Old Method (Checkout)

Purana tarika:

```bash
git checkout -b login-feature
```

Ye bhi branch create aur switch karta hai.

---

# Create Multiple Branches

```bash
git branch login
git branch signup
git branch dashboard
```

Check:

```bash
git branch
```

Output:

```text
* main
  login
  signup
  dashboard
```

---

# Merge a Branch

Maan lo:

```text
main
```

aur

```text
login-feature
```

branch hai.

Login feature complete ho gaya.

### Step 1

Main branch par jao:

```bash
git switch main
```

### Step 2

Merge karo:

```bash
git merge login-feature
```

Ab login-feature ke changes main branch me aa jayenge.

---

# Delete a Branch

Merged branch delete karne ke liye:

```bash
git branch -d login-feature
```

Force delete:

```bash
git branch -D login-feature
```

---

# Rename a Branch

Current branch rename:

```bash
git branch -m new-name
```

Example:

```bash
git branch -m login-page
```

---

# View All Branches (Including Remote)

```bash
git branch -a
```

Example:

```text
* main
  login-feature
  remotes/origin/main
  remotes/origin/login-feature
```

---

# Push Branch to GitHub

```bash
git push origin login-feature
```

Example:

```bash
git push origin login-feature
```

Ab GitHub par bhi branch create ho jayegi.

---

# Track Remote Branch

```bash
git push -u origin login-feature
```

`-u` future pushes ke liye upstream set karta hai.

Baad me sirf:

```bash
git push
```

likhna padega.

---

# Branch Workflow Example

### Create Branch

```bash
git switch -c login-feature
```

### Work on Code

```bash
git add .
git commit -m "Add login page"
```

### Push Branch

```bash
git push -u origin login-feature
```

### Switch Back to Main

```bash
git switch main
```

### Merge Branch

```bash
git merge login-feature
```

### Delete Branch

```bash
git branch -d login-feature
```

---

# Git Branch Commands Summary

```bash
# Show branches
git branch

# Create branch
git branch feature-name

# Switch branch
git switch feature-name

# Create and switch
git switch -c feature-name

# Merge branch
git merge feature-name

# Delete branch
git branch -d feature-name

# Force delete branch
git branch -D feature-name

# Rename branch
git branch -m new-name

# Show all branches
git branch -a

# Push branch
git push origin feature-name

# Push and set upstream
git push -u origin feature-name
```

---

# Summary

Git Branches developers ko independent environment provide karti hain jahan wo features develop, bugs fix aur experiments kar sakte hain bina main codebase ko affect kiye. Branching Git ki sabse powerful features me se ek hai aur collaborative development ka foundation hai.
