# git

Github: Default structure of repo: main - main branch, develop - development branch<br>
Need to have contributions to develop branch only(this was created on github website from main)
<br>
To work on that, 
```
	1. Clone the github repo <repo-name> on local
	2. Use git checkout -b <local-branch-name> to create and switch to that branch in local
		Remember that this branch is made on local only.
	3. Add the remote origin repo using 
		git remote add <repo-name>
	4. Push the changes in the <local-branch-name> into the remote repo by
		git push origin -u <local-branch-name>
	5. We can see that a branch has been created on the repo on github website 
		of the name local-branch-name with our changes.
	6. We can ask for merging the changes into the develop branch through a pull request(PR).
		We can specify the title and description and create a pull request into the develop branch.
	7. The owner of the branch will review the changes and then merge the commit and/or delete the <local-branch-name> branch.
```
Generally cloning the repo brings only the main branch, to update the local repo with the changes committed in branch remote-branch-name:
```
	1. git checkout <local-branch-name> to switch to the local branch where updates needs to be pulled into
	2. Use git pull <repo-name> <remote-branch-name>
```

If we need to merge changes between 2 local git branches, say branch-2 into branch-1:
```
	1. git checkout <branch-1>
	2. git merge <branch-2>
```
The changes of branch-2 will be merged into the branch-1 branch. <br>
But branch-2 is not deleted here.
	
To delete local git branch:
```
	1. git branch -d <local-branch-name>,
```
only delete if the commits are merged or unchanged.
	
https://www.varonis.com/blog/git-branching#:~:text=To%20merge%20branches%20locally%2C%20use,branch%20into%20the%20main%20branch.	
