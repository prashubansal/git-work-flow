# This is my first line 

No one ever reads the readme file 
-----------------------------------------------------
#How to create git repo, create your 'README.md' file and get track of it
------------------------------------------------------

git config --global user.name 'author_name'
git config --global user.email 'author_email'

mkdir git-work-flow
cd git-work-flow

subl .
create the 'README.md' file

git init . #initialize git in my working directory/repository
git status
	#tell me there is a untrack file 'README.md' because by default git doesn't jtrack every file that you have in repo
git add 'README.md'  
	#manually add the file in the git for it to track

git status
	#it shows you that a new file is coming up, because it hasn't been saved in the git.

	#That green area shows you what's going to happen when you make a commit

git commit -m 'created our first README'
	#Now you saved the changes to the local git repo

git log
	#to checkout your commits

------------------------------------------------------
#how to save our changes of repo into git using commit?
----------------------------------------------------

#make some changes in the 'README' file and save it

git status
	#it tell you that file has been modified because it is keeping track of your file

git add
	#add the modified file to git for telling git which changes to include in the 'git commit' command 

git commit -m 'notes on git work flow'
	#save the changes in your local git repo

------------------------------------------------------
#What is branch and How to work with them or use them?
-----------------------------------------------------

-> Branch: copy/duplicate of your repo to work knowing that your original repo is saved in master branch.	

git branch develop
	#creates a branch develop

git branch
	#show all the branch

git checkout develop
	#switch to 'develop' branch

#make some changes in the 'README' file
->Now we are on develop branch 

git status
	
git commit -am ''
	a - add
	
git checkout -b feature/new-feature
	it creates 'feature/new-feature' branch and switch to that branch.

------------------------------------------------------
#How to merge the branches?
------------------------------------------------------
git merge feature/new-feature
	#merges the 'feature' branch in to the 'develop' branch

------------------------------------------------------
#What is git-flow
----------------------------------------------------
->git-flow: helpful in using the git by conventional way

apt install git-flow

#initialize the git flow on specific repo
git flow init -d 
	d - use default settings of git flow

git flow feature finish new-feature
	#merge the 'feature' branch in your current working branch and remove 'feature' branch

------------------------------------------------------
#git flow feature branch and pushing to gihub
------------------------------------------------------

git flow feature start a-new-feature
	#creates a new branch(a-new-feature) and prefix it with feature

#Now you can create a new file in 'feature/a-new-feature' branch and it doesn't mess with develop branch 

git status
	#tells you that you have a new file to add in this branch

git add -A
	
git commit -am 'new file added'

-----------------------------------------------------
#Now we are going to publish our repo in github
---------------------------------------------------

			create a new repo
					|
			write a repo_name
					|
			click create repo
					|
			copy the git-link

git remote add origin <git-link>
	#creates a repo/cloud-storage on github

git remote -v 
	#list out the origin that i just added

git checkout master

git push origin master
	#push master branch up into our repo into github/allows us to share our work in public.