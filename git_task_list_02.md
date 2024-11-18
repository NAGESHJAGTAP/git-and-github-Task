# Part 1: Git Basics
## Task 1: Install and Configure Git
#### 1.Install Git from git-scm.com.
#### 2.Configure your global Git settings:
```
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```
* The commands you provided are used to configure your Git user information globally on your machine

#### 3.Verify the configuration
```
git config --list
```

* The command git config --list is used to display the current configuration settings for Git.

## Task 2: Initialize a Repository
#### 1. Create a directory and initialize it as a Git repository
```
mkdir MyProject
```
* create a new folder
```
cd MyProject
```
* The command cd MyProject is used to change the current directory to a directory named MyProject
```
git init
```
* initialization the the git repository

` Purpose: Initializes a .git folder to track changes `

# Part 2: Basic Workflow
## Task 3: Creating and Committing Files
#### Create a file:
```
echo "Hello Git" > file1.txt
```
* create a file git repository "file1.txt"

#### 2.Stage and commit the file:
```
git add file1.txt
```
* add the file git repository "file1.txt"
```
git commit -m "Initial commit: Added file1.txt"
```
* recored the change made the file

## Task 4: Viewing Changes
#### 1.Modify the file:
```
echo "Git is awesome!" >> file1.txt
```
The command echo "Git is awesome!" >> file1.txt is used to append the text "Git is awesome!" to the existing contents of the file named file1.txt(modify the file)

#### 2.Check file status and differences
```
git status
``` 
*    
```
git diff
```
* compair to the staging aria to working directory.

## Task 5: Undoing Changes
#### 1.Unstage a staged file:
```
git reset file1.txt
```
* reset the file 
* The command git reset file1.txt is used in Git to unstage a file, effectively removing it from the staging area (also known as the index) while keeping the changes in your working directory.

#### 2.Discard uncommitted changes:
```
git checkout -- file1.txt
```
* The command git checkout -- file1.txt is used in Git to discard changes made to a specific file in your working director


# Part 3: Branching and Merging
## Task 6: Branch Management
#### 1.Create a branch and switch to it:
```
git checkout -b feature-branch
```
* The command git checkout -b feature-branch is used in Git to create a new branch and immediately switch to that branch. 

## Task 7: Merging Branches
#### 1.Merge feature-enhanced into main
```
git checkout main
```
* The command git checkout main is used in Git to switch your current working branch to the main branch.
```
git merge feature-enhanced
```
*  The command git merge feature-enhanced is used in Git to merge the changes from the branch named feature-enhanced into the current branch you are on

## Task 8: Handling Merge Conflicts
#### 1.Create two conflicting branches and resolve a conflict manually
```
git merge <branch-name>
```
* The merge command is used to combine the histories of two branches.

#### 2.Use
```
git add <resolved-file>
```
* git add <resolved-file> is used to stage changes to files in your working directory, particularly after resolving conflicts.
```
git commit
```
* git commit is used to create a new commit with the staged changes, capturing the current state of the project along with a descriptive message.

# Part 4: Remote Repositories
## Task 9: Remote Setup
#### 1.Add a remote repository:
```
git remote add origin https://github.com/your-username/repo.git
```
* The command git remote add origin https://github.com/your-username/repo.git is used in Git to create a new remote repository reference named origin

#### 4.Verify the remote:
```
git remote -v
```
* The command git remote -v is used to display the remote repositories associated with your local Git repository,

## Task 10: Push and Pull
#### Push changes to the remote repository:
```
git push -u origin main
```
* The command git push -u origin main is used in Git to push your local changes to a remote repository

#### 2.Pull changes from the remote:
```
git pull origin main
```
* git-pull - Fetch from and integrate with another repository or a local branch

## Task 11: Cloning a Repository
#### 1.Clone a remote repository:
```
git clone https://github.com/your-username/repo.git
```
* git clone command used to create a local copy of a Git repository hosted on GitHub.

# Part 5: Advanced Git
## Task 12: Stashing Changes
#### 1.Save uncommitted changes
```
git stash
```
* The git stash command is a powerful feature in Git that allows you to temporarily save changes that you have made to your working directory without committing them

#### 2.Apply stashed changes:
```
git stash apply
```
* The git stash apply command is used in Git to reapply changes that you have previously stashed away.

#### 3.Drop the stash
```
git stash drop
```
* This is the basic form of the command. It removes a specific stash entry from the stash list


## Task 13: Tagging Commits
#### 1.Create and annotate a tag:
```
git tag -a v1.0 -m "Version 1.0 release"
```
*  Tags are often used to mark specific points in repository's history, such as releases or significant milestones.

#### 2.Push the tag to the remote:
```
git push origin v1.0
```
* The command git push -u origin main is used in Git to push your local changes to a remote repository

## Task 14: Rewriting Commit History
#### 1.Use interactive rebase to modify commit messages:
```
git rebase -i HEAD~3
```
* The git rebase command is a powerful feature in Git that allows you to integrate changes from one branch into another.

## Task 15: Cherry-Picking Commits
#### 1.Apply a specific commit to another branch:
```
git cherry-pick <commit-hash>
```
* The git cherry-pick command is used to apply the changes introduced by a specific commit from one branch to another branch in Git.

# Part 6: Collaboration
## Task 16: Forking and Pull Requests
#### 1. Fork a repository and clone it locally:
```
git clone https://github.com/your-username/forked-repo.git
```
*  git clone command used to create a local copy of a Git repository hosted on GitHub.

#### 2.Make changes and push them:
```
git checkout -b fix-typo
```
* This command creates a new branch named fix-typo and switches to it immediately. 

```
echo "Typo fixed" >> README.md

```
* add the file README.md

```
git commit -m "Fixed a typo"

```
* commit the messge "fixed a typo"
```
git push origin fix-typo
```
* git push: This is the Git command used to upload local repository content to a remote repository. 


#### 3.Open a pull request on GitHub.

## Task 17: Simulating Team Collaboration
#### 1.Simulate a conflict by having two users modify the same file.
#### 2.Practice resolving the conflict as a team.


# Part 7: Ignoring Files
## Task 18: Using .gitignore
#### 1.Create a .gitignore file:
```
echo "node_modules/" > .gitignore
```
* create a file ".gitingnore"
```
git add .gitignore
```
* add the file ".gitingnore"
```
git commit -m "Added .gitignore"
``` 
* git commit a message 

#### 2.Verify that ignored files are not staged:
```
git status
```
* To check the status of the files 

# Part 8: Automation and Cleanup
## Task 19: Cleaning the Repository
#### 1.Remove untracked files:
```
git clean -f
```
* The command git clean -f is used in Git to remove untracked files from your working directory

## Task 20: Aliases and Shortcuts
#### 1.Create an alias for frequently used commands:
```
git config --global alias.st status
git config --global alias.cm commit
```

#### 2. Use the alias:
```
git st
git cm -m "Message"
```


