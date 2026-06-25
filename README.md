# Git Learning

These are my notes while learning Git. This repository is mainly for practice and as a quick reference whenever I forget a command.

The notes cover the basics of Git before learning branching and merging.

---

# Navigate Around

### List files and folders

```bash
ls
```

### Change directory

```bash
cd <folder>
```

Example:

```bash
cd ~/Desktop/git-tutorial
```

---

# Create a Git Repository

### Initialize Git

Start tracking the current folder with Git.

```bash
git init
```

---

# Check Repository Status

### View current status

See which files have changed since the last commit.

```bash
git status
```

---

# Stage Changes

### Stage one file

```bash
git add <file_name>
```

### Stage everything

```bash
git add .
```

---

# Save Changes

### Create a commit

Save a new version of your project.

```bash
git commit -m "message"
```

### Edit the previous commit

Replace the most recent commit.

```bash
git commit --amend
```

---

# View History

### Show commit history

```bash
git log
```

### Show all commits

```bash
git log --all
```

### Show history as a graph

```bash
git log --all --graph
```

---

# Undo Changes

### Discard changes to one file

```bash
git checkout -- <file_name>
```

This throws away all uncommitted changes for that file.

### Move to an older commit

```bash
git checkout <commit_hash>
```

This puts Git into a detached HEAD state.

### Reset the repository

```bash
git reset --hard <commit_hash>
```

Moves both `HEAD` and the current branch back to an older commit.

---

# Switch Branches

### Return to the main branch

```bash
git switch main
```

---

# Git Shortcuts (Aliases)

Create your own shortcuts for commonly used commands.

### Status

```bash
git config --global alias.s "status"
```

Use:

```bash
git s
```

### Commit

```bash
git config --global alias.cm "commit -m"
```

Use:

```bash
git cm "message"
```

### Checkout

```bash
git config --global alias.co "checkout"
```

Use:

```bash
git co
```

---

# Delete Git History

Remove Git from the current project.

```bash
rm -rf .git
```

This deletes the entire Git repository, including every commit.

---

# Remote Repositories

### Add a remote repository

```bash
git remote add <name> <repository_url>
```

Example:

```bash
git remote add origin https://github.com/username/repository.git
```

### View remotes

```bash
git remote
```

### View remotes with URLs

```bash
git remote -v
```

---

# GitHub

### Save your GitHub username

```bash
git config --global credential.username "uncertain6"
```

---

# Push to GitHub

### Push to a remote branch

```bash
git push <remote_name> <branch_name>
```

Example:

```bash
git push origin main
```

### Remember the upstream branch

```bash
git push --set-upstream origin main
```

After that, you can simply use:

```bash
git push
```

### Force push

```bash
git push -f
```

> Be careful. Force pushing can overwrite commit history.

---

# Clone a Repository

Download an existing GitHub repository.

```bash
git clone <repository_url> <folder_name>
```

Example:

```bash
git clone https://github.com/username/project.git git-learning
```

---

# Fetch & Pull

### Fetch

Download information about changes from GitHub without changing your files.

```bash
git fetch
```

### Pull

Download changes and merge them into your current branch.

```bash
git pull <remote_name> <branch_name>
```

Example:

```bash
git pull origin main
```

### Remember the upstream

```bash
git pull --set-upstream origin main
```

After that, you can simply run:

```bash
git pull
```

---
