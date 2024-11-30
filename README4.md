# Advanced Git Operations
## Part 1: Understanding and Using git stash
### Task 1: Save Changes Temporarily with git stash
1.Make changes to a file without committing:

```bash
echo "Temporary changes" >> temp-file.txt
```
- Make changes to a file without committing.
```bash
git status
```
- View the status of the changes.

```bash
git stash
```
- Saves changes to a stash and restores the working directory to the last committed state.
```bash
git stash list
```
- Displays a list of stashed changes.
```bash
git stash apply
```
- Applies the most recent stash.
```bash

git stash drop
```
- Removes the most recently applied stash from the stash list.
```bash
git stash apply stash@{1}
```
- Applies a specific stash using its identifier.
```bash
git stash -u
```
- Stashes changes, including untracked files.
```bash
git stash apply
```
- Restores the latest stash, including untracked files.

## Part 2: Rewriting History with git rebase
```bash
git rebase main
```
- Reapplies commits from your current branch on top of the latest commit in main.
```bash
git rebase --continue
```
- Continues the rebase process after resolving conflicts.
```bash
git rebase --abort
```
- Cancels the rebase and returns the branch to its original state.

## Part 3: Interactive Rebase (git rebase -i)
```bash
git log --oneline
```
- View a summary of recent commits.
```bash
git rebase -i HEAD~3
```
- Starts an interactive rebase for the last 3 commits.

## Interactive Options:
```bash
pick
```
- Keep the commit as is.
```bash
squash
```
- Combine commits.
```bash
reword
```
- Edit commit message.
```bash
edit
```
- Edit commit content.
```bash
drop
```
Remove commit.
```bash
git rebase --continue
```
- Continues the interactive rebase after resolving any conflicts.

## Part 4: Cherry-Picking Commits (git cherry-pick)
```bash
git log --oneline
```
- Displays recent commits in a concise format.
```bash
git cherry-pick <commit-hash>
```
- Applies changes from a specific commit to the current branch.
```bash
git add .
```
- Stages resolved files.
```bash
git cherry-pick --continue
```
- Completes the cherry-pick after conflict resolution.

## Part 5: Tagging Commits (git tag)
```bash 
git tag -a v1.0 -m "Initial release"
```
- Tags the current commit with a version number.
```bash
git tag
```
- Lists all tags in the repository.
```bash
git tag -a v1.1 <commit-hash> -m "Bug fix"
```
- Tags a specific commit by its hash.
```bash
git push origin v1.0
```
- Pushes a specific tag to the remote repository.
```bash
git push --tags
 ```
 - Pushes all local tags to the remote repository.

## Part 6: Working with Remote Repositories
```bash
git remote add origin https://github.com/username/repo.git
```
- Adds a remote repository URL to the project.
```bash
git fetch origin
```
- Fetches changes from the remote repository without merging them.
```bash
git branch -r
```
- Lists all remote-tracking branches.
```bash
git pull origin main
```
- Downloads and merges updates from the main branch of the remote repository.
```bash
git push origin main
``` 
- Pushes local changes to the main branch of the remote repository.
```bash
git push origin feature-branch
```
- Creates and uploads feature-branch to the remote.
```bash
git push origin --delete feature-branch
```
- Deletes a remote branch.

## Part 7: Forking and Contributing to Open-Source Projects
### GitHub Action:
 **Fork a repository on GitHub by clicking "Fork" to create your own copy of the repository.**
```bash
git clone https://github.com/your-username/repo.git
 ```
 - Clones the forked repository to your local machine.
```bash
git checkout -b fix-typo
```
- Creates and switches to a new branch named fix-typo.
```bash
git add README.md
```
- Stages README.md for commit.
```bash
git commit -m "Fixed typo in README.md"
```
- Commits the staged changes with a descriptive message.
```bash
git push origin fix-typo
```
- Uploads the fix-typo branch to your forked repository.

**GitHub Action:**

Go to your forked repository on GitHub and click "Compare & Pull Request" to submit changes to the original repository.
```bash
git remote add upstream https://github.com/original-owner/repo.git
```
- Adds the original repository as a remote source.
```bash
git fetch upstream
```
- Fetches changes from the original repository.
```bash
git checkout main
```
- Switches to the main branch.
```bash
git merge upstream/main
```
- Integrates updates from the upstream repository.
```bash
git push origin main
```
- Updates your fork with the synchronized changes.