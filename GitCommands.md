# Saving Changes
	git add <file>
	git add <dir>
	git add . 
Add current dir

	git commit
	git commit -a 
		-> Snapshot all change in working dir

# Inspecting a repository
	git log
	git log -n <limit>
		-> show log of limit the number of commits
		
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

# Viewing old commit
	git checkout -b <new-branch>
	
	git checkout master
		-> Return to the master branch
		
	git checkout <commit> <file>
		-> Check out a previous version of a file. <file> will be added into staging area.
		
	git checkout <commit>
		-> Update all files in the working directory to match the specified commit. This will put you in a detached HEAD state.
		
	