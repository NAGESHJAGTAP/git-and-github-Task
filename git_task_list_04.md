# Task List: Focused on Advanced Git Operations

# Part 1: Understanding and Using `git stash`

## Task 1: Save Changes Temporarily with `git stash`

#### 1.Make changes to a file without committing:
```
echo "Temporary changes" >> temp-file.txt
```  
 * Adds temporary content to a file.
 #### 2.View the status of changes:


```
git status
```  
 * Displays the status of unstaged changes.
 #### 3.Stash the changes:


```
git stash
```  
  * Saves changes to a stash and reverts the working directory to the last commit.
  #### 4.View the stashed changes:


```
git stash list
```  
 * Shows a list of stashed changes.

## Task 2: Apply and Drop Stashed Changes
#### 1.Apply the most recent stash:


``` 
git stash apply
```  
 * Applies the most recent stash without removing it.
 #### 2.Drop the most recent stash after applying it:


``` 
git stash drop
```  
 * Deletes the most recent stash.
 #### 3.Alternatively, to apply a specific stash:


```
git stash apply stash@{1}
```  
 * Applies a specific stash by its identifier.

### Task 3: Stash Untracked Files
#### 1.Stash changes, including untracked files:

```
git stash -u
```  
*  Stashes both tracked and untracked files.
#### 2.Apply stashed changes including untracked files:

```
git stash apply
```  
 * Applies the stashed changes, including untracked files.

---

# Part 2: Rewriting History with `git rebase`

## Task 4: Rebase Commits to a New Base
#### 1.Rebase the current branch onto main:


```
git rebase main
```  
 * Re-applies commits from the current branch on top of `main`.
 #### 2.Resolve any conflicts that may arise during rebase, and continue:


```
git rebase --continue
```  
 * Resolves conflicts and continues the rebase.

## Task 5: Canceling a Rebase
#### 1.If a rebase goes wrong, abort it:

```
git rebase --abort
```  
  * Aborts the rebase and restores the branch to its original state.

---

# Part 3: Interactive Rebase (`git rebase -i`)

## Task 6: Use Interactive Rebase to Modify Commit History
#### 1.View the last few commits:


```
git log --oneline
```  
 * Displays a compact view of the commit history.
 #### 2.Start an interactive rebase for the last 3 commits:


```
git rebase -i HEAD~3
```  
  * Starts an interactive rebase for the last 3 commits.

  #### Modify the commits by changing pick to one of the following:

* squash (combine commits)
* reword (edit commit message)
* edit (edit commit content)
* drop (remove commit)
* Example of squashing two commits:

Change the second commit from pick to squash and save.
Git will combine the commit messages for the squashed commit.

## Task 7: Complete Interactive Rebase
#### 1.After modifying the commits, save and close the editor.
#### 2.Resolve any conflicts if prompted, then continue the rebase

git rebase --continue`  
  Completes the rebase after resolving conflicts.

---

# Part 4: Cherry-Picking Commits

## Task 8: Pick a Specific Commit
#### 01.View the commit history to find the commit hash you want to cherry-pick:


```
git log --oneline
```  
  * Finds the commit hash to cherry-pick.
  #### 2.Cherry-pick a specific commit by its hash:


```
git cherry-pick <commit-hash>
```  
 * Applies a specific commit to the current branch.
 #### 3.Resolve conflicts if any, then commit the changes:


```
git cherry-pick --continue
```  
 * Resolves conflicts and finishes cherry-picking.

---

# Part 5: Tagging Commits

## Task 9: Tag a Commit
#### 1.Tag the current commit with a version number:


```
git tag -a v1.0 -m "Initial release"
```  
 * Tags the current commit with a message.
 #### 2.List all tags:

```
git tag
```  
 * Lists all tags.

## Task 10: Tag a Specific Commit
#### 1.Tag a specific commit by its hash:

```
git tag -a v1.1 <commit-hash> -m "Bug fix"
```  
 * Tags a specific commit by its hash.

## Task 11: Push Tags to Remote
#### 1.Push a specific tag to the remote repository:


```
git push origin v1.0
```  
 * Pushes a specific tag to the remote repository.
 #### 2.Push all tags to the remote repository:


```
git push --tags
```  
Push all tags to the remote repository:

 * Pushes all tags to the remote repository.

---

# Part 6: Working with Remote Repositories

## Task 12: Add a Remote Repository
#### 1.Add a remote repository URL to the project:

```
git remote add origin https://github.com/username/repo.git
```  
 * Adds a remote repository named `origin`.

## Task 13: Fetch Changes from Remote
#### 1.Fetch changes from the remote repository without merging them:


```
git fetch origin
```  
 * Fetches changes from the remote repository without merging.
 #### 2.View fetched branches:


```
git branch -r
```  
 * Lists remote branches.

## Task 14: Pull Changes from Remote
#### 1.Pull the latest changes from the remote repository and merge them into the local branch:

```
git pull origin main
```  
 * Fetches and merges changes from the remote `main` branch.

## Task 15: Push Changes to Remote
#### 1.Push local changes to the remote repository:


```
git push origin main
```  
 * Pushes local changes to the remote `main` branch.
 #### 2.Push a new branch to the remote repository:


```
git push origin feature-branch
```  
 * Pushes a new branch to the remote repository.

## Task 16: Delete Remote Branch
#### 1.Delete a remote branch:

 ```
 git push origin --delete feature-branch
 ```  
  * Deletes a branch from the remote repository.

---

# Part 7: Forking and Contributing to Open-Source Projects

## Task 17: Fork a Repository on GitHub
- Fork a repository via GitHub UI and clone your fork: 
#### 1.Go to a repository on GitHub and click Fork in the top right corner to create your own copy of the repository.
#### 2.Clone the forked repository to your local machine:



 
  ```
  git clone https://github.com/your-username/repo.git
  ```

### Task 18: Make Changes and Commit
#### 1.Create a new branch for your changes:


```
git checkout -b fix-typo
``` 
 * Creates a new branch for changes.
 #### 2.Make changes to the code (e.g., fix a typo in README.md), stage, and commit them:


```
git add README.md
```  
 * Stages the modified file.
```
git commit -m "Fixed typo in README.md"
```  
 *  Commits the changes with a descriptive message.

## Task 19: Push Changes to Your Fork
#### 1.Push the changes to your remote fork:

```
git push origin fix-typo
```  
 * Pushes the changes to your forked repository.

## Task 20: Create a Pull Request
- Submit a pull request via GitHub after pushing your changes.

## Task 21: Sync Your Fork with the Original Repository
#### 1.Add the original repository as a remote source:


```
git remote add upstream https://github.com/original-owner/repo.git
```  
  Adds the original repository as a remote named `upstream`.
  #### 2.Fetch changes from the original repository:


```
git fetch upstream
```  
  Fetches changes from the original repository.
  #### 3.Merge changes from the original repository into your local branch:


```
git merge upstream/main
```  
  Merges the changes into your local branch.
  #### 4.Push the changes to your fork:


```
git push origin main
```  
  Pushes the updates to your fork.

---
# Consolidated Summary
#### 1.Stashing: Saving and applying uncommitted changes temporarily.
#### 2.Rewriting History: Using git rebase and interactive rebase to modify and clean up commit history.
#### 3.Cherry-Picking: Selecting specific commits from another branch.
#### 4. Tagging: Labeling commits for versioning.
#### 5.Working with Remote Repositories: Managing remotes, pushing, pulling, and fetching changes.
#### 6.Forking & Contributing: Forking repositories, contributing to open-source projects, and syncing your fork.