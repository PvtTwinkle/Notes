Documentation: git-scm.com

Vocabulary:

	Locations:
		working directory - directory that you are working in
		stagimg area - files that are going to be commited
		repository - .git folder where changes are committed to

Commands:

git config: configure git with your info (required)
	- git config --global user.email "youremail@example.com"
	- git config --global user.name "Name"
	- git config --global core.editor "nano -w"
git status: gives information on the current status of a git repository and its contents
git init: - create a new git repository
	- stores git data in .git
	- make sure you are not already in a git repo before running (git status)
git add: select the changes made you want to stage for commit
	- usage: git add <file>
	- to add all modified files, use "git add ."  
git commit: commit changes from the staging area to the .git repository
	- usages: git commit -m "message" 
	- requires message that summarizes changes made
	- redo the previous commit ussing "git commit --amend
git log: retrieves history of commits for repository

Best Practices:
	1. Atomic Commits - When possible, a commit should encompass a single feature, change, or fix.
		- Keep each commit focused on a single thing
		- Makes changes easy to track, review, and undo if needed
	2. Commit Messages (Present Tense) - Describe your changes in imperative mood
		- "Make foo do something" NOT "Made foo do something"
Other:

Ignoring Files: We can tell Git which files to ignore in a given repository, using a .gitignore file
	- Userful for Secrets, API keys, credentials, log files, dependencies, packages, etc
	- ".filename"  ignores file names
	- "/directory" ignores everything in directory
	- "*.txt" ignores all files with this file type
	- gitignore.io can help you get started on creating a .gitignore file	
