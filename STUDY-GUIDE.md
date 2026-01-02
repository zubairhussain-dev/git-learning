# Git & GitHub Professional Study Guide
**Source:** [freeCodeCamp Git & GitHub Crash Course](https://www.freecodecamp.org/news/git-and-github-crash-course-for-beginners)

## 1. Initial Setup & Configuration
Before starting any project, ensure that Git is configured and the project folder is set up.

* **Configure User:** `git config --list`
    * *Checks your current username and email settings.*
* **Create Project Folder:**
    * `mkdir [folder-name]` (Make directory)
    * `cd [folder-name]` (Change directory into the folder)
* **Open in Editor:** `code .`
    * *Opens the current folder in VS Code.*
* **Initialize Git:** `git init`
    * *Transforms the current folder into a Git repository.*

## 2. The Basic Workflow (Staging & Committing)
This cycle is repeated for every change made to the code.

1. **Check Status:** `git status`
    * *Shows which files are modified, staged, or untracked.*
2. **Stage Changes:**
    * `git add .` (Stage all changes in the current directory)
    * `git add -A` or `git add --all` (Stages all changes across the entire project)
    * `git add *` (Stages new/modified files, but excludes deleted files)
3. **Commit Changes:** `git commit -m "Descriptive message"`
    * *Saves the snapshot of the staged files.*
4. **View History:** `git log --oneline`
    * *Shows a condensed history of commit hashes and messages.*

## 3. Remote Repositories (GitHub)
Connecting your local computer to the cloud.

* **Clone a Repo:** `git clone [url]`
    * *Downloads an existing repository from GitHub to your computer.*
* **Push Changes:** `git push origin main`
    * *Uploads your local commits to the GitHub repository.*
* **Fetch Updates:** `git fetch`
    * *Downloads remote changes but does not merge them yet.*
* **Pull Updates:** `git pull`
    * *Combines `fetch` + `merge`. Updates your current working directory with remote changes.*

## 4. Branching & Merging
Used to work on new features without breaking the main code.

* **Create Branch:** `git branch [branch-name]`
    * *Example: `git branch development`*
* **List Branches:** `git branch`
* **Switch Branch:**
    * `git checkout [branch-name]`
    * *Note: You can also use `git checkout [commit-id]` to view an old version (Detached HEAD state).*
* **Merge Branch:** `git merge [branch-name]`
    * *Combines the specified branch into the one you are currently on.*
* **Rebase:** `git rebase main`
    * *Moves your feature branch to begin from the current tip of the main branch (cleaner history).*

## 5. Undoing Changes & Deletions
Commands to fix mistakes or remove files.

* **Delete File:**
    * `git rm [file]` (Removes file from Git and disk)
    * `git rm -f [file]` (Force removal)
    * `git rm -r [folder]` (Recursive removal for folders)
* **Restore Files:**
    * `git restore .` (Discard all local changes in the working directory)
    * `git restore --staged .` (Unstage files but keep the changes in the folder)
* **Reset History:**
    * `git reset HEAD~` (Undo last commit, keep changes unstaged)
    * `git reset --hard` (Undo last commit and **delete** all changes)
* **Revert Commit:** `git revert [commit-id]`
    * *Creates a NEW commit that does the opposite of the specific old commit (Safe for shared repos).*

## 6. Stashing (Temporary Storage)
Useful when switching branches with unfinished work.

* **Save Stash:** `git stash`
* **View Stashes:** `git stash list`
* **Apply & Remove:** `git stash pop`
    * *Applies the latest stash and removes it from the list.*
* **Apply & Keep:** `git stash apply`
* **Delete Stash:** `git stash drop`