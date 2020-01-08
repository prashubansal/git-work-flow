# This is my first line 

No one ever reads the readme file 
--------
How to create git repo, create your 'README.md' file and get track of it
---------

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

check 'git status' again:
	#it shows you that a new file is coming up, because it hasn't been saved in the git.

	#That green area shows you what's going to happen when you make a commit

git commit -m 'created our first README'
	#Now you saved the changes to the local repo

git log
	#to checkout your commits


#Now make some changes in your 'README.md' file

git status
	#it tell you that file has been modified

git add
	#add the modified file to git

git commit -m 'notes on git work flow'


