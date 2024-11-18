# part 1: introduction to version control and git
## Task1: Install and configure git 
#### 1.Configure Git with your username and email
```

 git config --global user.name "user Name"

 git config --global user.email "your-email@example.com"
```
* shows the globally configured user name and email, along with any other global settings  defined.
 

 #### 2.View your Git configuration:
 ```
  git config --list
 ```
* view all active Git configuration settings

## Task 2: Initialize a Repository
 #### 1.Create a new project folder and navigate to it:
 ```
  mkdir MyProject
 create a folder

 cd myproject
current working directory.
```
#### 2.Initialize it as a Git repository
```
  git init 
  ```
 * The command git init is used to initialize a new Git repository




## Task 3: Create a File and Make Multiple Commits
#### 1.create a new file and add content
git commit -m "intial commit :added README.md
```
echo "My First Project" > README.md
```
* The command echo "My First Project" > README.md is used to create a new file named README.md and write the text "My First Project" into that file


#### 2.Stage the file:
```
git add README.md
```
* The command git add README.md is used to stage the README.md file for the next commit in your Git repository

#### 3.Commit the file
```
git commit -m "Initial commit: Added README.md"
```
 * Added " README.md " is used to create a new commit in your Git repository with a message describing the changes made.
#### 4.Make changes to the file
```
echo "Added a description" >> README.md
```
* "Added a description" to the end of the README.md file
#### 5.Stage and commit the changes
```
git add README.md
git commit -m "Updated README with a description"
```
* "Added a description" to the end of the README.md file.

## Task 4: Check Status and Log
#### 1.Check the repository’s current status
```
git status
```
* The command git status is used in Git to display the current state of your working directory and staging area.

#### 2.View commit history in detail
```
git log --oneline --graph --decorate
```
* The command git log --oneline --graph --decorate is a way to visualize the commit history of a Git repositor

Example Output:
```
* 2f8d6a2 (HEAD -> main) Updated README with a description
* d3c4b21 Initial commit: Added README.md
```
#### 2.View your Git configuration
```
git config --list
```
* The command git config --list is used in Git to display all the configuration settings that are currently set for your Git environment

## Task 5: Create and Clone a Repository
#### 1. Create a repository on GitHub named example-repo.

#### 2. Clone it locally
```
git clone http://codinggita.com/example-repo
```
* clone repository you created on GitHub to your local machine

## Task 6: Understanding the git Working directory
example Workflow

i. Make change to a file in the working directory
```
echo "Workflow example" > workflow.md
```
* it is the used to create a new file named workflow.md and write the text "Workflow example" into that file

ii.stage the file
```
git add workflow.md 
```
* add the file 

iii. commit the file to the repository.
```
git commit -m "Added workflow example"
```
* is used to create a commit in your Git repository with a message describing the changes you made

# part 2: Working with Repositories
## Task 7:Branching and Merging
#### 1. create a new branch for a feature 
```
git branch feature-login
git checkout feature -login
```
* git branch feature-login and switch to that branch in your Git repository.
git checkout feature-login are used to create a new branch named.

or.use:
```
git checout -b feature -login
```
* The correct command to create and switch to a new branch in Git

#### 2. Add a new file and commit change
```
echo "login page" > login.html
git add login .html
git commit -m "added login page"
```
* echo "login page" > login.html  This command creates a new file named* 
* git add login.html  add the file 
* git commit -m "added login page" This creates a new commit with the staged changes and includes the message


#### 3.Merge the feature branch into main
``` 
git checkout main 
git merge feature-login
```
* switch to the main branch and then merge changes from the feature-login branch into main

## Task 8: Handling merge conflicts
#### 1. create to branch:
```
git branch branch -A
git branch branch -B
```
* This command creates a new branch named branch-A
* This command creates a new branch named branch-B

#### 2.Modify the same line in README.md in both branches.
To modify the same line in the README.md file in both branch-A and branch-B

#### 3.merge branch-A into main:
```
git checkout main
git merge branch-A
```
* git checkout main command it is used to switch branch 
* git merge branch-A: This command merges the changes from branch-A 

#### 4.Attempt to merge branch -B into main (this will cause  conflict):
```
git merge branch-B
```
* merge the branch-B

#### 5. Resolve the conflict manually in README.md , then;
```
git add README.md
git commit -m "resolved merge conflict brtween branch -A and branch -B"
```
* add the file README.md
* commit a message "resolved merge conflict between branch -A and branch -B

## Task 9:Renaming and deleting Branches
#### 1.Rename a branch 
```
git branch -m old-branch-name new-branch-name
```
* The command you provided is used to rename a Git branch

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
#### 2.stash the change:
```
git stash
```
* The git stash command is a powerful feature in Git that allows you to temporarily save changes that you have made to your working directory without committing them

#### 3.View stashed changes:
```
git stash list
```
* The git stash list command is used to display a list of all the stashes that you have saved in your Git repository

#### 4.Apply the stashed changes:
```
git stash apply
```
* The git stash apply command is used in Git to reapply changes that you have previously stashed away.

#### 5.Drop the stash after applying:
```
git stash drop
```
* This is the basic form of the command. It removes a specific stash entry from the stash list

## Task 11: Rewriting History with Interactive Rebase

#### 1.Create multiple commits:
```
echo "Commit 1" > file1.txt && git add file1.txt && git commit -m "Commit 1"
echo "Commit 2" > file2.txt && git add file2.txt && git commit -m "Commit 2"
echo "Commit 3" > file3.txt && git add file3.txt && git commit -m "Commit 3"
```

* The commands you've provided are a series of shell commands that create three text files, add them to a Git repository
* Use of &&: The && operator ensures that the next command runs only if the previous command succeeded

#### 2.Squash commits into one:
```
git rebase -i HEAD~3
```
* This command is used to reapply commits on top of another base tip. In the context of -i, it allows you to modify commits in various ways.

#### Example: Replace pick with squash for the second and third commits.
* Sure! Let's go through a detailed example of how to replace pick with squash for the second and third commits using Git's interactive rebase feature

## Task 12: Cherry-Picking Commits
#### 1.Create a new branch:
```
git checkout -b cherry-pick-example
```
* The command git checkout -b cherry-pick-example is used to create a new branch in Git and switch to it at the same time. 

#### 2. Cherry-pick a specific commit from another branch:
```
git cherry-pick <commit-hash>
```
* The command git cherry-pick <commit-hash> is used in Git to apply the changes introduced by a specific commit from one branch to another

## Task 13: Tagging Commits
#### 1.Tag the current commit:
```
git tag -a v1.0 -m "Version 1.0 release"
```
* The command git tag -a v1.0 -m "Version 1.0 release" is used in Git to create an annotated tag. Tags are often used to mark specific points in your repository's history, such as releases or significant milestones.

#### 2.Push the tag to the remote repository
```
git push origin v1.0
```
The command git push origin v1.0 is used in Git to push a specific tag (in this case, v1.0) from your local repository to a remote repository

## Task 14: Working with Remote Repositories
#### 1.Add a remote repository:
```
git remote add origin <repository-url>
```
* The command git remote add origin <repository-url> is used in Git to add a remote repository to your local Git configuration 

#### 2. Push your changes to the remote repository:
```
git push origin main
```
* This is the command used to upload local repository content to a remote repository. It updates the remote branch with the commits from your local branch.

## Task 15: Forking and Contributing
#### 1.Fork a repository on GitHub.
#### 2.Clone the fork locally:
```
git clone <forked-repo-url>
```
* The command git clone <forked-repo-url> is used in Git to create a local copy of a remote repository that has been forked from another repository

#### 3.Create a new branch, make changes, and push:
```
git checkout -b fix-typo
```
* git checkout -b fix-typo: This command creates a new branch called fix-typo and switches to it immediately.
```
echo "Typo fixed" >> README.md
```
* echo "Typo fixed" >> README.md: This command appends the text "Typo fixed" to the end of the README.md file
```
git add README.md
```
* git add README.md: This command stages the changes made to README.md for the next commit.
```
git commit -m "Fixed a typo"
```
* This command creates a new commit with the staged changes and includes a commit message describing what was done. The -m flag allows you to provide the commit message inline.
```
git push origin fix-typo
```
* git push origin fix-typo: This command pushes the fix-typo branch to the remote repository named origin

#### 4.Open a pull request on GitHub.
## Task 16: Simulate Team Collaboration
#### 1.Create a repository and share it with a friend.
#### 2.Both make changes to the same file simultaneously.
#### 3.Practice resolving merge conflicts and pushing changes.

## Task 17: Git Ignore
#### 1.Create a .gitignore file
```
echo "node_modules/" > .gitignore
```
* file is used to specify files and directories that should be ignored by Git

#### 2.Add files and ensure ignored files are not staged
```
git add .
```
* When you run the command git add ., Git will stage all changes in the current directory, including new files