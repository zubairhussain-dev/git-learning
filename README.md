# Git Learning Journey
This repository documents my progress through the [freeCodeCamp Git & GitHub Crash Course](https://www.freecodecamp.org/news/git-and-github-crash-course-for-beginners). It serves as a personal cheat sheet for common and advanced Git commands.

## 1. Setup & Configuration
| Command | Description |
| :--- | :--- |
| `git config --list` | View current configuration settings |
| `git init` | Initialize a new Git repository |
| `git clone [url]` | Clone a repository from GitHub to local machine |
| `git status` | Check the status of changed or staged files |

## 2. Staging & Committing
| Command | Description |
| :--- | :--- |
| `git add .` | Stage **all** changes in the current directory |
| `git add --all` / `-A` | Stage every change across the entire project |
| `git commit -m "msg"` | Commit staged changes with a descriptive message |
| `git log --oneline` | View a simplified version of the commit history |

## 3. Branching & Merging
| Command | Description |
| :--- | :--- |
| `git branch` | List all local branches |
| `git branch [name]` | Create a new branch (e.g., `development`) |
| `git checkout [name]` | Switch to a specific branch |
| `git switch -c [name]` | Create and switch to a new branch (modern syntax) |
| `git merge [branch]` | Merge the specified branch into the current one |
| `git rebase [main]` | Reapply commits on top of another base tip |

## 4. Undoing Changes (Danger Zone)
| Command | Description |
| :--- | :--- |
| `git restore .` | Discard local changes in the current directory |
| `git reset HEAD~` | Undo the last commit but keep changes in working dir |
| `git reset --hard` | **Force** undo changes (deletes unstaged work) |
| `git revert [id]` | Create a *new* commit that reverses a previous specific commit |

## 5. Stashing (Temporary Saves)
*Useful when you need to switch branches but aren't ready to commit.*
| Command | Description |
| :--- | :--- |
| `git stash` | Temporarily save changes |
| `git stash list` | View all stashed changes |
| `git stash pop` | Apply the stash and remove it from the list |
| `git stash apply` | Apply the stash but keep it in the list |
| `git stash drop` | Delete a specific stash |

## 6. Remote Commands
| Command | Description |
| :--- | :--- |
| `git fetch` | Download changes from remote but do not merge |
| `git pull` | Download **and** merge changes (`fetch` + `merge`) |
| `git push origin main` | Upload local commits to GitHub |

[cite_start]*(Based on my notes and the tutorial [cite: 1])*