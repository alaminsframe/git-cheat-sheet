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
```

## Branching

### Create and Switch Branches
```bash
# Create new branch
git branch <branch-name>

# Switch to a branch
git checkout <branch-name>

# Create and switch in one command
git checkout -b <branch-name>
```

### Merge and Delete Branches
```bash
# Merge branch into current branch
git merge <branch-name>

# Delete a branch
# (only after merging, to keep things clean)
git branch -d <branch-name>
```

## Remote Repositories

```bash
# Add a remote repository
git remote add origin <repository-url>

# Push a branch to remote
git push -u origin <branch-name>

# View configured remotes
git remote -v
```

## Advanced

### Undo Changes
```bash
# Unstage a file
git reset <file-name>

# Undo local changes (careful, irreversible)
git checkout -- <file-name>
```

### Resetting Commits
```bash
# Soft reset (keeps changes staged)
git reset --soft HEAD~1

# Mixed reset (keeps changes but unstaged)
git reset --mixed HEAD~1

# Hard reset (discard all changes)
git reset --hard HEAD~1
```

### Stashing
```bash
# Save changes for later
git stash

# Apply stashed changes
git stash apply

# View stashes
git stash list
```

### Tagging
```bash
# Create a tag
git tag <tag-name>

# Push tags
git push origin <tag-name>

# Push all tags
git push --tags
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

---

# Helpful Tips

- Always pull before starting new work: `git pull`
- Make small, frequent commits.
- Use descriptive commit messages.
- Keep your `main` (or `master`) branch clean.
- Practice safe branching: create a new branch for each feature/fix.

---

# Common Problems

### Authentication Failed
- Update your Git credentials or use SSH keys.

### Merge Conflicts
- Manually fix conflicting files.
- Stage and commit the resolved files.

### Detached HEAD
- Checkout a branch: `git checkout <branch-name>`

---

# Resources

- [Official Git Documentation](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com/en)

---

Happy Coding! 🚀

