# Git Commands Cheat Sheet

## Basic Local Commands

| Command | Purpose |
|:---|:---|
| `git init` | Start a new Git repository in your folder. |
| `git status` | See what has changed or is ready to commit. |
| `git add .` | Stage **all** changed files for commit. |
| `git add filename` | Stage a **specific** file for commit. |
| `git commit -m "your message"` | Save your staged changes with a message. |
| `git log` | See a list/history of your commits. |
| `git diff` | See what has changed before committing. |
| `git clone [repo-url]` | Copy (download) a GitHub repository to your machine. |
| `git checkout branch-name` | Switch to another branch. |
| `git checkout -b new-branch-name` | Create and switch to a **new** branch. |
| `git pull` | Bring down (download) latest changes from GitHub. |
| `git push` | Upload your commits to GitHub. |

## Remote Commands (GitHub)

| Command | Purpose |
|:---|:---|
| `git remote add origin [repo-url]` | Connect your local repo to a GitHub repo. |
| `git branch -M main` | Rename your branch to **main** (common default). |
| `git push -u origin main` | Push code and link your local branch to GitHub. |
| `git fetch` | Download updates from GitHub (without merging). |
| `git merge branch-name` | Merge another branch into your current branch. |

## Helpful Extra Commands

| Command | Purpose |
|:---|:---|
| `git reset --hard` | Undo all changes (⚡ careful! wipes unsaved work). |
| `git stash` | Temporarily save changes without committing. |
| `git stash pop` | Retrieve your stashed changes. |
| `git remote -v` | Show linked GitHub repository URL(s). |
| `git commit --amend` | Modify the last commit message or add forgotten changes. |
| `git reset --soft HEAD~1` | Undo last commit but keep changes staged. |
| `git reset --mixed HEAD~1` | Undo last commit and unstage the changes (keep files). |
| `git reset --hard HEAD~1` | Completely remove last commit and all changes (⚡ permanent). |
| `git revert HEAD` | Create a new commit that undoes the last commit (safe way). |

## Typical Workflow

```bash
git status
git add .
git commit -m "Meaningful message"
git push
```

---

# Notes
- Use `git commit --amend` immediately after a wrong commit.
- Use `git reset` carefully; it can cause data loss if `--hard` is used.
- Use `git stash` if you need to switch branches but aren't ready to commit.

---

# Good Practice
- Always write clear commit messages.
- Pull changes before pushing if working in a team.
- Backup your repo before using destructive commands like `reset --hard`.

