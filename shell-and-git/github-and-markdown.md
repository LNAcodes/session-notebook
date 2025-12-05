Git Workflow Notes
Initialize a repository

Navigate to your project folder: cd <folder-name>

Initialize Git: git init

Check status: git status

Adding files

Stage a single file: git add <file-name>

Stage multiple specific files: git add file1 file2 folder/file3

⚠️ Avoid using git add . blindly – this stages everything, which can include unwanted files.

Commit

Commit staged changes: git commit -m "meaningful message"

Commit regularly after each step.

Use clear commit messages like "Add initial HTML files" or "Update CSS layout".

Branching

Create and switch to a new feature branch: git switch -c <branch-name>

Example: git switch -c notes/github-and-markdown

Check current branch: git branch

Pushing to remote

Connect to remote repository (first time): git remote add origin <ssh-or-https-link>

Push a new branch: git push -u origin <branch-name>

Example: git push -u origin notes/github-and-markdown

Editing files in terminal

Create a new file: touch folder/file.md

Open it in Nano: nano folder/file.md

Add your notes or commands.

Save in Nano: Ctrl + O → Enter

Exit Nano: Ctrl + X

Workflow tip

Commit after each meaningful step.

Avoid staging everything unless you really want all files included.

Use branches for features or session notes.

Push branches regularly and create Pull Requests for review.
