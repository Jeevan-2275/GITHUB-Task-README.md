# TASK List: Focused Management, commits, Branching & Merging, and Code Review
# Git Commands and Explanations
## Part 1: Creating and Cloning Repositories
### Task 1: Create a Local Git Repository
```bash
mkdir MyProject
```
- Creates a new folder named "MyProject."
```
cd MyProject
```
- Navigates into the "MyProject" folder.
### 2.Initialize it as a Git repository:
```
git init
```
 -Initializes a new Git repository in the current folder by creating a .git directory.
### 3.Verify the repository status
```
git status
```
- Shows the current status of the repository, including untracked and staged files.
### Task 2: Clone a Remote Repository
```bash
git clone https://github.com/username/repo.git
```
- Clones a remote repository to your local system.
```bash
cd repo
```
- Navigates into the cloned repository folder.
```bash
ls -a 
```
- Lists all files, including hidden ones like .git, to verify that the repository was cloned.
## Part 2: Understanding Commits and Commit Messages
### Task 3: Commit Changes Locally
```bash
echo "Welcome to Git" > README.md
```
- Creates a new file called README.md with the content "Welcome to Git."
```bash
git add README.md
```
- Stages README.md for committing.
```bash
git commit -m "Initial commit: Added README.md"
```
- Commits the staged changes with a message "Initial commit: Added README.md."
### Task 4: Write Effective Commit Messages
```bash
git commit -m "Added initial version of README.md with project overview"
```
- Commits changes with a detailed message describing what was added.
```bash
touch file1.txt file2.txt
```
- Creates two new empty files: file1.txt and file2.txt.
```bash
git add .
```
- Stages all changes in the current directory.
```bash
git commit -m "Added two new files for feature setup"
```
- Commits the staged files with a single message.
## Part 3: Viewing Commit History with git log
### Task 5: View Detailed Commit History
```bash
git log
```
- Displays a list of all commits made in the repository, including commit hashes, authors, dates, and
```bash
git log --oneline
```
- Displays a compact commit history with a single line for each commit.
### Task 6: Customize Log Outputs
```bash
git log --oneline --graph --decorate
```
- Shows a compact history with a graphical representation of branches and tags.
```bash
git log README.md
```
- Displays commit history that affects only the README.md file.
## Part 4: Understanding Branching and Merging
### Task 7: Understanding Branching
```bash
git branch
```
Lists all branches in the repository and highlights the current one.
```bash
git branch feature-branch
```
Creates a new branch called feature-branch.
```bash
git checkout feature-branch
```
Switches to the feature-branch.
```bash
git checkout -b feature-branch
```
Creates and switches to a new branch called feature-branch.
## Part 5: Creating and Working with Branches
### Task 8: Make Changes in a Branch
```bash
echo "Feature in progress" > feature.txt
```
Creates a new file called feature.txt with the content "Feature in progress."
```bash
git add feature.txt
```
Stages feature.txt for committing.
```bash
git commit -m "Added feature.txt in feature-branch"
```
Commits feature.txt with a message.
### bTask 9: Merging Branches
```bash
git checkout main
```
Switches back to the main branch.
bash
```
git merge feature-branch
```
Merges the changes from feature-branch into main.
## Part 6: Resolving Merge Conflicts
### Task 10: Simulate a Merge Conflict
```bash
echo "Main branch content" > conflict.txt
```
Creates a file called conflict.txt in the main branch.
```bash
git add conflict.txt
```
Stages conflict.txt for committing.
```bash
git commit -m "Added conflict.txt in main branch"
```
Commits the file in the main branch.
```bash
git checkout feature-branch
```
Switches to the feature-branch.
```bash
echo "Feature branch content" > conflict.txt
```
Creates or modifies conflict.txt with conflicting content.
```bash
git add conflict.txt
```
Stages the conflicting version for committing.
```bash
git commit -m "Modified conflict.txt in feature-branch"
```
Commits the conflicting changes.
```bash
git checkout main
```
Switches back to the main branch.
```bash
git merge feature-branch
```
Attempts to merge feature-branch into main, leading to a conflict.
Resolve the conflict manually by editing conflict.txt.
```bash
git add conflict.txt
```
Stages the resolved file.
```bash
git commit -m "Resolved conflict in conflict.txt"
```
Commits the conflict resolution.
## Part 7: Deleting and Renaming Branches
### Task 11: Delete a Branch
```bash
git branch -d feature-branch
```
Deletes the feature-branch if it has been merged.
```bash
git branch -D feature-branch
```
Force-deletes the feature-branch even if it hasn’t been merged.
### Task 12: Rename a Branch
```bash
git branch -m new-branch-name
```
Renames the current branch to new-branch-name.
```bash
git branch -m old-branch-name new-branch-name
```
Renames old-branch-name to new-branch-name.