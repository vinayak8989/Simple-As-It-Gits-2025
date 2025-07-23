# Simple As It Gits 2025 Curriculum

*"Simple as it Gits"* is a full-day, hands-on workshop on Git and GitHub, conducted by FOSS Club SSET.

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
### Exercise:

1. Create a project folder with mkdir

2. Initialize Git repo

3. Create README.md, modify it, stage & commit

4. Check status/history after each step

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

2. Connect local repo to GitHub

3. Push branches

4. Clone a partner's repo

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

1. Commit → git reset --soft → modify → recommit

2. Intentionally break code → git restore

3. Use git revert on pushed commit

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
