# Git Commands Cheat-sheet
This repo is my go to guide for git commands.
<br/><br/><br/><br/><br/><br/>





# Some more Common Terms

## Fork
A repo in A's gitHub ---> A's repo copy in my gitHub

## Clone
to save your repo in your local machine
- go to the directory where you want to save your repo
- `git clone https://github.com/{username}/{repo}.git`

## .gitignore file
This file contains list of files that we dont want to update to our remote repo (i.e. gitHub)
<br/><br/><br/><br/><br/><br/>






# General commands

## git status
to check the current status i.e. the current staging area location of your various files.

## git log --oneline
gives list of all the commits you made in the current branch you are in.

## git remote -v
displays current remote server URL
```
Fetch URL: /Users/alex/Documents/Presentations/githowto/auto/hello
Push  URL: /Users/alex/Documents/Presentations/githowto/auto/hello
```
<br/><br/><br/><br/><br/><br/>




# Transfering code from Local Repo to Remote Repo

## git init
to initialize a git repo for new or existing projects

## git add <file_name>
to add <file_name> to the staging area

## git add .
to add all files to the staging area

## git rm --cached <file_name>
to undo `git add` i.e. to remove file from staging area

## git commit -m "commit message"
this marks the check point of the branch, which means the snapshot of all your data is saved in the logs, which means you can get back to this position anytime at the development process.

## git commit -am "commit mssg"
If you want to add and commit in the same line

## Defining origin
This is to set the remote server URL, i.e. to which repo you want to push your code to.
```
git remote remove origin
git remote add origin https://github.com/{username}/{repo}.git
```

## git push -u origin <branch_name>
to push a particular branch to the repo which is defined in the origin.
<br/><br/><br/><br/><br/><br/>





# Transfering code from other's Remote Repo to my Local machine
```
NOTE: 
git pull = git fetch + git merge
```

## git pull
When many people are working on the same project. The project is undergoing constant changes. And to update your local repo, you pull data from the <branch_name> of the repo.

- Set the correct origin of the repo we need to update our code from
- Set the correct branch of the repo we need to update our code from
- `git pull`
<br/><br/><br/><br/><br/><br/>






# Branch Traversal

## git branch <new_branch_name>
to create a new branch with the name **'new_branch_name'**

## git checkout <branch_name>
to switch from one branch to another. The main branch is called master branch.

## **Merge side branch in the LOCAL REPOSITORY**

## git merge <branch_name>
to merge branch_name to current branch

## **Merge side branch to master branch in REMOTE REPOSITORY**

- Request the owner of the master branch to merge my code. This is called **pull request**.
  - compare and pull request >> Write a comment >> CREATE PULL REQUEST
  - (this step is for those who are having merge rights): Merge PR >> CONFIRM MERGE