GITMAC - Git for Designers
---------

This tool aims to replace any sync/collaboration tool a designer use like DropBox or Box.com for a Git based one.

Use: 
It is assumed you have a working Git repository in your computer.

Be sure you have permission to write in your Git repository. Guide here: https://help.github.com/articles/error-permission-denied-publickey

Place gitmac in the root folder of your Git repository.

Run with ```./gitmac "Commit message" branch 1``` where "Commit message" is the message all the commits for this project will have, master is the branch of the Git repository and 1 is time between commits/syncs in minutes. Be extra sure you are in your root folder and not somewhere else when running ```./gitmac "Commit message" branch 1```.

To quit/stop ctrl + z in most consoles should work.

Enjoy seeing your files being synced with Git automatically.

Notes:
This can be used in multiple projects at the same time.

Issues:
If you get bash: ```./gitmac: Permission denied``` DO NOT run this as sudo but give your file the correct permissions. 
```chmod 700 gitmac``` or ```chmod 755 gitmac``` should fix the error.

As a nice gesture, please dont kill the program in the middle of a commit/sync or your files will be transmitted partially. Wait until the waiting message is in your console

If the branch is changed and it does not exist, an error will appear 

	error: src refspec newbranch does not match any.

	error: failed to push some refs to 'git@github.com:yourname/yourepo.git'. 

To prevent this, stop the script and do ```git checkout -b newbranch```

If you see 

	There is no tracking information for the current branch.
	Please specify which branch you want to merge with.
	See git-pull(1) for details

    git pull <remote> <branch>

	If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> newbranch

	On branch newbranch
	nothing to commit, working directory clean
do not freak out. It simply means you have not commited anything yet to the new branch and once you commit/push something, the error will go away.
