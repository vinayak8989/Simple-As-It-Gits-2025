# Simple As It Gits 2025 Curriculum

*"Simple as it Gits"* is a full-day, hands-on workshop on Git and GitHub, conducted by FOSS Club SSET.

## Table of Content

- [Module 1: Git Fundamentals & Local Workflow](#module-1-git-fundamentals--local-workflow)
- [Module 2: Branching & Merging](#module-2-branching--merging)
- [Module 3: GitHub Integration](#module-3-github-integration)
- [Module 4: Collaboration Workflow](#module-4-collaboration-workflow)
- [Module 5: Undoing Changes](#module-5-undoing-changes)
- [Module 6: Advanced Practices](#module-6-advanced-practices)


## Module 1: Git Fundamentals & Local Workflow
### Concepts Covered:

- Version control basics

- Repository initialization

- Staging/Committing

- Change tracking

```bash
CLI Commands:
git init
git status
git add <file>            # Stage specific file
git add .                 # Stage all changes
git commit -m "Message"
git log
git diff
```

### Installation & Initial Configuration

> [Use the official website](https://git-scm.com/) to download git

Setting up the global identity

```bash
# Configure author name
git config --global user.name "Alex Johnson"

# Configure author email
git config --global user.email "alex@example.com"
```

### Exercise:

1. Create a project folder with mkdir

```bash
mkdir my-first-git-repo
cd my-first-git-repo
```

2. Initialize Git repo

```bash
git init
```

3. Create README.md and write something

```bash
code README.md
```

4. Stage & commit

```bash
git add README.md
git commit -m "My first commit"
```

5. Check Log

```bash
git log
```

6. Modify README.md then check status & diff

```bash
git status
git diff
```
7. Stage, commit all changes and check log

```bash
git add .
git commit -m "<message>"
git log
```

## Module 2: Branching & Merging
### Concepts Covered:

- Branch isolation

- Fast-forward vs. 3-way merges

- Conflict resolution

```bash
CLI Commands:

bash
git branch                       # List branches
git branch <name>                # Create branch
git switch <branch>              # Switch branch
git switch -c <new-branch>       # Create & switch
git merge <branch>               # Merge into current branch
```

### Exercise:

1. Create feature branch from main

2. Make conflicting changes in both branches

3. Resolve merge conflict manually:

3. Edit conflicted files

4. git add resolved files

5. git commit

## Module 3: GitHub Integration
### Concepts Covered:

- Remote repositories

- Push/Pull workflow

- Clone vs. Fork
```bash
CLI Commands:

bash
git remote add origin <URL>     # Link local ↔ remote
git push -u origin main         # First push (set upstream)
git push                        # Subsequent pushes
git pull                        # Fetch + merge
git clone <URL>
```
### Exercise:

1. Create GitHub repo (no README/license)
Create an account on GitHub
Initialize a repository 
    
2. Connect local repo to GitHub
reference: https://docs.github.com/en/authentication/connecting-to-github-with-ssh
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```
Enter file in which to save the key (/c/Users/YOU/.ssh/id_ALGORITHM):[Press enter]
```bash
clip < ~/.ssh/id_ed25519.pub
```
In the upper-right corner of any page on GitHub, click your profile picture, then click  Settings.

In the left sidebar: Access > SSH and GPG keys

Click New SSH key or Add SSH key.

In the "Title" field, add a descriptive label for the new key.

In the "Key" field, paste what was copied from the clip command

Click Add SSH key.

```bash
git remote add origin git@github.com:YourUsername/YourRepository.git
```
4. Push branches
```bash
git push -u origin main
```
If your local branch is named master, use:
```bash
git push -u origin master
```
5. Clone a partner's repo
```bash
git clone git@github.com:partnerusername/their-repo-name.git
```   

## Module 4: Collaboration Workflow
### Concepts Covered:

- Pull Requests (GitHub UI)

- Fetching changes

- Upstream tracking
  
```bash
CLI Commands:

bash
git fetch                        # Check remote changes
git merge origin/main            # Merge fetched changes
git pull --rebase                # Rebase instead of merge
git push --force-with-lease      # Safely overwrite history
```
### Exercise:

1. Simulate team collaboration:

2. Partner A: Push commit to main

3. Partner B: git fetch → git merge

4. Create PR via GitHub, review diff

5. Resolve merge conflict via CLI

## Module 5: Undoing Changes
### Concepts Covered:

- Commit history rewriting

- Stashing temporary work

```bash
CLI Commands:

bash
git restore <file>              # Discard uncommitted changes
git reset --soft HEAD~1         # Undo commit (keep changes)
git reset --hard HEAD~1         # ⚠️ Destroy last commit
git revert <commit-hash>        # Safe undo for shared history
git stash                       # Temporary shelf
```

### Exercise:

1. Undo and recommit
-Make a change and commit it
```bash
git reset --soft HEAD~1
```
-Modify the file and recommit the updated change

2. Discard Broken Code
-intentionally break a file
-Discard changes with:
```bash
git restore <file>
```

3. Revert a pushed commit
-Identify the hash of a commit already pushed
```bash
git revert <commit-hash>
```
-Push the reverted commit to remote
```bash
git push
```

4. Use git stash
-Make uncommitted changes
```bash
git stash
```
-switch branches of perform other tasks
-reapply the changes with:
```bash
git stash pop
```

## Module 6: Advanced Practices
### Concepts Covered:

- .gitignore patterns

- Tagging releases

- Rebasing vs. merging

```bash
CLI Commands:

bash
# .gitignore patterns
*.log
temp/
git tag v1.0                  # Release tagging
git rebase main               # Reapply commits on updated base
git cherry-pick <commit>      # Grab specific commit
```
