# Saving Changes
### Git Add
	git add <file>
	git add <dir>
	git add . 
		-> Add current dir
### Git Commit
	git commit
	git commit -a 
		-> Snapshot all change in working dir
# Inspecting a repository
	git log
	git log -n <limit>
		-> Show log of limit the number of commits
		
	git log --oneline
	git log --stat 
		-> Show history with which files were added or altered
		
	git log -p 
		-> Show full diff of each commit
		
	git log --author="<pattern>"
	
	git log --grep="<pattern">
		-> Search commits by message
		
	git log <since>...<until> 
		-> Search commits in range
		
	git log <file>
		-> Show changed history of file
		
	git log --graph --decorate --oneline 
		-> Show history with commit ID and message in column format
		
# Git Stash
### Stashing your work
	git stash
		-> Temporary save current working
		
	git stash -u
		-> Stash untracked file (file has not been added)
		
	git stash save <message>
		-> Annotate your stash with a description
		
	git stash list
		-> List out all available stashes
		
### Re-apply your stashed changes
	git stash pop
		-> Removes the changes from your stash and reapplies them to your working copy
		
	git stash apply
		-> Reapply the changes to your working copy and keep them in your stash
	
	git stash pop <stash version>
		-> Reapply specific stash
		
	git stash -p
		-> Iterate through each changed “hunk” and ask whether you wish to stash it
		
	git stash branch <new branch>
		-> Create new branch from you stash
		
### Viewing stash diff
	git stash show
		-> View a summary of a stash
		
	git stash show -p
		-> View full diff of a stash
		
### Cleaning up your stash
	git stash drop <stash id>
		-> Delete all stash

# Viewing old commits
	git checkout -b <new-branch>
	
	git checkout master
		-> Return to the master branch
		
	git checkout <commit> <file>
		-> Check out a previous version of a file. <file> will be added into staging area.
		-> Remember, unlike checking out a commit, this does affect the current state
		of your project. The old file revision will show up as a “Change to be committed,”
		giving you the opportunity to revert back to the previous version of the file.
		
	git checkout <commit>
		-> Update all files in the working directory to match the specified commit.
		This will put you in a detached HEAD state.
		
	git checkout HEAD <file>
		-> Check out the most recent version of file if don’t want to keep the
		old version after execute git checkout <commit> <file>.
		
# Undoing Changes
### Using git checkout
	
### Using git revert
	git revert <commit>
		-> Generate a new commit that undoes all of the changes introduced in <commit>,
		then apply it to the current branch.
	
	git revert HEAD
		-> Revert the commit we just created.
		
### Using git reset
	
		
	