# Mission 6 — Git and GitHub

## 1. Task / objective
Understand version control, stage and commit changes, create a branch, open a Pull Request and explain the collaboration workflow.

## 2. Work completed
I checked the repository status and history, created a branch named `update-about`, added a "My Learning" section to the root README on that branch, committed and pushed it, and opened a Pull Request from `update-about` into `main`. I also wrote a Git command glossary.

### Task 6.1 — Basic Git workflow

| Git operation | What it does in my own words |
|---------------|------------------------------|
| Check repository status (`git status`) | Shows which files are changed, which are staged for the next commit and which are not tracked yet |
| Stage selected changes (`git add <file>`) | Picks the changes I want to include in my next commit |
| Create a commit (`git commit -m "..."`) | Saves a snapshot of the staged changes with a message describing them |
| View commit history (`git log --oneline`) | Shows the list of earlier commits with their short IDs and messages |

**Staging vs committing:** Staging means choosing which changes will go into the next save. Committing is the actual save that records those staged changes in the history. I can stage several files first and then commit them together as one snapshot.

### Task 6.2 — Branch `update-about`
I created the branch with `git switch -c update-about`, added a "My Learning" section to the root `README.md`, checked `git status`, staged the file with `git add README.md`, committed it with the message "Add My Learning section to root README", and published the branch with `git push -u origin update-about`.

### Task 6.3 — Pull Request
- **Pull Request:** `update-about` into `main`
- **Description I wrote:** Adds a My Learning section to the root README.
- **PR status:** CHOOSE ONE: "Merged, because my instructor asked me to merge it. After merging I ran `git switch main` and `git pull origin main`." OR "Open and not merged, because my instructor did not ask me to merge it."

**What a branch is:** A branch is a separate line of work in a repository. I can change files on a branch without touching `main`, so the main version stays safe.

**What a Pull Request is:** A Pull Request is a request on GitHub to bring the changes from one branch into another. It lets other people review the changes and discuss them before they are merged.

**Why they are useful in teamwork:** When many people work on the same project, each person can work on their own branch without breaking others' work. The Pull Request lets the team check changes first, so mistakes are caught before they reach `main`.

### Task 6.4 — Git command glossary

| Git operation | Command | One-line explanation |
|---------------|---------|----------------------|
| Initialise a repository | `git init` | Starts Git tracking in a folder |
| Check status | `git status` | Shows which files are changed, staged or untracked |
| Stage changes | `git add` | Chooses changes for the next commit |
| Commit changes | `git commit` | Saves the staged changes as a snapshot with a message |
| View history | `git log` | Lists the earlier commits |
| Create or list branches | `git branch` or `git switch -c <name>` | Lists branches, or creates a new one and moves to it |
| Switch branches | `git switch <name>` | Moves to a different branch |
| Publish changes | `git push` | Uploads my commits to GitHub |
| Retrieve remote changes | `git pull` | Downloads new changes from GitHub and updates my local branch |

## 3. Commands / tools used
- `git status`: checks the state of my files.
- `git add`: stages changes.
- `git commit`: saves a snapshot.
- `git log --oneline`: shows history.
- `git switch -c update-about`: creates and moves to a new branch.
- `git push -u origin update-about`: publishes the branch to GitHub.
- `git switch main` and `git pull origin main`: return to main and fetch the latest changes (used after merging).
- Tools: Terminal (zsh), VS Code, GitHub website (to create the Pull Request).

## 4. My understanding
Git is a version control system that records changes so I can look back at earlier versions and work safely. Adding (staging) and committing are two separate steps: add selects, commit saves. A branch lets me try changes in a separate space, and a Pull Request lets me ask to merge those changes into `main` after review. GitHub hosts the repository online so people can collaborate. This matters because it keeps teamwork organised and protects the main version of a project.

## 5. Difficulties faced
No major difficulties.

## 6. How I resolved them
Not applicable.

## 7. Evidence / files
- Root `README.md` (contains the "My Learning" section)
- Branch `update-about` and its Pull Request, visible on GitHub
- `mission-06-git-github/README.md`

## 8. Commit details
Commit messages used: "Add My Learning section to root README" (on branch `update-about`) and "Complete Git and GitHub collaboration mission" (this mission's README).
I pushed these commits to GitHub and checked that the branch and Pull Request are visible.