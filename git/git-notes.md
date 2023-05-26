# Git Notes

[Documentation](https://git-scm.com/doc)

## Vocabulary:
- Working directory: directory that you are working in
- Stagimg area: files that are going to be commited
- Repository: .git folder where changes are committed to

## Commands:

`git config`

Configure git with your info (required)

Options: 
- git config --global user.email "youremail@example.com"
- git config --global user.name "Name"
- git config --global core.editor "[editor](https://git-scm.com/book/en/v2/Appendix-C:-Git-Commands-Setup-and-Config)"

`git status`

Gives information on the current status of a git repository and its contents

`git init`

Create a new git repository
- stores git data in .git
- make sure you are not already in a git repo before running (git status)

`git add`

Elect the changes made you want to stage for commit
```
git add <file> #adds specified file
```
```
git add . #adds all files
```

`git commit`

- requires message that summarizes changes made
Commit changes from the staging area to the .git repository
```
git commit #uses configured default editor to create message
```
```
git commit -m <message> #specifies message
``` 
```
git commit --amend #make changes to previous commit
```

`git log`

Retrieves history of commits for repository

## Best Practices:
1. Atomic Commits: When possible, a commit should encompass a single feature, change, or fix.
	- Keep each commit focused on a single thing
	- Makes changes easy to track, review, and undo if needed
2. Commit Messages (Present Tense) - Describe your changes in imperative mood
	- "Make foo do something" NOT "Made foo do something"
## Other:

### Ignoring Files: 
We can tell Git which files to ignore in a given repository, using a .gitignore file
- Userful for Secrets, API keys, credentials, log files, dependencies, packages, etc
  - `.filename`  ignores file names
  - `/directory` ignores everything in directory
  - `*.txt` ignores all files with this file type
- [gitignore.io](https://gitignore.io) can help you get started on creating a .gitignore file	
