# Git and GitHub: Complete Guide

This `README.md` serves as a comprehensive guide to understanding and using **Git** (version control system) and **GitHub** (a cloud-based Git repository hosting service).

---

## 📚 Table of Contents

1. [What is Git?](#what-is-git)
2. [What is GitHub?](#what-is-github)
3. [Installation](#installation)
4. [Git Configuration](#git-configuration)
5. [Basic Git Commands](#basic-git-commands)
6. [Git Branching](#git-branching)
7. [Remote Repositories](#remote-repositories)
8. [GitHub Collaboration Workflow](#github-collaboration-workflow)
9. [GitHub Features](#github-features)
10. [Best Practices](#best-practices)
11. [Common Issues & Fixes](#common-issues--fixes)
12. [Resources](#resources)

---

## 🔧 What is Git?

Git is a distributed version control system used to track changes in source code during software development. It allows multiple developers to work on the same project without interfering with each other.

---

## ☁️ What is GitHub?

GitHub is a hosting platform for Git repositories that adds additional features like issue tracking, pull requests, Actions (CI/CD), and more. It’s commonly used for open-source collaboration and team-based development.

---

## 🛠️ Installation

### Install Git

- **Windows**: [Download Git for Windows](https://git-scm.com/download/win)
- **macOS**: `brew install git`
- **Linux**: `sudo apt install git` or `sudo yum install git`

---

## ⚙️ Git Configuration

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --global core.editor "code --wait"
git config --global init.defaultBranch main

To check config:

git config --list

## 🧪 Basic Git Commands

| Task            | Command                         |
| --------------- | ------------------------------- |
| Initialize repo | `git init`                      |
| Clone repo      | `git clone <url>`               |
| Check status    | `git status`                    |
| Add file(s)     | `git add <file>` or `git add .` |
| Commit          | `git commit -m "Message"`       |
| View history    | `git log`                       |
| See changes     | `git diff`                      |

## 🌿 Git Branching

git branch                   # List branches
git branch <branch-name>     # Create branch
git checkout <branch-name>   # Switch branch
git checkout -b <branch>     # Create and switch
git merge <branch>           # Merge into current
git branch -d <branch>       # Delete branch

## 🌍 Remote Repositories

git remote add origin <url>        # Link to remote
git push -u origin main            # Push to GitHub
git pull origin main               # Pull from GitHub
git fetch                          # Fetch changes
git remote -v                      # Show remotes

## 🤝 GitHub Collaboration Workflow

Fork → Make a copy of a repository.
Clone → Get it locally with git clone.
Create a branch → git checkout -b feature-x
Make changes → Edit files.
Stage & Commit → git add . && git commit -m "Message"
Push changes → git push origin feature-x
Create a Pull Request on GitHub.
Review & Merge.

## 🌟 GitHub Features

Issues: Bug tracking and feature requests.
Pull Requests: Propose, review, and merge code.
Actions: CI/CD workflows.
Projects: Kanban-style project management.
Wiki: Documentation inside the repo.
Insights: Contribution graphs and statistics.

## ✅ Best Practices

Use meaningful commit messages.
Make frequent, smaller commits.
Use .gitignore to avoid committing sensitive or unnecessary files.
Always pull before you push.
Use branches for features/fixes.
Keep main/master branch clean and deployable.

## 🧯 Common Issues & Fixes

| Problem            | Solution                                         |
| ------------------ | ------------------------------------------------ |
| Merge conflict     | Manually edit, then `git add` and `git commit`   |
| Forgot to add file | `git add <file>` then `git commit --amend`       |
| Undo last commit   | `git reset --soft HEAD~1`                        |
| Discard changes    | `git checkout -- <file>` or `git restore <file>` |


## 📚 Resources

Official Git Documentation - https://git-scm.com/doc
GitHub Docs - https://docs.github.com/
Git Cheat Sheet - https://education.github.com/git-cheat-sheet-education.pdf
Learn Git Branching - https://learngitbranching.js.org/
