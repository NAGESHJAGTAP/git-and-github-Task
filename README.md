# Advanced Git Operations

This document provides an in-depth guide to advanced Git operations, including stashing changes, rewriting history, cherry-picking commits, tagging versions, working with remote repositories, and contributing to open-source projects. This guide is aimed at developers looking to enhance their Git workflow for better efficiency and collaboration.

---

# 📌 Part 1: Understanding and Using `git stash`

## ✅ Task 1: Save Changes Temporarily with `git stash`

### 1️⃣ Modify a file without committing changes:
```sh
echo "Temporary changes" >> temp-file.txt
```
* Adds temporary content to a file.

### 2️⃣ View the status of changes:
```sh
git status
```
* Displays the status of unstaged changes.

### 3️⃣ Stash the changes:
```sh
git stash
```
* Saves changes to a stash and resets the working directory to the last commit.

### 4️⃣ View the stashed changes:
```sh
git stash list
```
* Shows a list of stashed changes.

## ✅ Task 2: Apply and Drop Stashed Changes

### 1️⃣ Apply the most recent stash:
```sh
git stash apply
```
* Applies the most recent stash without removing it from the stash list.

### 2️⃣ Drop the most recent stash after applying it:
```sh
git stash drop
```
* Deletes the most recent stash entry.

### 3️⃣ Apply a specific stash:
```sh
git stash apply stash@{1}
```
* Applies a specific stash by its identifier.

## ✅ Task 3: Stash Untracked Files

### 1️⃣ Stash changes, including untracked files:
```sh
git stash -u
```
* Stashes both tracked and untracked files.

### 2️⃣ Apply stashed changes including untracked files:
```sh
git stash apply
```
* Applies the stashed changes, including untracked files.

---

# 📌 Part 2: Rewriting History with `git rebase`

## ✅ Task 4: Rebase Commits to a New Base

### 1️⃣ Rebase the current branch onto `main`:
```sh
git rebase main
```
* Moves the commits of the current branch on top of the `main` branch.

### 2️⃣ Resolve conflicts and continue:
```sh
git rebase --continue
```
* Resolves conflicts and proceeds with the rebase process.

## ✅ Task 5: Cancel a Rebase

### 1️⃣ Abort the rebase if needed:
```sh
git rebase --abort
```
* Cancels the rebase and restores the branch to its original state.

---

# 📌 Part 3: Interactive Rebase (`git rebase -i`)

## ✅ Task 6: Modify Commit History with Interactive Rebase

### 1️⃣ View the last few commits:
```sh
git log --oneline
```
* Displays a compact commit history.

### 2️⃣ Start an interactive rebase for the last 3 commits:
```sh
git rebase -i HEAD~3
```
* Opens an interactive rebase session for the last 3 commits.

Modify commits by changing `pick` to:
- `squash` (combine commits)
- `reword` (edit commit message)
- `edit` (modify commit content)
- `drop` (remove commit)

## ✅ Task 7: Complete Interactive Rebase

### 1️⃣ Save and close the editor after making changes.
### 2️⃣ Resolve conflicts and continue:
```sh
git rebase --continue
```
* Completes the rebase after conflict resolution.

---

# 📌 Part 4: Cherry-Picking Commits

## ✅ Task 8: Apply a Specific Commit from Another Branch

### 1️⃣ Find the commit hash to cherry-pick:
```sh
git log --oneline
```
* Displays commit hashes and messages.

### 2️⃣ Cherry-pick a specific commit:
```sh
git cherry-pick <commit-hash>
```
* Applies the specified commit to the current branch.

### 3️⃣ Resolve conflicts if needed:
```sh
git cherry-pick --continue
```
* Completes cherry-picking after conflict resolution.

---

# 📌 Part 5: Tagging Commits

## ✅ Task 9: Tag a Commit

### 1️⃣ Tag the current commit with a version number:
```sh
git tag -a v1.0 -m "Initial release"
```
* Creates an annotated tag with a message.

### 2️⃣ List all tags:
```sh
git tag
```
* Displays all available tags.

## ✅ Task 10: Push Tags to Remote

### 1️⃣ Push a specific tag:
```sh
git push origin v1.0
```
* Pushes the specified tag to the remote repository.

### 2️⃣ Push all tags:
```sh
git push --tags
```
* Pushes all tags to the remote repository.

---

# 📌 Part 6: Working with Remote Repositories

## ✅ Task 11: Add a Remote Repository
```sh
git remote add origin https://github.com/username/repo.git
```
* Links a remote repository named `origin`.

## ✅ Task 12: Fetch Changes from Remote
```sh
git fetch origin
```
* Retrieves updates from the remote repository without merging.

## ✅ Task 13: Pull Changes from Remote
```sh
git pull origin main
```
* Fetches and merges changes from the remote `main` branch.

## ✅ Task 14: Push Changes to Remote
```sh
git push origin main
```
* Pushes local commits to the remote `main` branch.

---

# 📌 Part 7: Forking and Contributing to Open-Source Projects

## ✅ Task 15: Fork a Repository on GitHub
- Use the GitHub UI to fork a repository.
- Clone the forked repository:
```sh
git clone https://github.com/your-username/repo.git
```

## ✅ Task 16: Create a Pull Request
- Submit a pull request (PR) via GitHub after pushing your changes.

## ✅ Task 17: Sync Your Fork with the Original Repository
```sh
git remote add upstream https://github.com/original-owner/repo.git
```
* Links the original repository as `upstream`.

```sh
git fetch upstream
```
* Fetches updates from the upstream repository.

```sh
git merge upstream/main
```
* Merges updates into your local branch.

```sh
git push origin main
```
* Pushes the updates to your forked repository.

---

# 📌 GitHub Repository
[🔗 Visit GitHub Repository](https://github.com/your-username/repo)

---

# 📌 Summary
- **Stashing:** Temporarily save and apply uncommitted changes.
- **Rewriting History:** Modify commit history using `git rebase`.
- **Cherry-Picking:** Apply specific commits from another branch.
- **Tagging:** Label commits for versioning.
- **Remote Repositories:** Manage remotes, pushing, pulling, and fetching changes.
- **Forking & Contributing:** Collaborate effectively in open-source projects.

🎯 **Master these Git techniques to boost your development workflow!** 🚀

