
# Short Cuts

## Python environment

- Activate: conda activate <environment_name>
- Check what environment is active: conda info --envs OR conda env list

## Git commands

### Repository status and inspection
- `git status` — show the current branch and the state of the working tree and staging area
- `git diff` — show unstaged changes in the working tree
- `git diff --staged` — show changes that have been staged for the next commit
- `git diff <branch1>..<branch2>` — compare two branches or references
- `git log --oneline --decorate --graph --all` — display the commit history as a compact graph

### Staging and committing
- `git add <file>` — stage a file for the next commit
- `git add .` — stage all current changes in the working directory
- `git commit -m "<message>"` — create a commit with a message
- `git commit` — create a commit and open the configured editor for the commit message
- Commit log: git log --oneline --decorate --graph --all

### Restoring and unstaging
- `git restore <file>` — discard unstaged changes to a file, stage area -> working tree: 
   Make my working-tree file look like the staged version
- `git restore --staged <file>` — remove a file from the staging area without discarding its changes. Head-> staging area: Make my staged file look like the HEAD version. It cghanges the staging area, but preserves your working-tree work.

### Moving and renaming
- `git mv <old_name> <new_name>` — move or rename a tracked file

### Branching
- `git branch` — list branches
- `git branch <name>` — create a branch
- `git switch <name>` — switch branches
- `git switch -c <branch_name>` — create and switch to a new branch
- `git branch -d <branch>` — safely delete a merged local branch
- `git branch -r` — list remote branches
- `git branch -a` — list all branches (local and remote)
- `git branch -vv` — list local branches and show their upstream/tracking relationships

### Mergings
- `git merge <branch>` — merge another branch into the current branch
- `git merge origin/main` — merge the fetched state of remote `main` into the current branch

### Remote repositories
- `git remote` — list configured remote names
- `git remote -v` — list remote repositories
- `git remote add <name> <url>` — add a remote repository

### Pushing to a remote repository
-u is short for: --set-upstream
- `git push -u <remote> <branch>` — push a branch and establish its upstream tracking relationship
- `git push` — push the current branch using its configured upstream
- `git push origin main` — push the local `main` branch to the remote named `origin`
- `git push origin --delete <branch>` — delete a remote branch

### Pulling from a remote repository
- `git fetch` — download information and commits from the remote without integrating them into the current local branch
- `git pull` — fetch remote changes and integrate them into the current branch
- `git diff main..origin/main` — compare local `main` with the fetched state of remote `main`

# What a GitHub Pull Request Does

A **GitHub pull request (PR)** is a way to propose changes you've made on a branch and request that someone review and merge those changes into another branch (usually the main branch).

In short, a PR:

1. **Proposes changes** — You push commits from a feature branch and open a PR to show what you changed, line by line.
2. **Invites review** — Teammates can comment on the code, suggest edits, and approve (or request changes) before anything merges.
3. **Runs checks** — CI tests, linting, and other automated checks can run automatically on the PR before it's allowed to merge.
4. **Merges the work** — Once approved and checks pass, the PR merges your branch's commits into the target branch, integrating the changes into the project.

Think of it as a controlled, reviewable handoff: *"I've finished this work on a separate branch — please review it and pull it into the main project."*


### Upcoming
- rebase, reset, revert, cherry-pick, stash and more advanced commands


