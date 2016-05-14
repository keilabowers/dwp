Portfolio Production Server Deployment Plan
======

Server and Local Setup
------

###Production Server Settings:
	* DigitalOcean Droplet (Size: 512MB)
	* OS: Ubuntu 12.04.5 x64
	* Web Server: Apache2
	* Version Control System: GIT


Creating and Updating Production Server Files
------

###Changing the Files

	1.	Get recent copy of master branch from Production Server
			```git checkout master```

	2.	Create a new branch to make local changes on
			```git branch newBranchName
			git checkout newBranchName```

	3.	Save changes
			```git add -A
			git commit -m "Comment Explaining Commit"```

###Ready to send to the Production Server

	1.	Merge the local changes with the MASTER branch
			```git checkout master
			git merge newBranchName```
		In the event of a conflict, resolve conflict and retry

	2.	Send the changes to the Production Server and Github Repo
			```git push prodServer		<-- Alias for Production Server
			git push github 		<-- Alias for Github Repo```




