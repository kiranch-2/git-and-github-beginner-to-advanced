# Git Clone — Cloning a GitHub Repository to Ubuntu

........................................................................................................

## 1. What is Git Clone?

`git clone` is used to copy a GitHub repository from the online GitHub server to our local computer.

After cloning, we get a local copy of the repository on our Ubuntu computer.

This allows us to work on the project using the Ubuntu Terminal and Git commands.

........................................................................................................

## 2. GitHub Repository vs Local Repository

### GitHub Repository

This is the online version of our project stored on GitHub.

### Local Repository

This is the copy of the same repository stored on our Ubuntu computer.

### Simple Understanding

GitHub Repository = Online

Local Repository = Our Computer

`git clone` connects these two by creating a local copy of the GitHub repository.

........................................................................................................

## 3. Before Cloning

Before using `git clone`, make sure:

1. Git is installed on Ubuntu.
2. The required repository exists on GitHub.
3. We have the GitHub repository URL.
4. We know where we want to store the repository on our computer.

To check whether Git is installed:

git --version

........................................................................................................

## 4. Step 1 — Open Ubuntu Terminal

Press:

Ctrl + Alt + T

This opens the Ubuntu Terminal.

........................................................................................................

## 5. Step 2 — Check the Current Location

Command:

pwd

### Purpose

`pwd` shows the current directory/location in the Terminal.

Example:

/home/username

This helps us understand where the repository will be cloned.

........................................................................................................

## 6. Step 3 — Check the Files and Folders

Command:

ls

### Purpose

`ls` lists the files and folders available in the current directory.

Example:

Desktop
Documents
Downloads
Music
Pictures
Public
Templates
Videos

........................................................................................................

## 7. Step 4 — Copy the Repository URL from GitHub

Open the required repository on GitHub.

Click:

Code → HTTPS

Copy the repository URL.

Example:

https://github.com/USERNAME/REPOSITORY.git

Do not type the actual URL manually if it can be copied directly from GitHub.

........................................................................................................

## 8. Step 5 — Clone the Repository

Use:

git clone <GitHub-repository-URL>

Example:

git clone https://github.com/USERNAME/REPOSITORY.git

Press Enter.

Git will download the repository from GitHub to the current location on the Ubuntu computer.

........................................................................................................

## 9. What Happens During Cloning?

When `git clone` runs, Git:

1. Creates a folder using the repository name.
2. Downloads the repository files.
3. Downloads the Git history.
4. Sets up the local Git repository.
5. Connects the local repository with the remote GitHub repository.

After successful cloning, the repository is available on the local computer.

........................................................................................................

## 10. Step 6 — Check the Cloned Repository

Run:

ls

The newly cloned repository folder should now appear.

Example:

Crypto-Analysis

........................................................................................................

## 11. Step 7 — Enter the Repository

Use:

cd Crypto-Analysis

Replace `Crypto-Analysis` with the actual repository name.

After entering the repository, run:

ls

This will show the files and folders inside the repository.

........................................................................................................

## 12. Step 8 — Check Git Status

Command:

git status

This shows the current status of the local Git repository.

If there are no changes, Git may show:

nothing to commit, working tree clean

This means there are no uncommitted changes.

........................................................................................................

## 13. Step 9 — Check the Remote GitHub Repository

Command:

git remote -v

This shows the GitHub repository connected to the local repository.

Example:

origin  https://github.com/USERNAME/REPOSITORY.git (fetch)

origin  https://github.com/USERNAME/REPOSITORY.git (push)

### Meaning

`origin` is the default name given to the remote GitHub repository.

`fetch` refers to getting information or changes from GitHub.

`push` refers to sending our committed changes to GitHub.

........................................................................................................

## 14. Complete Cloning Workflow

Open Terminal:

Ctrl + Alt + T

Check current location:

pwd

Check available folders:

ls

Copy the repository URL from GitHub.

Clone the repository:

git clone <GitHub-repository-URL>

Check the repository:

ls

Enter the repository:

cd <repository-name>

Check files:

ls

Check Git status:

git status

Check the GitHub connection:

git remote -v

........................................................................................................

## 15. Example — Our Crypto Analysis Repository

Suppose our GitHub repository is:

Crypto-Analysis

The command would be:

git clone https://github.com/USERNAME/Crypto-Analysis.git

Then:

cd Crypto-Analysis

Then:

ls

We can now see our project folders, for example:

theta

ARRR

fundamental-analysis

........................................................................................................

## 16. Important Note

`git clone` is normally used when we want to bring an existing GitHub repository to a computer for the first time.

We do not normally clone the same repository again every time we want to work on it.

Once the repository has been cloned, we can open the existing local repository and use Git commands such as:

git status

git pull

git add

git commit

git push

........................................................................................................

## 17. Git Clone vs Git Pull

### git clone

Used to create a local copy of a GitHub repository for the first time.

### git pull

Used later to bring the latest changes from GitHub into an existing local repository.

### Simple Difference

git clone = Get the repository for the first time

git pull = Get the latest changes later

........................................................................................................

## 18. Common Mistake

If Terminal shows:

git: command not found

Git is not installed on the computer.

Install Git first using:

sudo apt update

sudo apt install git

Then verify:

git --version

........................................................................................................

## 19. Another Common Mistake

If we run:

cd Crypto-Analysis

and Ubuntu says:

No such file or directory

the repository may not have been cloned in the current location, or the repository name may be different.

First check:

ls

Then use the exact folder name shown by `ls`.

........................................................................................................

## 20. Learning Sequence After Cloning

After cloning a repository, our next learning steps are:

1. Understand the local repository.
2. Create and edit files.
3. Rename files and folders.
4. Check changes using `git status`.
5. Stage changes using `git add`.
6. Save changes using `git commit`.
7. Upload changes using `git push`.
8. Get updated changes using `git pull`.

........................................................................................................

## 21. Key Commands

Check Git version:

git --version

Check current location:

pwd

List files and folders:

ls

Clone repository:

git clone <GitHub-repository-URL>

Enter repository:

cd <repository-name>

Check repository status:

git status

Check remote connection:

git remote -v

........................................................................................................

## 22. Summary

`git clone` creates a local copy of an existing GitHub repository.

The basic process is:

GitHub Repository

↓

Copy Repository URL

↓

Open Ubuntu Terminal

↓

git clone <URL>

↓

Local Repository Created

↓

cd <repository-name>

↓

ls

↓

git status

........................................................................................................
