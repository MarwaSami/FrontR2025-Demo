-	Git ? git hub?
-	Before version control ? issues ?
-	Type of version control
-	Short history of git 
-	Features of git 
o	Speed
o	Simple design
o	Support for non-linear development
o	Distributed
o	Scalable
-	Git Basics
o	Differnt than others (eg Subversion or Perforce) Snapshots Not Differences
Requirement for achieving this 
	Nearly Eveything is Local
	Git Has Integrity
	Git Generally Only Adds Data(simple folder ,simple file)
	The Three States
 

-	The Command Line (Cli vs GUI)
-	Installing Git
-	First-Time Git Setup
-	Configuration :Identity
-	 git config --global # User (global) -> ~/.gitconfig
-	 git config --system # System -> /etc/gitconfig
-	 git config  # Project -> /.git/conifg
-	Git Basics
•	Configure and initialize a repository
•	Begin and stop tracking files and stage and commit changes
•	Set up Git to ignore certain files and file patterns
•	Undo mistakes quickly and easily
•	Browse the history of your project
•	View changes between commits
•	Push and pull from remote repositories
 
-	Ignoring Files
Use .gitgnore file
Examples:
# a comment - this is ignored
*.a # no .a files
- Skipping the Staging Area
$ git commit -a -m "<msg>"

-	Removing Files
$ git rm <filename> # removes file from tracking and from filesystem
-	Undoing Things
o	Change the most recent Commit
	git commit --amend
o	Untracking tracked file
	git rm --cached <filename>
o	Unmodifying a Modified File
 git restore <filename>
                      Unstaging staged file
                          git restore --staged <filenmame> # recent command
                          git reset HEAD <filenmame> # old command but still works so far        
 Restore (revert) a committed change
This will revert everything committed in a specific commit. That's why it's better to have atomic commits
 git revert <commitrefs>
Deleted Files!
Deleted a file but not committed
git checkout HEAD <filename>
Deleted a file and committed
 git reset --hard HEAD~1
Working with Remotes
Showing Your Remotes
                           git clone https://github.com/schacon/ticgit
git remote
 git remote -v

Add a remote to an existing repo
git remote add [shortname] [url]
Fetching from Remote
fetches any new work that has been pushed to
that server since you cloned (or last fetched from) it**
git fetch [remote-name]

            
