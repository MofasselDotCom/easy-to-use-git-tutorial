#How to use git and github?

<p>Here all the steps and git bash code snippet are discussed shortly but I tried to set those step by step. I personally use these steps and those work for me effectively. Hope it will be help full for beginners.</p>

<h3>1. To set name and email address for a repo</h3>
	git config --global user.name "mofassel"
	git config --global user.email "mofassel.me@gmail.com"
	
<h3>1.1. To see current username and email info</h3>
	git config --list

<h3>2. To initiating git repo we need to create a directory where to set the local repo named gitrepo.git</h3>
	git init gitrepo.git

<h3>3. When we create a file in gitrepo.git folder then we need to add it before making commit</h3>
	git add . or git add filename
	

<h3>4. Shortcut for status, log and for speedy add+commit</h3>
	git commit -m "commit message here"
	git commit -a -m "commit message goes here" // it will directly add and commit. it must use with existing file that were commited before not very new file.

<h3>4.1. To delete/remove a commit to switch head to that commit.</h3>
<p>NB: all latest commit that were commited after reset commit will be deleted.</p>
	git reset --hard commit_id

<h3>5. We can see status or log message</h3>
	git status
	git status -s
	git log
	git log --oneline
	
<h3>6. We can see difference with old file when their is a change</h3>
	git diff //before adding it using git add command
	git diff --cached //when it is already added/staged

<h3>7 When our log message will be larger than terminal screen then their will be appeared a message named "end" at the bottom of the screen</h3>
	shift+zz //We need to press shift+zz to be get rid of from here.

<h3>8. To create and use ssh key follow this link</h3>
	https://help.github.com/articles/generating-ssh-keys

<h3>9. To add remote repo url and to reset remote url</h3>
	git remote add origin your-github-project-url
	git remote set-url origin your-new-github-project-url

<h3>10. To upload/push local repo to github repo.</h3>
	git push -u origin master

<h3>10.1. To force push a specific commit to remote repo</h3>
<p>NB: Sometime you may want to delete a specific commit from remote repo and change the head to its previous commit</p>
	git push origin +commit_id^:master

<h3>11. To download/pull remote repo into local repo folder (note: do pull before each push - recommended)</h3>
	git pull origin master

<h2>12. BRANCHIG IN GIT</h2>
<p>Branching is used to create individual environment for developing any new feature without creating any issue with master branch. While feature is ready then this branch can be be merged to master for production.</p>

<h3>12.1. To see existing branch and create new branch</h3>
	git branch
	git branch new_branch_name

<h3>12.2. To enter/switch into new branch</h3>
	git checkout new_branch_name


<h3>12.3. To create a new branch and immediately switch to that branch
	git checkout -b new_branch_name</h3>

<h3>12.4. To pull or push repo to its respective branch</h3>
	git pull origin branchname
	git push origin branchname

<h3>12.5. To make a clone of master branch repo to a new branch (needed for different PC). First checkout into that brach...</h3>
	git clone ssh-repo-url

<h3>12.6. To delete a local branch</h3>
	git branch -d branchName

<h3>12.7. To delete a remote branch</h3>
	git push origin :branchName

<h3>12.8. To import remote branch into local repo with same branch name like remote</h3>
	git fetch origin branchName:branchName

<h3>12.9. To merge branch repo with master repo (checkout into master first, need to make additional commit to see changes in master after merge command)</h3>
	git merge origin branchName

<h2>13. TAGGING AND RELEASING A REPO IN GIT</h2>
<p>Tag is used to create version of the repo and it helps ot release that version while it is ready to release.</p> 

<h3>13.1. To create a tag (verision info) Example: tagname-v1.0</h3>
	git tag tagname

<h3>13.2. To push a tag to github to release that version to github</h3>
	git push origin tagname

<h3>13.3. To create branch from a specific tagname to edit a tag</h3>
	git checkout -b newbranch tagname

<h3>13.4. To delete a local tag</h3>
	git tag -d tagname

<h3>13.5. To delete a remote tag</h3>
	git push --delete origin tagname
	git push origin :tagname

	
<p>I collected and gathered all the codes above to use easily from one place. If anyone wants to update some codes or snippets he/she is most welcome</p>
