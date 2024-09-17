# **Git Quick Guide**

## **1. Basic Git Setup**

### Install Git
- **Linux**: `sudo apt install git`
- **Mac**: `brew install git`
- **Windows**: [Download Git](https://git-scm.com/downloads)

### Configure Git
```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```
To verify configuration:
```bash
git config --list
```

## **2. Starting a New Project**

### Initialize a New Repository
```bash
git init
```

### Clone an Existing Repository
```bash
git clone https://github.com/user/repository.git
```

## **3. Basic Commands**

### Check Repository Status
```bash
git status
```

### Add Files to Staging
```bash
git add <file>   # Add specific file
git add .        # Add all files
```

### Commit Changes
```bash
git commit -m "Your commit message"
```

### View Commit History
```bash
git log
```

## **4. Branching and Merging**

### Create a New Branch
```bash
git branch <branch-name>
```

### Switch to a Branch
```bash
git checkout <branch-name>
```

### Create and Switch to a New Branch
```bash
git checkout -b <branch-name>
```

### Merge Branches
Switch to the branch you want to merge into, typically `main`:
```bash
git checkout main
git merge <branch-name>
```

## **5. Pushing and Pulling**

### Push to Remote Repository
```bash
git push origin <branch-name>
```

### Pull Latest Changes from Remote
```bash
git pull
```

## **6. Undoing Changes**

### Unstage Files
```bash
git reset <file>
```

### Discard Unstaged Changes
```bash
git checkout -- <file>
```

### Reset to a Previous Commit
```bash
git reset --hard <commit-hash>
```

## **7. Tagging**

### Create a Tag
```bash
git tag <tag-name>
```

### Push Tags to Remote
```bash
git push origin --tags
```

## **8. Working with Remotes**

### Add a Remote
```bash
git remote add origin <remote-url>
```

### Show Remote URLs
```bash
git remote -v
```

### Remove a Remote
```bash
git remote rm <remote-name>
```
