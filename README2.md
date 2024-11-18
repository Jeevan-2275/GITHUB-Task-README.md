# Git Commands Overview

## Part 1: Git Basics

### Task 1: Install and Configure Git
```bash
[git-scm.com](https://git-scm.com/).
```
- Install Git from 
  
```bash
git config --global user.name "Your Name"
```

- Sets your Git username globally.

```bash
git config --global user.email "your-email@example.com"
```
- Sets your Git email address globally.

```bash
git config --list
```



### Task 2: Initialize a Repository
- Create a directory and initialize it as a Git repository:
```
mkdir MyProject
```

- Creates a new directory named `MyProject`.
```
cd MyProject
```

- Navigates into the `MyProject` directory.

```
git init
```

- Initializes a new Git repository, creating a hidden `.git` folder to track changes.

## Part 2: Basic Workflow

### Task 3: Creating and Committing Files
- Create a file:

```
echo "Hello Git" > file1.txt
```


- Creates a file named `file1.txt` with the content "Hello Git".

- Stage and commit the file:

```
git add file1.txt
```

- Stages `file1.txt` for commit.

```
git commit -m "Initial commit: Added file1.txt"
```

- Commits the staged file with a message.

### Task 4: Viewing Changes
- Modify the file:

```
echo "Git is awesome!" >> file1.txt
```

- Appends "Git is awesome!" to `file1.txt`.

- Check file status and differences:
```
git status
```

- Shows the working directory status and any staged changes.

```
git diff
```

- Displays differences between the working directory and the last commit.

### Task 5: Undoing Changes
- Unstage a staged file:

```
git reset file1.txt
```

- Unstages `file1.txt` but keeps the changes in the working directory.

- Discard uncommitted changes:
```
git checkout -- file1.txt
```

- Reverts `file1.txt` to the last committed version.

## Part 3: Branching and Merging

### Task 6: Branch Management
- Create a branch and switch to it:
```
git checkout -b feature-branch
```

- Creates and switches to a new branch called `feature-branch`.

- List branches:
```
git branch
```

- Lists all branches in the repository.

- Rename a branch:
```
git branch -m feature-branch feature-enhanced
```

- Renames `feature-branch` to `feature-enhanced`.

### Task 7: Merging Branches
- Merge `feature-enhanced` into `main`:
```
git checkout main
```

- Switches to the `main` branch.
```
git merge feature-enhanced
```

- Merges `feature-enhanced` branch into `main`.

### Task 8: Handling Merge Conflicts
- Create two conflicting branches and resolve a conflict manually:
```
git merge <branch-name>
```

- Attempts to merge `<branch-name>` into the current branch, possibly causing a conflict.

- Resolve conflicts, then:
```
git add <resolved-file>
```

- Stages the resolved file.
```
git commit
```

- Commits the resolved changes.

## Part 4: Remote Repositories

### Task 9: Remote Setup
- Add a remote repository:
```
git remote add origin https://github.com/your-username/repo.git
```

- Adds a remote named `origin` to your repository.

- Verify the remote:
```
git remote -v
```

- Displays the current remotes.

### Task 10: Push and Pull
- Push changes to the remote repository:
```
git push -u origin main
```

- Pushes the `main` branch to the remote repository and sets the upstream.

- Pull changes from the remote:
```
git pull origin main
```

- Pulls the latest changes from the `main` branch on the remote repository.

### Task 11: Cloning a Repository
- Clone a remote repository:
```
git clone https://github.com/your-username/repo.git
```

- Creates a local copy of the repository.

## Part 5: Advanced Git

### Task 12: Stashing Changes
- Save uncommitted changes:
```
git stash
```

- Stashes the current changes without committing.

- Apply stashed changes:
```
git stash apply
```

- Reapplies the most recent stash.

- Drop the stash:
```
git stash drop
```

- Deletes the latest stash after applying it.

### Task 13: Tagging Commits
- Create and annotate a tag:
```
git tag -a v1.0 -m "Version 1.0 release"
```

- Tags the current commit with version `v1.0`.

- Push the tag to the remote:
```
git push origin v1.0
```

- Pushes the `v1.0` tag to the remote repository.

### Task 14: Rewriting Commit History
- Use interactive rebase to modify commit messages:
```
git rebase -i HEAD~3
```

- Opens an interactive rebase editor for the last 3 commits.

- Replace `pick` with `edit` or `squash` as needed.

### Task 15: Cherry-Picking Commits
- Apply a specific commit to another branch:
```
git cherry-pick <commit-hash>
```

- Applies the changes from the specified commit to the current branch.

## Part 6: Collaboration

### Task 16: Forking and Pull Requests
- Fork a repository and clone it locally:
```bash
git clone https://github.com/your-username/forked-repo.git
```

- Creates a local copy of the forked repository.

- Make changes and push them:
```
git checkout -b fix-typo
```
- Creates and switches to a new branch called `fix-typo`.
```bash
echo "Typo fixed" >> README.md
```
- Fixes a typo in `README.md`.
```
git commit -m "Fixed a typo"
```

- Commits the typo fix.
```
git push origin fix-typo
```
Pushes the `fix-typo` branch to the remote.

- Open a pull request on GitHub.

### Task 17: Simulating Team Collaboration
- Simulate a conflict by having two users modify the same file.

- Practice resolving the conflict as a team.

## Part 7: Ignoring Files

### Task 18: Using .gitignore
- Create a `.gitignore` file:
```
echo "node_modules/" > .gitignore
```

- Adds `node_modules/` to `.gitignore`.
```
git add .gitignore
```

- Stages the `.gitignore` file.
```
git commit -m "Added .gitignore"
```

- Commits the `.gitignore` file.

- Verify that ignored files are not staged:
```
git status
```

- Confirms that `node_modules/` is being ignored.

## Part 8: Automation and Cleanup

### Task 19: Cleaning the Repository
 
```
git clean -f
```
Removes untracked files.



### Task 20: Aliases and Shortcuts
- Create an alias for frequently used commands:
```
git config --global alias.st status
```
Creates an alias for `status`.
```
git config --global alias.cm commit
```

- Creates an alias `cm` for `git commit`.

- Use the alias:
```
git status
```
- Short for `git status`.
```
git cm -m "Message"
```
- Short for `git commit -m "Message"`.