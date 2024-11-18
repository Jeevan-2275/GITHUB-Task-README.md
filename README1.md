# Git Commands Overview

## Part 1: Introduction to Version Control and Git

### Task 1: Install and Configure Git
 ```bash
git config --global user.name "Your Name
```  
  - Sets your Git username globally.
 ```bash
 git config --global user.email "your-email@example.com"
 ```  
  - Sets your Git email address globally.
```bash
git config --list
```  
  - Displays the current Git configuration settings.

### Task 2: Initialize a Repository
```bash
mkdir MyProject
```  

  - Creates a new directory named MyProject.

```bash
cd MyProject
```
  - Navigates into the MyProject directory.

  ```bash
  .git init
  ```
  - Initializes a new Git repository in the current directory.
    


### Task 3: Create a File and Make Multiple Commits
```bash
echo "My First Project" > README.md
``` 
  - Creates a README.md file with initial content.
 
```bash
git add README.md
```  
  - Stages README.md for commit.
```bash
git commit -m "Initial commit: Added README.md"
``` 
  - Commits the staged file with a message.
 
```bash
echo "Added a description" >> README.md
```
  - Appends a description to README.md.
  
```bash
git add README.md
```  
  - Stages the modified README.md file.
```bash
git commit -m "Updated README with a description"
```  
  - Commits the updated README.md.

### Task 4: Check Status and Log
```bash
git status
```  
  - Shows the working directory status and any staged changes.
```bash
git log --oneline --graph --decorate
```  
  - Displays a brief, graphical commit history.

### Task 5: Create and Clone a Repository
```bash
git clone http://codinggita.com/example-repo
```  
  - Clones the repository from the provided URL to your local machine.

### Task 6: Understanding the Git Workflow
```bash
echo "Workflow example" > workflow.md
```  
  - Creates a file named workflow.md.
```bash
git add workflow.md
```  
  - Stages workflow.md.
```bash
git commit -m "Added workflow example"
```  
  - Commits the file with a message.

## Part 2: Working with Repositories

### Task 7: Branching and Merging
```bash
git branch feature-login
```  
  - Creates a new branch called feature-login.
```bash
git checkout feature-login
```  
  - Switches to the feature-login branch.
```bash
git checkout -b feature-login
```  
  - Creates and switches to a new branch named feature-login.
```bash
echo "Login Page" > login.html
```  
  - Creates a file called login.html.
```bash
git add login.html
```  
  - Stages login.html for commit.
```bash
git commit -m "Added login page"
```  
  - Commits the login.html file.
```bash
git checkout main
```  
  - Switches back to the main branch.
```bash
git merge feature-login
```  
  - Merges feature-login branch into main.

### Task 8: Handling Merge Conflicts
```bash
git branch branch-A
```  
  - Creates a new branch called branch-A.
```bash
git branch branch-B
```  
  - Creates a new branch called branch-B.
```bash
git checkout main
```  
  - Switches to the main branch.
```bash
git merge branch-A
```  
  - Merges branch-A into the main branch.
```bash
git merge branch-B
```  
  - Attempts to merge branch-B into main 
```bash
git add README.md
```  
  - Stages the conflict-resolved README.md file.
```bash
git commit -m "Resolved merge conflict between branch-A and branch-B"
```  
  - Commits the merge conflict resolution.

### Task 9: Renaming and Deleting Branches
```bash
git branch -m old-branch-name new-branch-name
```  
  - Renames a branch.
```bash
git branch -d feature-login
```  
  - Deletes the feature-login branch.

## Part 3: Advanced Git Operations

### Task 10: Using Git Stash
```bash
echo "Temporary work" >> temp.md
```  
  - Adds temporary content to temp.md.
```bash
git stash
```  
  - Stashes uncommitted changes.
```bash
git stash list
```  
  - Lists all stashed changes.
```bash
git stash apply
```  
  - Applies the latest stashed changes.
```bash
git stash drop
```  
  - Removes the most recent stash after applying.

### Task 11: Rewriting History with Interactive Rebase
```bash
echo "Commit 1" > file1.txt && git add file1.txt && git commit -m "Commit 1"
```  
  - Creates and commits file1.txt.
```bash
echo "Commit 2" > file2.txt && git add file2.txt && git commit -m "Commit 2"
```  
  - Creates and commits file2.txt.
```bash
echo "Commit 3" > file3.txt && git add file3.txt && git commit -m "Commit 3"
```  
  - Creates and commits file3.txt.
```bash
git rebase -i HEAD~3
```  
  - Interactive rebase for the last 3 commits to combine or modify.

### Task 12: Cherry-Picking Commits
```bash
git checkout -b cherry-pick-example
```  
  - Creates and switches to a new branch.
```bash
git cherry-pick <commit-hash>
```  
  - Picks a specific commit from another branch to apply to the current one.

### Task 13: Tagging Commits
```bash
git tag -a v1.0 -m "Version 1.0 release"
```  
  - Tags the current commit with version 1.0.
```bash
git push origin v1.0
```  
  - Pushes the tag to the remote repository.

### Task 14: Working with Remote Repositories
```bash
git remote add origin <repository-url>
```  
  - Adds a remote repository.
```bash
git push origin main
```  
  - Pushes local changes to the remote main branch.

### Task 15: Forking and Contributing
```bash
git clone <forked-repo-url>
```  
  - Clones the forked repository.
```bash
git checkout -b fix-typo
```  
  - Creates a new branch called fix-typo.
```bash
echo "Typo fixed" >> README.md
```  
  - Fixes a typo in README.md.
```bash
git add README.md
```  
  - Stages the typo fix.
```bash
git commit -m "Fixed a typo"
```  
  - Commits the typo fix.
```bash
git push origin fix-typo
```  
  - Pushes the fix to the remote.

## Part 4: Additional Practice

### Task 16: Simulate Team Collaboration
- Practice making changes to the same file simultaneously with a collaborator and resolve merge conflicts.

### Task 17: Git Ignore
```bash
echo "node_modules/" > .gitignore
```  
  - Creates a 
  .gitignore
   file to ignore the
     node_modules 
   folder.
```bash
git add .
```  
  - Adds all files except those ignored by 
  .gitignore

