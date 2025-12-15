# Git – Core Concepts and Learnings

## ! What to Do When I’m Confused

1. **Check your branch**  
   `git branch` → make sure you are on the correct branch
2. **Check status**  
   `git status` → see which files are staged, unstaged, or untracked
3. **Check commit history**  
   `git log --oneline --decorate --all`
4. **Stage carefully**  
   Avoid `git add .` unless you know what will be included
5. **Commit small changes**  
   Keep each commit focused and meaningful
6. **Pull before push**  
   If unsure, do: `git pull origin <branch-name>` to avoid conflicts
7. **Review Pull Requests**  
   Use GitHub to merge changes, not just push blindly
8. **Ask for help or look at documentation**  
   Git is recoverable; mistakes are fixable

> Key mindset: Git is strict, but predictable. Always check status, branch, and staged files before committing or pushing.


## 1. What Git Is
Git is a **version control system**.  
It tracks changes in files and allows you to go back in time.

- Git works **locally on your computer**
- GitHub is a **remote platform** to store repositories online

Git does nothing automatically.  
Every step must be done **manually and explicitly**.

---

## 2. Repositories

### Local Repository
A local repository is a folder tracked by Git.

Create it with:
git init

This creates a hidden `.git` folder.

### Remote Repository
A remote repository lives on GitHub.

It is connected to the local repo with:
git remote add origin <repository-url>

---

## 3. The Git Workflow (Most Important)

Git always works in this order:

1. Create or edit files
2. Stage files
3. Commit changes
4. Push to GitHub

Commands:
git add <file>
git commit -m "meaningful message"
git push

### Golden Rule
> If a file is not staged, it will not be committed.  
> If it is not committed, it will not be pushed.

---

## 4. `git status` – Your Best Friend

git status

Shows:
- current branch
- staged files
- unstaged files
- untracked files

### Rule
> Always check `git status` before adding, committing, or pushing.

---

## 5. Staging Files (`git add`)

### What `git add` Does
- Moves files to the **staging area**
- Only staged files are included in the next commit

### Common Mistake
git add .

This adds **everything**, including:
- files from other tasks
- temporary folders
- mistakes

### Better Practice
git add path/to/file.md

### Rule
> Add files intentionally, not automatically.

---

## 6. Commits

A commit is a **snapshot** of staged changes.

Good commits are:
- small
- focused
- easy to understand

Example:
git commit -m "Add notes about Git branches"

### Rule
> One logical change equals one commit.

---

## 7. Branches

### What a Branch Is
A branch is an **independent line of work**.

- `main` is the stable branch
- feature branches are for tasks and experiments

Create a new branch:
git switch -c feature/my-task

Switch branches:
git switch <branch-name>

### Rule
> Real work happens on feature branches, not on `main`.

---

## 8. Folder Structure vs Branches

This is **very important**.

- Folders organize **files**
- Branches organize **work**

Example:
web-challenges/
css/
html/
javascript/

This is **one repository**, not multiple branches.

### Rule
> Folders are structure. Branches are workflow.

---

## 9. Working on a Feature Branch

Typical process:

1. Switch to feature branch
2. Create or edit files
3. Stage selected files
4. Commit changes
5. Push branch to GitHub

git push -u origin feature/my-task

---

## 10. Pull Requests (PR)

A Pull Request is created on **GitHub**.

It means:
> “Please merge my branch into another branch (usually `main`).”

Workflow:
1. Push feature branch
2. Open Pull Request on GitHub
3. Review
4. Merge

### Rule
> Pull Requests merge branches, not folders.

---

## 11. Merging Does NOT Delete Branches

After a merge:
- the branch still exists
- this is normal and expected

Delete branch manually if needed:
git branch -d feature/my-task
git push origin --delete feature/my-task

### Rule
> Merge does not mean delete.

---

## 12. `git pull`

git pull

Downloads changes from GitHub and applies them locally.

Use it when:
- a Pull Request was merged
- the remote branch changed

### Rule
> Pull when the remote changed — not randomly.

---

## 13. Untracked Files

Untracked files are:
- files Git sees
- but are not staged yet

They are **not an error**.

Add them only if needed:
git add <file>

### Rule
> Untracked means “not added”, not “wrong”.

---

## 14. The Three Git Areas (Mental Model)

Git has three states:

1. Working Directory (your files)
2. Staging Area (`git add`)
3. Repository (`git commit`)

### Rule
> If it is not staged, it is not committed.  
> If it is not committed, it is not pushed.

---

## 15. Final Safety Rules

- Always check your branch
- Use `git status` often
- Avoid `git add .`
- Do not panic — Git is recoverable

---

## One-Sentence Summary

Git is strict but predictable.  
Once the rules are clear, Git becomes calm and safe to use.

