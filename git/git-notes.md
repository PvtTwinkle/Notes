# Git Notes
[Documentation](https://git-scm.com/doc)
## **Vocabulary:**
- **Working directory:** directory that you are working in
- **Stagimg area:** files that are going to be commited
- **Repository:** .git folder where changes are committed to
## **Commands:**
### `git config`
Configure git with your info (required)
Options: 
- git config --global user.email "youremail@example.com"
- git config --global user.name "Name"
- git config --global core.editor "[editor](https://git-scm.com/book/en/v2/Appendix-C:-Git-Commands-Setup-and-Config)"

### `git status`
Gives information on the current status of a git repository and its contents
### `git init`
Create a new git repository
- stores git data in .git
- make sure you are not already in a git repo before running (git status)
### `git add`
Elect the changes made you want to stage for commit
#### Options:
- Add a specific file with `git add <file>`
- Add all modified files with `git add .`
### `git commit`
Commit changes from the staging area to the .git repository
- Requires message that summarizes changes made
Options:
- Using `git commit` on its own will use the configured default editor to write message
- Using `git commit -m <message>` will specify the message in the command
- Using `git commit --amend` will make changes to the previous commit
- Using `git commit -a` will automatically add all modified files
### `git log`
Retrieves history of commits for repository
### `git branch`
View existing branches
- Create a branch with ` git branch <branch-name>`
- Delete a branch with `git branch -d <branch-name>`
- Rename current branch with `git branch -m <new-branch-name>`
### `git switch <branch-name>`
Switch to another branch name
- Create and switch to a new branch with `git switch -c 
- Unstaged changes will be overwritten if there is conflict (modified file that exists in both branches)
- Unstaged changes will come with you to new branch if there is no conflict (File doesn't exist in other branch)
### `git checkout`
Create and switch to a new branch
- Also has a ton of more features than git switch
### `git merge`
Merge two branches into one another
- You merge to the head branch (branch you are currently in), 
  1. Switch to the branch you want to merge to
  2. Use `git merge <merging-branch>`
- Fast Forward Merge: Moving branch head/pointer forward to the head/pointer of another branch
- Merge Commit: Merging two branches that have different commits since branching
  - Can result in conflicts
- Resolving Conflicts:
  - Open up the files(s) with merge confilcts
  - Edit the files(s) to remove the conflicts. Decide which branch's content you want to keep in each conflict. Or keep the content from both. 
  - Remove the conflict "markers" in the document
  - Add your changes and then make a commit!   
## **Best Practices:**
1. Atomic Commits: When possible, a commit should encompass a single feature, change, or fix.
	- Keep each commit focused on a single thing
	- Makes changes easy to track, review, and undo if needed
2. Commit Messages (Present Tense) - Describe your changes in imperative mood
	- "Make foo do something" NOT "Made foo do something"
## **Other:**
### Ignoring Files: 
We can tell Git which files to ignore in a given repository, using a .gitignore file
- Userful for Secrets, API keys, credentials, log files, dependencies, packages, etc
  - `.filename`  ignores file names
  - `/directory` ignores everything in directory
  - `*.txt` ignores all files with this file type
- [gitignore.io](https://gitignore.io) can help you get started on creating a .gitignore file	
