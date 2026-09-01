# User Manual: Creating a GitHub Repository and Making a First Commit

## Prerequisites

Before starting, you need:

* A GitHub account.
* Git installed on your computer.
* Git Bash or another terminal.
* Basic computer literacy.
* An internet connection.

## Procedure

### Step 1: Open Git Bash

Open Git Bash on your computer.

**Expected result:** The Git Bash terminal opens and displays a command prompt.

### Step 2: Create a project folder

Run `mkdir my-first-project`.

**Expected result:** A folder named `my-first-project` is created.

### Step 3: Enter the project folder

Run `cd my-first-project`.

**Expected result:** The terminal moves into the `my-first-project` folder.

### Step 4: Initialize Git

Run `git init`.

**Expected result:** Git initializes a local repository in the project folder.

### Step 5: Create a README file

Create a file named `README.md`.

**Expected result:** The `README.md` file appears in the project folder.

### Step 6: Add project information

Add a short description of the project to `README.md`.

**Expected result:** The README contains information describing the project.

### Step 7: Check the repository status

Run `git status`.

**Expected result:** Git displays the current status of the repository and identifies the README file.

### Step 8: Stage the README file

Run `git add README.md`.

**Expected result:** The README file is added to the staging area.

### Step 9: Make the first commit

Run `git commit -m "Initial commit"`.

**Expected result:** Git creates the first commit and displays the commit information.

### Step 10: Create a GitHub repository

Create a new repository on GitHub.

**Expected result:** A new GitHub repository is created and its repository page opens.

### Step 11: Connect the local repository

Add the GitHub repository as the remote named `origin`.

**Expected result:** The local repository is connected to the GitHub repository.

### Step 12: Push the commit

Run `git push -u origin main`.

**Expected result:** The first commit appears in the GitHub repository.

## Screenshot Description

Include a screenshot of the GitHub repository after the first commit has been pushed. The screenshot should show the repository name, the `README.md` file, and evidence that the first commit is present.

## Troubleshooting

**Problem: `src refspec main does not match any`**

This error commonly occurs when there is no commit on the local repository or the branch has a different name. Check the repository status and make sure you have created a commit. If necessary, rename the branch to `main` using `git branch -M main`, then run the push command again.
