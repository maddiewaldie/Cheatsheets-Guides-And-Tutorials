# Github Commands

## Table of Contents

1. [User Setup](#User-Setup)
2. [Repo Setup](#Repo-Setup)
3. [Stage & Snapshot](#Stage-&-Snapshot)
4. [Branch & Merge](#Branch-&-Merge)
5. [Inspect & Compare](#Inspect-&-Compare)
6. [Rewrite History](#Rewrite-History)
7. [Temporary Commits](#Temporary-Commits)
8. [Tracking Path Changes](#Tracking-Path-Changes)
9. [Share & Update](#Share-&-Update)

## User Setup

Set a name that is identifiable for credit when review version history.

    git config --global user.name “[firstname lastname]”

Set an email address that will be associated with each history marker.

    git config --global user.email “[valid-email]”

Set automatic command line coloring for Git for easy reviewing.

    git config --global color.ui auto

## Repo Setup

Initialize an existing directory as a Git repository.

    git init

Retrieve an entire repository from a hosted location via URL.

    git clone [url]

## Stage & Snapshot

Show modified files in working directory, staged for your next commit.

    git status

Add a file as it looks now to your next commit (stage).

    git add [file]

Unstage a file, while retaining the changes in working directory.

    git reset [file]

See what the differences are in files that are changed but not staged.

    git diff

See what the differences are in files that are staged but not yet committed.

    git diff --staged

Commit your staged content as a new commit snapshot.

    git commit -m “[descriptive message]”

## Branch & Merge

List your branches. Note: A * will appear next to the currently active branch.

    git branch

Create a new branch at the current commit.

    git branch [branch-name]

Switch to another branch and check it out into your working directory.

    git checkout

Merge the specified branch’s history into the current one.

    git merge [branch]

Show all commits in the current branch’s history.

    git log

## Inspect & Compare

Show the commit history for the currently active branch.

    git log

Show the commits on branchA that are not on branchB.

    git log branchB..branchA

Show the commits that changed file, even across renames.

    git log --follow [file]

Shows content differences between two branches.

    git diff branchB...branchA

Show any object in Git in human-readable format.

    git show [SHA]

## Rewrite History

Apply any commits of current branch ahead of specified one.

    git rebase [branch]

Clear staging area, rewrite working tree from specified commit.

    git reset --hard [commit]

## Temporary Commits

Save modified and staged changes.

    git stash

List stack-order of stashed file changes.

    git stash list

Write working from top of stash stack.

    git stash pop

Discard the changes from top of stash stack.

    git stash drop

## Tracking Path Changes

Delete the file from project and stage the removal for commit.

    git rm [file]

Change an existing file path and stage the move.

    git mv [existing-path] [new-path]

Show all commit logs with indication of any paths that moved.

    git log --stat -M

## Share & Update

Add a git URL as an alias.

    git remote add [alias] [url]

Fetch down all the branches from that Git remote.

    git fetch [alias]

Merge a remote branch into your current branch to bring it up to date.

    git merge [alias]/[branch]

Transmit local branch commits to the remote repository branch.

    git push [alias] [branch]

Fetch and merge any commits from the tracking remote branch.

    git pull
