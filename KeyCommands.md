
# Short Cuts

## Python environment

- Activate: conda activate <environment_name>
- Check what environment is active: conda info --envs OR conda env list

## Git commands


### Branching
- `git branch` — list branches
- `git branch <name>` — create a branch
- `git switch -c <branch_name>` — create and switch to a new branch
- `git switch <name>` — switch branches

### Commiting
- Commit log: git log --oneline --decorate --graph --all

### Mergings
- `git merge <branch>` — merge another branch into the current branch

### Adding a remote repository
- `git remote add <name> <url>` — add a remote repository
- `git remote -v` — list remote repositories

### Pushing to a remote repository
- `git push -u <remote> <branch>` — push changes to a remote repository