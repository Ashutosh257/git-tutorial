
# GIT 


## How can I remove unwanted files?

Git can help you clean up files that you have told it you don't want.
The command `git clean -n` will show you a list of files that are in the repository, but whose history Git is not currently tracking. 
A similar command `git clean -f` will then delete those files.

Use this command carefully: git clean only works on untracked files, so by definition, their history has not been saved.
If you delete them with git clean -f, they're gone for good.


## How can I undo changes to staged files?
At the start of this chapter you saw that git reset will unstage files that you previously staged using git add. By combining git reset with git checkout, you can undo changes to a file that you staged changes to. The syntax is as follows.


> git reset HEAD path/to/file

> git checkout -- path/to/file


(You may be wondering why there are two commands for re-setting changes. The answer is that unstaging a file and undoing changes are both special cases of more powerful Git operations that you have not yet seen.)