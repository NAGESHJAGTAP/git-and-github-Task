
# Part 1: Creating and Cloning Repositories

## Task 1: Create a Local Git Repository
```
mkdir MyProject
```
  * Creates a new project directory.
```
cd MyProject
```  
 * Navigates into the project directory.
```
git init 
```  
  * Initializes the folder as a Git repository by creating a `.git` directory.
```
git status
```  
 * Displays the current status of the repository, including staged and unstaged changes.

## Task 2: Clone a Remote Repository
```
git clone https://github.com/username/repo.git
``` 
 * Clones a remote repository to your local machine.
```
cd repo
```
  * Changes to the cloned repository directory.
``` 
ls -a
``` 
 * Lists all files, including hidden ones like `.git`.

---

## Part 2: Understanding Commits and Commit Messages

### Task 3: Commit Changes Locally
```
echo "Welcome to Git" > README.md
``` 
 * Creates a new file with the specified content.
```
git add README.md
```  
  * Stages the file, preparing it for the next commit.
```
git commit -m "Initial commit: Added README.md"
```  
 * Commits the staged changes with a descriptive message.

### Task 4: Write Effective Commit Messages
```
git commit -m "Added initial version of README.md with project overview"
``` 
  * Creates a clear and concise commit message in the imperative mood.
```
git add .
```  
  * Stages all changes in the current directory.
```
git commit -m "Added two new files for feature setup"
```  
 * Commits all staged changes with a single message.

---

## Part 3: Viewing Commit History with `git log`

### Task 5: View Detailed Commit History
```
git log
```
  * Displays detailed commit history with hash, author, date, and message.
``` 
git log --oneline
```  
*  Shows a compact, one-line summary of commit history.

### Task 6: Customize Log Outputs
```
git log --oneline --graph --decorate
``` 
 * Displays commits in a graphical format with branch decorations.
```
git log README.md
``` 
 * Filters the log to show history related to the specified file.

---

## Part 4: Understanding Branching and Merging

### Task 7: Understanding Branching
``` 
git branch
```  
 * Lists all branches and highlights the current branch.
```
git branch feature-branch
```  
  * Creates a new branch without switching to it.
 ```git checkout feature-branch
 ```  
  * Switches to the specified branch.
    ```
    git checkout -b feature-branch
    ```  
  * Creates and switches to a new branch in one step.

---

## Part 5: Creating and Working with Branches

### Task 8: Make Changes in a Branch
```
echo "Feature in progress" > feature.txt
```  
  * Creates or modifies a file with the specified content.
```
git add feature.txt
```  
  * Stages the file for commit.

```
git commit -m "Added feature.txt in feature-branch"
```  
 * Commits the changes in the current branch.

### Task 9: Merging Branches
```
git checkout main
```  
 * Switches back to the `main` branch.
```
git merge feature-branch
```  
 * Integrates changes from `feature-branch` into `main`.

---

## Part 6: Resolving Merge Conflicts

### Task 10: Simulate a Merge Conflict
```
echo "Main branch content" > conflict.txt
```  
 * Adds or modifies content in `main` branch.
```
git add conflict.txt
```  
 * Stages the change.
```git commit -m "Added conflict.txt in main branch"
```  
 * Commits the staged file in the `main` branch.
```
git checkout feature-branch
```  
 * Switches to the `feature-branch`.
```
echo "Feature branch content" > conflict.txt
```  
 * Modifies the same file, creating conflicting content.
```
git add conflict.txt
```  
  * Stages the conflicting change.
```
git commit -m "Modified conflict.txt in feature-branch"
```  
 * Commits the conflicting changes in the branch.
```
git checkout main
```  
 * Switches back to the `main` branch.
```git merge feature-branch
```  
 * Attempts to merge changes, causing a conflict.
```git add conflict.txt
```  
 * Stages the resolved file after manually editing it.
```
git commit -m "Resolved conflict in conflict.txt"
```  
 * Commits the merge resolution.

---

## Part 7: Deleting and Renaming Branches

### Task 11: Delete a Branch
```
git branch -d feature-branch
```  
 * Deletes the branch only if it has been fully merged.
```
git branch -D feature-branch
```  
 * Force-deletes the branch regardless of merge status.

### Task 12: Rename a Branch
```
git branch -m new-branch-name
```  
 * Renames the current branch to the specified name.
```
git branch -m old-branch-name new-branch-name
```  
 * Renames another branch that is not checked out.

---
# Consolidated Flow Summary

#### 1.Start by creating and cloning repositories.
#### 2. Learn to commit changes effectively with clear messages.
#### 3.Exploe commit history using various git log commands.
#### 4.Understand branching and practice creating, switching, and merging branches.
#### 5.Dive into resolving merge conflicts.
#### 6.End by managing branches through deletion and renaming.
