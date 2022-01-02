# Git Part-1
```python
// Creating Snapshots

// Initializing a repository
git init

// Staging files
git add file1.js // stages a single file
git add file1.js file2.js // stages multiple files
git add *.js // stages with a pattern
git add . // stages the current directory and all its content

// Viewing the status
git status // full status
git status -s // short status

// Committing the staged files
git commit -m 'Message' // commits with an one-line message
git commit // open the default editor to type a long message

// Skipping the staging area (Not Recommended)
git commit -am "Message"

// Removing Files
git rm file1.js // removes from working directory and staging area
git rm --cached file1.js // removes from staging area only

// Renaming or moving files
git mv file1.js file1.txt


// Viewing the staged/unstaged changes
git diff // shows unstaged changes
git diff --staged // shows staged changes
git diff --cached // same as the above

// Viewing the history
git log // full history
git log --oneline // summary
git log --reverse // lists the commits from the oldest to the newest

// Viewing a commit
git show 82la2ff // shows the given commit
git show HEAD // shows the last commit
git show HEAD~2 // Two Steps before the last commit
git show HEAD:file.js // shows the version of file.js stored in the last commit

// Unstaging files (undoing git add)
git restore --staged file.js // copies the last version of file.js from repo to index

// Discarding local changes
git restore file.js // copies file.js from index to woking directory
git restore file1.js file2.js // restore multiple files in wokring directory
git restore . // discards all local changes (except untracked files)
git clean -fd // removes all untracked files

// Restoring an earlier version of a file
git restore --source=HEAD~2 file.js
```