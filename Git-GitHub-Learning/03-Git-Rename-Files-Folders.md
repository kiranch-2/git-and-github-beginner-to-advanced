# Git Rename Files and Folders

........................................................................................................

## 1. Why Do We Need to Rename Files and Folders?

While working on a project, we may sometimes need to change the name of a file or folder.

For example:

A folder may have been created with the wrong name:

undamental-analysis

but the correct name should be:

fundamental-analysis

Similarly, a file may have a spelling mistake or may need a clearer name.

Git allows us to rename files and folders while keeping track of the change.

........................................................................................................

## 2. Important Concept — Git Tracks Files, Not Empty Folders

Git tracks files and the changes made to them.

Git does not directly track empty folders.

This means an empty folder normally does not appear in a Git repository.

A folder becomes part of a Git repository when it contains files that Git can track.

### Example

Suppose we have:

fundamental-analysis/

and inside it:

README.md

Git tracks:

fundamental-analysis/README.md

The folder itself is not tracked separately.

........................................................................................................

## 3. Before Renaming a File or Folder

Before renaming anything, first make sure that:

1. Git is installed.
2. The GitHub repository has already been cloned.
3. We are inside the correct local repository.
4. The file or folder exists.
5. We know the old name and the new name.

Check Git:

git --version

Check the current location:

pwd

Check files and folders:

ls

........................................................................................................

## 4. Step 1 — Open the Ubuntu Terminal

Press:

Ctrl + Alt + T

This opens the Ubuntu Terminal.

........................................................................................................

## 5. Step 2 — Go to the Local Repository

Use the `cd` command to enter the local Git repository.

Example:

cd Crypto-Analysis

Replace `Crypto-Analysis` with the actual repository name.

Then check the current location:

pwd

........................................................................................................

## 6. Step 3 — Check the Files and Folders

Run:

ls

This shows the files and folders available in the current repository.

Example:

theta

ARRR

undamental-analysis

README.md

Suppose we want to rename:

undamental-analysis

to:

fundamental-analysis

........................................................................................................

## 7. Step 4 — Check the Current Git Status

Before making changes, it is good practice to check the repository status.

Command:

git status

This tells us whether there are already any uncommitted changes.

If everything is clean, Git may show:

nothing to commit, working tree clean

This means there are no pending changes before we start the rename operation.

........................................................................................................

## 8. Renaming a File Using Git

The Git command for renaming a file is:

git mv old-file-name new-file-name

### Example

Suppose the file is:

old-notes.md

and we want to rename it to:

new-notes.md

Command:

git mv old-notes.md new-notes.md

Git will rename the file and automatically stage the rename.

........................................................................................................

## 9. Renaming a Folder Using Git

The same `git mv` command can be used to rename a folder.

Syntax:

git mv old-folder-name new-folder-name

### Example

Suppose the existing folder is:

undamental-analysis

and we want to rename it to:

fundamental-analysis

Command:

git mv undamental-analysis fundamental-analysis

Press Enter.

The folder will be renamed locally.

........................................................................................................

## 10. Check the Renamed Folder

After renaming the folder, run:

ls

The old folder name should no longer appear.

Instead, we should see:

fundamental-analysis

........................................................................................................

## 11. Check Git Status After Renaming

Run:

git status

Git should detect the rename.

The output may show something similar to:

renamed:    undamental-analysis/README.md -> fundamental-analysis/README.md

The exact output can vary depending on the files inside the folder.

This confirms that Git has detected the rename.

........................................................................................................

## 12. Why Does Git Show the File Instead of the Folder?

Git tracks files rather than folders.

Therefore, when we rename a folder containing files, Git identifies the change through the files inside that folder.

For example:

Before:

undamental-analysis/README.md

After:

fundamental-analysis/README.md

Git understands that the tracked file has moved from the old folder path to the new folder path.

........................................................................................................

## 13. Alternative Method — Using the mv Command

Linux also provides the `mv` command for renaming files and folders.

### Rename a file

mv old-file-name new-file-name

### Rename a folder

mv old-folder-name new-folder-name

Example:

mv undamental-analysis fundamental-analysis

However, when working with a Git repository, using:

git mv

is convenient because Git immediately recognizes the rename and stages the change.

........................................................................................................

## 14. Difference Between mv and git mv

### Linux `mv`

Command:

mv old-name new-name

This renames or moves the file/folder at the Linux level.

Git will detect the change later when we check or stage the repository.

### Git `mv`

Command:

git mv old-name new-name

This renames or moves the file/folder and stages the change for Git.

### Simple Difference

`mv` = Linux rename/move

`git mv` = Git-aware rename/move

........................................................................................................

## 15. Example — Renaming Our Folder

Suppose our repository contains:

Crypto-Analysis

Inside it:

theta

ARRR

undamental-analysis

README.md

We want to correct:

undamental-analysis

to:

fundamental-analysis

First enter the repository:

cd Crypto-Analysis

Check the folders:

ls

Rename the folder:

git mv undamental-analysis fundamental-analysis

Check the folders again:

ls

Then check Git:

git status

........................................................................................................

## 16. What Happens When We Use git mv?

When we run:

git mv undamental-analysis fundamental-analysis

Git performs two things:

1. The folder/file path is renamed locally.
2. The rename is staged for the next commit.

Therefore, after the command, `git status` can show the rename as a staged change.

........................................................................................................

## 17. Check the Staged Changes

Command:

git status

For more detailed information about the staged changes, we can also use:

git diff --cached

This shows the changes that are currently staged and ready to be committed.

........................................................................................................

## 18. Commit the Rename

After confirming that the rename is correct, create a commit.

Command:

git commit -m "Rename fundamental analysis folder"

This saves the rename operation in Git history.

### Important

The commit message should clearly describe what changed.

For example:

Rename fundamental analysis folder

is better than:

Changes

because the first message explains exactly what was changed.

........................................................................................................

## 19. Push the Rename to GitHub

After committing, the rename exists in the local Git repository.

To upload the change to GitHub, use:

git push

Git will send the committed rename to the connected GitHub repository.

After the push completes successfully, open the repository on GitHub and verify the new name.

........................................................................................................

## 20. Complete File Rename Workflow

Suppose we want to rename:

old-notes.md

to:

git-notes.md

The complete workflow is:

Check repository:

git status

Rename the file:

git mv old-notes.md git-notes.md

Check status:

git status

Review staged changes:

git diff --cached

Commit:

git commit -m "Rename Git notes file"

Push to GitHub:

git push

........................................................................................................

## 21. Complete Folder Rename Workflow

Suppose we want to rename:

undamental-analysis

to:

fundamental-analysis

The complete workflow is:

Enter repository:

cd Crypto-Analysis

Check files and folders:

ls

Check Git status:

git status

Rename the folder:

git mv undamental-analysis fundamental-analysis

Check files and folders:

ls

Check Git status:

git status

Review staged changes:

git diff --cached

Commit the rename:

git commit -m "Rename fundamental analysis folder"

Push to GitHub:

git push

........................................................................................................

## 22. What Happens on GitHub?

Before the push:

GitHub contains:

undamental-analysis

After the local rename and commit:

Local repository contains:

fundamental-analysis

After:

git push

GitHub will be updated with the new name:

fundamental-analysis

The old name will no longer be the current folder path.

........................................................................................................

## 23. Important — Rename Only Happens Locally Until We Push

Running:

git mv old-name new-name

changes the local repository.

Running:

git commit

saves the change in local Git history.

Running:

git push

uploads the committed change to GitHub.

### Simple Understanding

git mv

↓

Rename locally and stage

↓

git commit

↓

Save change in local Git history

↓

git push

↓

Update GitHub

........................................................................................................

## 24. Renaming a File and Changing Its Content

Sometimes we may rename a file and also edit its contents.

For example:

old-notes.md

becomes:

git-notes.md

and then we modify the contents.

In this case, Git can track both:

1. The rename.
2. The content changes.

Check the changes using:

git status

For detailed unstaged changes:

git diff

For staged changes:

git diff --cached

........................................................................................................

## 25. Renaming Multiple Files

Multiple files can be renamed one by one using:

git mv old-file-1.md new-file-1.md

git mv old-file-2.md new-file-2.md

git mv old-file-3.md new-file-3.md

Then check:

git status

Review:

git diff --cached

Commit:

git commit -m "Rename documentation files"

Push:

git push

........................................................................................................

## 26. Renaming a Folder That Contains Multiple Files

Suppose we have:

undamental-analysis/

Inside it:

README.md

crypto-analysis.md

checklist.md

If we run:

git mv undamental-analysis fundamental-analysis

the entire folder path is renamed.

The files become:

fundamental-analysis/README.md

fundamental-analysis/crypto-analysis.md

fundamental-analysis/checklist.md

Git tracks the path changes of the files inside the folder.

........................................................................................................

## 27. Important Naming Rules

When creating or renaming files and folders, use clear and consistent names.

Recommended:

fundamental-analysis

git-notes.md

python-learning

Useful naming style:

lowercase-with-hyphens

Avoid unnecessary spaces and confusing names.

For example:

fundamental analysis

can be replaced with:

fundamental-analysis

This makes command-line work easier.

........................................................................................................

## 28. Common Mistake — Wrong Old Name

If we run:

git mv undamental-analysis fundamental-analysis

but the folder does not exist in the current location, Git may show an error.

First check:

ls

Use the exact name shown by the Terminal.

Linux is case-sensitive.

For example:

Fundamental-Analysis

and:

fundamental-analysis

are treated as different names.

........................................................................................................

## 29. Common Mistake — Wrong Repository Location

If Git says that a file or folder cannot be found, first check:

pwd

Then:

ls

Make sure we are inside the correct repository.

For example:

cd Crypto-Analysis

Then:

ls

........................................................................................................

## 30. Common Mistake — Forgetting to Commit

Renaming the file or folder locally does not permanently save the change in Git history.

After the rename, we should create a commit:

git commit -m "Rename fundamental analysis folder"

Without a commit, the rename remains an uncommitted/staged local change.

........................................................................................................

## 31. Common Mistake — Forgetting to Push

A commit saves the change in the local Git repository.

It does not automatically update GitHub.

To update GitHub, run:

git push

### Simple Difference

git commit = Save in local Git history

git push = Upload committed changes to GitHub

........................................................................................................

## 32. Verify the Final Result

After:

git push

check the repository on GitHub.

Verify that:

1. The new file/folder name is visible.
2. The old name is no longer the current path.
3. The files are present in the correct location.

We can also check the local repository:

ls

and:

git status

If everything is synchronized, Git may show:

nothing to commit, working tree clean

........................................................................................................

## 33. Complete Rename Workflow — From Start to Finish

### Example

Old folder:

undamental-analysis

New folder:

fundamental-analysis

### Step 1 — Open Terminal

Ctrl + Alt + T

### Step 2 — Enter Repository

cd Crypto-Analysis

### Step 3 — Check Current Location

pwd

### Step 4 — Check Files and Folders

ls

### Step 5 — Check Git Status

git status

### Step 6 — Rename the Folder

git mv undamental-analysis fundamental-analysis

### Step 7 — Check the Result

ls

### Step 8 — Check Git Status Again

git status

### Step 9 — Review Staged Changes

git diff --cached

### Step 10 — Commit

git commit -m "Rename fundamental analysis folder"

### Step 11 — Push to GitHub

git push

### Step 12 — Verify on GitHub

Open the GitHub repository and check that:

fundamental-analysis

is present.

........................................................................................................

## 34. Key Commands

Check Git version:

git --version

Check current location:

pwd

List files and folders:

ls

Enter repository:

cd <repository-name>

Check Git status:

git status

Rename a file:

git mv old-file-name new-file-name

Rename a folder:

git mv old-folder-name new-folder-name

Review staged changes:

git diff --cached

Commit changes:

git commit -m "Commit message"

Push changes to GitHub:

git push

........................................................................................................

## 35. Git Rename Workflow at a Glance

For a file:

git mv old-file.md new-file.md

↓

git status

↓

git diff --cached

↓

git commit -m "Rename file"

↓

git push

For a folder:

git mv old-folder new-folder

↓

git status

↓

git diff --cached

↓

git commit -m "Rename folder"

↓

git push

........................................................................................................

## 36. Summary

Git provides the `git mv` command for renaming or moving tracked files and folders.

### File Rename

git mv old-file-name new-file-name

### Folder Rename

git mv old-folder-name new-folder-name

### Check Status

git status

### Review Staged Changes

git diff --cached

### Commit

git commit -m "Rename file or folder"

### Push to GitHub

git push

### Complete Process

Rename

↓

Check

↓

Review

↓

Commit

↓

Push

↓

Verify on GitHub

........................................................................................................
