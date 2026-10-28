# Git Practice Record

## Commands Used
* `git init -b main`: Initializes a new local Git repository with `main` as the default branch.
* `git config`: Sets user-specific configuration values like email and username.
* `git status`: Displays the state of the working directory and staging area.
* `git add <file>`: Adds specific file contents to the index (staging area) for the next commit.
* `git commit -m "<message>"`: Records the staged snapshots in the repository's history with a descriptive message.
* `git log --oneline`: Shows a compact version of the commit history.
* `git diff`: Shows unstaged changes between the working directory and the index.
* `git branch`: Lists, creates, or deletes branches.
* `git switch -c <branch>`: Creates a new branch and switches to it immediately.
* `git merge <branch>`: Integrates changes from a specified branch into the current branch.
* `git restore <file>`: Discards uncommitted local changes in the working directory.
* `git stash`: Temporarily shelves (stashes) changes you've made to your working copy.
* `git revert <commit>`: Creates a new commit that undoes the changes from a previous commit.
* `git remote add <name> <url>`: Connects the local repository to a remote server.
* `git push -u origin main`: Uploads local branch commits to the remote repository.
* `git fetch origin`: Downloads commits, files, and refs from the remote repository.
* `git pull --ff-only origin main`: Fetches and integrates remote changes using a fast-forward merge only.

## Merge Conflict Experience
During Exercise 9, a merge conflict was intentionally created by modifying the exact same line in the `mode.txt` file on two different branches (`main` and `feature/conflict-test`). 

When attempting to merge the feature branch into main using `git merge`, Git paused the merge and outputted a conflict warning. Inside the file, Git inserted standard conflict markers (`<<<<<<< HEAD`, `=======`, `>>>>>>> feature/conflict-test`). 

**Resolution:** 
I opened `mode.txt` in my editor, reviewed both changes, and manually deleted the conflict markers. I replaced the conflicting lines with the final agreed-upon text (`Mode: resolved`). After saving the file, I staged it using `git add mode.txt` and completed the merge using `git commit -m "Resolve merge conflict in mode.txt"`.
