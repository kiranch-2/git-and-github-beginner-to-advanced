# Git Installation on Ubuntu

........................................................................................................

## 1. Why Do We Need Git?

Git is a version-control tool.

It allows us to manage changes in our files and synchronize our local projects with GitHub repositories.

GitHub is the online platform where our repositories are stored.

Git is the software installed on our Ubuntu computer that allows us to work with GitHub repositories from the Terminal.

........................................................................................................

## 2. Step 1 — Update Ubuntu Package Information

### Command

sudo apt update

### Meaning

**sudo** = SuperUser Do  
Runs the command with administrator privileges.

**apt** = Advanced Package Tool  
Ubuntu's package-management system.

**update** = Refreshes the package information available to Ubuntu.

### Important

`sudo apt update` does not install Git.

It only refreshes Ubuntu's information about available software packages and their latest versions.

........................................................................................................

## 3. Step 2 — Install Git

### Command

sudo apt install git

### Meaning

This command installs the Git software on Ubuntu using administrator privileges.

### If Ubuntu asks:

Do you want to continue? [Y/n]

Type:

Y

and press Enter.

........................................................................................................

## 4. Step 3 — Verify Git Installation

### Command

git --version

If Git is installed successfully, Ubuntu will show something similar to:

git version 2.x.x

The exact version number may be different.

........................................................................................................

## 5. Commands Used

sudo apt update

sudo apt install git

git --version

........................................................................................................

## 6. Git vs GitHub

### Git

Git is a version-control software installed on our computer.

### GitHub

GitHub is an online platform where Git repositories can be hosted and shared.

### Simple Difference

Git = Tool

GitHub = Online Platform

........................................................................................................

## 7. What Happens After Git Installation?

After installing Git, we can clone a GitHub repository to our Ubuntu computer.

### Example

git clone <GitHub-repository-URL>

After cloning, the repository will exist on our local computer.

We can then work with the repository using Git commands such as:

git status

git add

git commit

git push

git pull

........................................................................................................

## 8. Learning Sequence

Git Installation

↓

GitHub Repository Clone

↓

Local Repository

↓

Files and Folders

↓

Rename Files/Folders

↓

git status

↓

git add

↓

git commit

↓

git push

↓

git pull

........................................................................................................

## 9. Important Note

Git needs to be installed only once on the Ubuntu computer.

After Git is installed successfully, we do not need to run the installation commands every time we want to use Git.

We can directly use Git commands such as:

git status

git add

git commit

git push

git pull

........................................................................................................

## 10. Next Step

The next step is to connect our local Ubuntu environment with a GitHub repository.

We will learn how to:

1. Copy the GitHub repository URL.
2. Clone the repository to Ubuntu.
3. Open the local repository using Terminal.
4. Check files and folders using `ls`.
5. Make changes locally.
6. Rename files or folders.
7. Commit the changes.
8. Push the changes back to GitHub.

........................................................................................................
