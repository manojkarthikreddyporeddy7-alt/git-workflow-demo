# Git Workflow Demo

This project demonstrates a practical Git workflow using branches, commits, merge conflicts, merging, rebasing, and GitHub.

## Week 1 Goals

- Feature branches
- Pull requests
- Merge conflict resolution
- Git rebase

## Project Details

This project demonstrates a practical Git workflow.

The workflow includes:

- Creating feature branches
- Making changes independently
- Committing changes
- Merging branches
- Resolving merge conflicts
- Rebasing branches

## Feature Branches

Two feature branches were created:

- `feature/add-project-details`
- `feature/rebase-demo`

Feature branches allow developers to work on changes independently without directly modifying the main branch.

## Merge Conflict

A merge conflict was intentionally created by modifying the same line differently on two branches.

The `main` branch contained:

"This project demonstrates a Git workflow from the main branch."

The feature branch contained:

"This project demonstrates a Git workflow from the feature branch."

When the feature branch was merged into `main`, Git detected a conflict in `README.md`.

The conflict was resolved manually by combining the changes:

"This project demonstrates a Git workflow from the main and feature branches."

The resolved file was staged and committed using:

git add README.md

git commit -m "Resolve merge conflict"

## Git Rebase

A separate branch was created for the rebase demonstration:

git switch -c feature/rebase-demo

A feature commit was created:

git add README.md

git commit -m "Add rebase demo"

A new commit was then added to the `main` branch.

The feature branch was rebased onto the updated `main` branch using:

git rebase main

A conflict occurred during the rebase and was resolved manually.

After resolving the conflict:

git add README.md

git rebase --continue

The rebase completed successfully.

The original feature commit:

2ac46a8 Add rebase demo

was replayed as a new commit:

e687991 Add rebase demo

This demonstrates that Git rebase creates a new commit with a different commit ID.

## Git Commands Used

Initialize repository:

git init

Create a branch:

git switch -c feature/branch-name

Switch branches:

git switch main

Check status:

git status

Stage changes:

git add README.md

Create a commit:

git commit -m "Commit message"

Merge a branch:

git merge feature/branch-name

Rebase a branch:

git rebase main

Continue a rebase:

git add README.md

git rebase --continue

View Git history:

git log --oneline --decorate --graph --all

View all branches:

git branch -a

Push a branch to GitHub:

git push -u origin branch-name

## Branches in This Project

| Branch | Purpose |
|---|---|
| `main` | Main project branch |
| `feature/add-project-details` | Feature branch and merge conflict demonstration |
| `feature/rebase-demo` | Rebase demonstration |

## What I Learned

Through this Git workflow exercise, I learned:

- How Git repositories work
- How to create and switch branches
- How feature branches are used
- How to create commits
- How merge conflicts occur
- How to identify conflict markers
- How to resolve merge conflicts manually
- How to merge branches
- How Git rebase works
- How to resolve rebase conflicts
- How rebase changes commit history
- How to push branches to GitHub
- How to view Git branch and commit history

## GitHub Repository

https://github.com/manojkarthikreddyporeddy7-alt/git-workflow-demo

## Final Git Workflow

Initial Commit
      |
      +-----------------------------+
      |                             |
     main                    feature/add-project-details
      |                             |
 Main branch change          Feature branch changes
      |                             |
      +-------- Merge Conflict -----+
                    |
             Conflict Resolution
                    |
                   main
                    |
              Main Branch Update
                    |
             feature/rebase-demo
                    |
                  Rebase
                    |
             Rebase Conflict
                    |
             Conflict Resolution
                    |
             Successful Rebase

## Conclusion

This project demonstrates a practical Git workflow involving feature branches, commits, merge conflicts, conflict resolution, merging, rebasing, and GitHub remote branches.