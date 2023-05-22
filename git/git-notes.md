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
git log: retrieves history of commits for repository
