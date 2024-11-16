# part 1: introduction to version control and git
## Task1: Install and configure git 
#### 1.Configure Git with your username and email
```

 git config --global user.name "user Name"

 git config --global user.email "your-email@example.com"
```
  shows the globally configured user name and email, along with any other global settings  defined.
 

 #### 2.View your Git configuration:
 ```
  git config --list
 ```
 view all active Git configuration settings

## Task 2: Initialize a Repository
 #### 1.Create a new project folder and navigate to it:
 ```
 mkdir MyProject
 
create a folder

### cd myproject
current working directory.
```
#### 2.Initialize it as a Git repository
```
  git init 
  ```
  The command git init is used to initialize a new Git repository




## Task 3: Create a File and Make Multiple Commits
#### 1.create a new file and add content
git commit -m "intial commit :added README.md
```
echo "My First Project" > README.md
```
The command echo "My First Project" > README.md is used to create a new file named README.md and write the text "My First Project" into that file


#### 2.Stage the file:
```
git add README.md
```
The command git add README.md is used to stage the README.md file for the next commit in your Git repository

#### 3.Commit the file
```
git commit -m "Initial commit: Added README.md"
```
 Added " README.md " is used to create a new commit in your Git repository with a message describing the changes made.
#### 4.Make changes to the file
```
echo "Added a description" >> README.md
```
"Added a description" to the end of the README.md file
#### 5.Stage and commit the changes
```
git add README.md
git commit -m "Updated README with a description"
```
"Added a description" to the end of the README.md file.

## Task 4: Check Status and Log
#### 1.Check the repository’s current status
```
git status
```
The command git status is used in Git to display the current state of your working directory and staging area.

#### 2.View commit history in detail
```
git log --oneline --graph --decorate
```
The command git log --oneline --graph --decorate is a way to visualize the commit history of a Git repositor

Example Output:
```
* 2f8d6a2 (HEAD -> main) Updated README with a description
* d3c4b21 Initial commit: Added README.md
```
#### 2.View your Git configuration
```
git config --list
```
The command git config --list is used in Git to display all the configuration settings that are currently set for your Git environment

## Task 5: Create and Clone a Repository
#### 1. Create a repository on GitHub named example-repo.

#### 2. Clone it locally
```
git clone http://codinggita.com/example-repo
```
 clone repository you created on GitHub to your local machine

## Task 6: Understanding the git Working directory
example Workflow

i. Make change to a file in the working directory
```
echo "Workflow example" > workflow.md
```
it is the used to create a new file named workflow.md and write the text "Workflow example" into that file

ii.stage the file
```
git add workflow.md 
```
add the file 

iii. commit the file to the repository.
```
git commit -m "Added workflow example"
```
 is used to create a commit in your Git repository with a message describing the changes you made

# part 2: Working with Repositories
## Task 7:Branching and Merging
#### 1. create a new branch for a feature 
```
git branch feature-login
git checkout feature -login
```
 git branch feature-login and switch to that branch in your Git repository.
git checkout feature-login are used to create a new branch named.

or.use:
```
git checout -b feature -login
```
The correct command to create and switch to a new branch in Git

#### 2. Add a new file and commit change
```
echo "login page" > login.html
git add login .html
git commit -m "added login page"
```
echo "login page" > login.html  This command creates a new file named

git add login.html  add the file 

git commit -m "added login page" This creates a new commit with the staged changes and includes the message


#### 3.Merge the feature branch into main
``` 
git checkout main 
git merge feature-login
```
switch to the main branch and then merge changes from the feature-login branch into main

## Task 8: Handling merge conflicts
#### 1. create to branch:
```
git branch branch -A
git branch branch -B
```
This command creates a new branch named branch-A

This command creates a new branch named branch-B

#### 2.Modify the same line in README.md in both branches.
To modify the same line in the README.md file in both branch-A and branch-B

#### 3.merge branch-A into main:
```
git checkout main
git merge branch-A
```
git checkout main command it is used to switch branch 

git merge branch-A: This command merges the changes from branch-A 

#### 4.Attempt to merge branch -B into main (this will cause  conflict):
```
git merge branch-B
```
merge the branch-B

#### 5. Resolve the conflict manually in README.md , then;
```
git add README.md
git commit -m "resolved merge conflict brtween branch -A and branch -B"
```
add the file README.md

commit a message "resolved merge conflict between branch -A and branch -B

## Task 9:Renaming and deleting Branches
#### 1.Rename a branch 
```
git branch -m old-branch-name new-branch-name
```
The command you provided is used to rename a Git branch

#### 2.Delete a branch:
```
git branch -d feature-login
```

# part 3: Advanced git Operation 
## Task 10: Using git stash
#### 1.Make change to a file but don`t commit:
```
echo "temporary work" >> temp.md
```
