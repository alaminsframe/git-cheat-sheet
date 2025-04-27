# Git and GitHub Cheat Sheet

## Basics

### Configuration
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Create or Initialize a Repo
```bash
# Initialize in an existing folder
git init

# Clone an existing repo
git clone <repository-url>
```

### Basic Workflow
```bash
# Check current status
git status

# Stage changes
git add <file-name>
# Stage all changes
git add .

# Commit changes
git commit -m "Your commit message"

# Push changes to remote
git push

# Pull latest changes
git pull

# View commit history
git log

# View concise commit history
git log --oneline
```

## Branching

### Create, View, Switch, and Rename Branches
```bash
# List all branches
git branch

# Create new branch
git branch <branch-name>

# Switch to a branch
git checkout <branch-name>

# Create and switch in one command
git checkout -b <branch-name>

# Rename current branch
git branch -m <new-branch-name>

# Rename a specific branch
git branch -m <old-branch-name> <new-branch-name>
```

### Merge and Delete Branches
```bash
# Merge branch into current branch
git merge <branch-name>

# Delete a branch locally
git branch -d <branch-name>
# Force delete a branch locally
git branch -D <branch-name>

# Delete a branch remotely
git push origin --delete <branch-name>
```

## Remote Repositories

```bash
# Add a remote repository
git remote add origin <repository-url>

# View configured remotes
git remote -v

# Push a branch to remote
git push -u origin <branch-name>

# Fetch latest from remote without merging
git fetch

# Fetch and merge from remote
git pull

# Remove a remote
git remote remove <remote-name>

# Rename a remote
git remote rename <old-name> <new-name>
```

## Advanced

### Undo Changes
```bash
# Unstage a file
git reset <file-name>

# Undo local changes
git checkout -- <file-name>

# Revert a commit (creates a new commit)
git revert <commit-hash>
```

### Resetting Commits
```bash
# Soft reset (keeps changes staged)
git reset --soft HEAD~1

# Mixed reset (keeps changes but unstaged)
git reset --mixed HEAD~1

# Hard reset (discard all changes)
git reset --hard HEAD~1

# Reset to a specific commit
git reset --hard <commit-hash>
```

### Stashing
```bash
# Save changes for later
git stash

# Apply stashed changes
git stash apply

# Apply and drop the stash
git stash pop

# View stashes
git stash list

# Show specific stash details
git stash show stash@{0}

# Drop a specific stash
git stash drop stash@{0}

# Clear all stashes
git stash clear
```

### Tagging
```bash
# Create a tag
git tag <tag-name>

# Annotated tag (recommended)
git tag -a <tag-name> -m "Message"

# List tags
git tag

# Push a specific tag
git push origin <tag-name>

# Push all tags
git push --tags

# Delete local tag
git tag -d <tag-name>

# Delete remote tag
git push origin --delete <tag-name>
```

## GitHub Specific

### Fork and Pull Request
1. Fork the repository.
2. Clone your fork locally.
3. Create a new branch for your feature or fix.
4. Push changes to your fork.
5. Create a Pull Request (PR) from your fork to the original repo.

### Issues and Discussions
- **Open Issues** for bugs, feature requests, or tasks.
- **Use Discussions** for general conversations or questions.

## Working with Remotes

```bash
# Set upstream branch
git push --set-upstream origin <branch-name>

# Change URL of remote repository
git remote set-url origin <new-url>
```

## Cherry-Picking
```bash
# Apply changes from a specific commit onto the current branch
git cherry-pick <commit-hash>
```

## Rebase
```bash
# Rebase current branch onto another branch
git rebase <branch-name>

# Continue after conflict resolution
git rebase --continue

# Abort rebase process
git rebase --abort
```

## Squashing Commits
```bash
# Squash commits during interactive rebase
git rebase -i HEAD~n
# (replace "pick" with "squash" for the commits you want to merge)
```

## Helpful Tips

- Always pull before starting new work: `git pull`
- Make small, frequent commits.
- Use descriptive commit messages.
- Keep your `main` (or `master`) branch clean.
- Practice safe branching: create a new branch for each feature/fix.
- Regularly prune deleted branches from remote: `git fetch --prune`

---

## Common Problems

### Authentication Failed
- Update your Git credentials or use SSH keys.

### Merge Conflicts
- Manually fix conflicting files.
- Stage and commit the resolved files.

### Detached HEAD
- Checkout a branch: `git checkout <branch-name>`

### Accidentally Committed to Wrong Branch
- Create new branch from current state: `git checkout -b <new-branch-name>`
- Reset the wrong branch: `git reset --hard origin/<branch-name>`

---

## Resources

- [Official Git Documentation](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com/en)

---

Happy Coding! 🚀
