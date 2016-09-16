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
	
### Re-apply your stashed changes
	git stash pop
		-> Removes the changes from your stash and reapplies them to your working copy
		
	git stash apply
		-> Reapply the changes to your working copy and keep them in your stash
	

# Viewing old commits
	git checkout -b <new-branch>
	
	git checkout master
		-> Return to the master branch
		
	git checkout <commit> <file>
		-> Check out a previous version of a file. <file> will be added into staging area.
		
	git checkout <commit>
		-> Update all files in the working directory to match the specified commit. This will put you in a detached HEAD state.
		
	git checkout HEAD <file>
		-> Check out the most recent version of file if don’t want to keep the old version after execute git checkout <commit> <file>.
		
# Undoing Changes
		
	