# 🚀 Git & GitHub: Beginner's Handbook

> A practical introduction to version control, Git fundamentals, and collaborating through GitHub.

---

## 📖 1. Introduction to Version Control

Version Control is a system that records modifications made to files over time. It allows developers to track project history, restore previous versions, manage changes, and work collaboratively.

### Git and GitHub: What's the Difference?

| Git | GitHub |
|---|---|
| A distributed version control system. | An online platform for hosting Git repositories. |
| Runs on your local machine. | Provides cloud-based repository management. |
| Records and manages project history. | Supports collaboration and code reviews. |
| Works offline for most operations. | Requires an internet connection for online collaboration. |

---

## 🏗️ 2. Understanding Git's Architecture

Git organizes project changes into three important areas:

| Component | Function |
|---|---|
| **Working Directory** | Contains the files you are currently editing. |
| **Staging Area** | Holds selected changes that are ready to be committed. |
| **Local Repository** | Stores committed versions of your project. |

### How Git Works

```text
   Working Directory
          |
          | git add
          ▼
     Staging Area
          |
          | git commit
          ▼
    Local Repository
          |
          | git push
          ▼
   Remote Repository
       (GitHub)
```

---

## 🛠️ 3. Commonly Used Git Commands

The following commands cover the basic operations needed to manage a Git project.

| Command | Description |
|---|---|
| `git init` | Creates a new Git repository. |
| `git status` | Checks modified, staged, and untracked files. |
| `git add <file>` | Moves file changes into the staging area. |
| `git add .` | Stages all changes in the current directory. |
| `git commit -m "message"` | Records staged changes in the repository. |
| `git log --oneline` | Displays a simplified commit history. |
| `git diff` | Displays unstaged changes. |
| `git diff --staged` | Displays staged changes. |

### Basic Development Cycle

```bash
# Initialize repository
git init

# Check file status
git status

# Stage project files
git add .

# Create a commit
git commit -m "Initial project setup"

# View commit history
git log --oneline
```

---

## 🔄 4. Managing and Reversing Changes

Git provides several commands to correct mistakes and restore earlier project states.

| Command | Description |
|---|---|
| `git restore <file>` | Discards unstaged changes in a file. |
| `git restore --staged <file>` | Removes a file from staging while preserving its modifications. |
| `git revert <commit-id>` | Creates a new commit that reverses an earlier commit. |
| `git reset --soft HEAD~1` | Removes the latest commit while keeping changes staged. |
| `git reset --hard HEAD~1` | Removes the latest commit and discards associated changes. |

**Important:** Be careful with `git reset --hard`, as it can permanently discard uncommitted work.

**Key distinction:**
- `restore` is mainly used to modify the working directory or staging area.
- `revert` safely reverses an existing commit through a new commit.
- `reset` moves the current branch reference to an earlier commit.

---

## ☁️ 5. Connecting Git with GitHub

A remote repository is a version of your project hosted on an external server, such as GitHub.

### Important Remote Commands

| Command | Description |
|---|---|
| `git remote -v` | Lists configured remote repositories. |
| `git remote add origin <url>` | Adds a remote repository named `origin`. |
| `git push -u origin main` | Uploads commits and establishes upstream tracking. |
| `git clone <url>` | Creates a local copy of an existing repository. |
| `git fetch` | Downloads remote changes without integrating them. |
| `git pull` | Fetches and integrates remote changes. |

### Publishing a Local Project to GitHub

```bash
# Connect to GitHub
git remote add origin <repository-url>

# Upload the main branch
git push -u origin main

# Get updates from GitHub
git pull
```

---

## 🌳 6. Branch Management

Branches allow developers to work on different features or fixes independently without directly modifying the main development branch.

### Essential Branch Commands

| Command | Description |
|---|---|
| `git branch` | Lists local branches. |
| `git branch <name>` | Creates a new branch. |
| `git switch <branch>` | Changes the active branch. |
| `git switch -c <name>` | Creates and switches to a new branch. |
| `git merge <branch>` | Integrates another branch into the current branch. |
| `git branch -d <name>` | Deletes a merged local branch. |

### Example: Developing a New Feature

```bash
# Create a feature branch
git switch -c feature-login

# Make changes to the project

# Stage and commit changes
git add .
git commit -m "Implement login functionality"

# Return to the main branch
git switch main

# Merge the feature branch
git merge feature-login
```

### Understanding Merge Conflicts

A merge conflict occurs when Git cannot automatically combine changes, often because different branches modify the same portion of a file.

**Steps to resolve a conflict:**

1. Identify the files containing conflicts.
2. Open the affected files.
3. Examine the conflicting changes.
4. Choose or combine the appropriate code.
5. Remove Git's conflict markers.
6. Stage the resolved files.
7. Complete the merge commit if necessary.

### Pull Requests (PRs)

A Pull Request is a GitHub feature that allows developers to propose changes from one branch to another.

**Why are Pull Requests useful?**

- Enable collaborative code reviews.
- Allow discussions about proposed modifications.
- Help detect bugs before merging.
- Maintain code quality.
- Make team collaboration easier.

---

## 📝 7. Essential Concepts: Quick Reference

| Term | Meaning |
|---|---|
| Version Control | Tracks changes made to files. |
| Git | Distributed version control software. |
| GitHub | Platform for hosting Git repositories. |
| Repository | Storage location for project history. |
| Staging | Selecting changes for the next commit. |
| Commit | A recorded snapshot of project changes. |
| Push | Sends local commits to a remote repository. |
| Pull | Retrieves and integrates remote changes. |
| Fetch | Downloads remote updates without merging. |
| Branch | An independent development path. |
| Merge | Combines changes from different branches. |
| Pull Request | Proposes changes for review and merging. |

---

## 🎓 8. Conclusion

Git and GitHub are essential tools in modern software development.

Git provides a reliable way to track code changes and manage project versions, while GitHub makes it easier to share projects, review contributions, and collaborate with other developers.

The best way to master these tools is to practice their commands on real projects and become familiar with the complete development workflow.

---

*Learning resource: Git and GitHub fundamentals | Beginner Level*