+++
hidden = true
date = '2025-09-13T18:53:24+03:00'
title = 'Full list of Git commands: branches, commits, cherry-pick, rebase, stash and more'
draft = true
+++

## Git Cheatsheet ^-^

This is a complete guide with 100 Git commands.  
From basics to advanced workflows — everything you need to feel like a Git Ninja 🥷.

### Basics

git init — create a new repository

git clone <url> — clone a project

git status — check current changes

git add <file> — add a file to staging

git add . — add all files

git commit -m "msg" — commit changes

git log — full commit history

git log --oneline — short history view

git show <hash> — details of a commit

git diff — show unstaged changes

### Branches

git branch — list all branches

git branch <name> — create a branch

git checkout <name> — switch to a branch

git checkout -b <name> — create and switch

git switch <name> — switch branch (modern way)

git switch -c <name> — create and switch (modern way)

git merge <name> — merge a branch

git rebase <name> — reapply commits on top

git branch -d <name> — delete branch

git branch -D <name> — force delete branch

### Remote Repositories

git remote -v — show all remotes

git remote add origin <url> — add a remote

git push origin <branch> — push branch to remote

git push -u origin <branch> — push and set upstream

git pull origin <branch> — pull from remote

git fetch — fetch changes without merging

git remote remove origin — remove a remote

git remote rename old new — rename a remote

git remote set-url origin <url> — change remote URL

git push origin --delete <branch> — delete remote branch

### Managing Changes

git diff --staged — compare staged changes

git reset <file> — unstage a file

git reset --hard <hash> — reset to commit (delete changes)

git reset --soft <hash> — reset but keep changes

git revert <hash> — undo commit by new commit

git checkout -- <file> — restore file

git restore <file> — modern restore file

git restore --staged <file> — unstage file (modern way)

git commit --amend — edit last commit

git commit --amend -m "msg" — edit commit message

### Stash

git stash — save changes temporarily

git stash list — list all stashes

git stash pop — restore last stash and delete it

git stash apply stash@{n} — apply specific stash

git stash drop stash@{n} — delete stash

git stash clear — delete all stashes

git stash save "msg" — save stash with message

git stash show — show stash changes

git stash branch <name> — create branch from stash

git stash show -p — show patch of stash

### Cherry-pick & Tags

git cherry-pick <hash> — apply commit from another branch

git cherry-pick -n <hash> — apply without commit

git cherry-pick --continue — continue after conflict

git cherry-pick --abort — stop cherry-pick

git tag <name> — create tag

git tag -a <name> -m "msg" — annotated tag

git push origin <tag> — push tag to remote

git push origin --tags — push all tags

git tag -d <name> — delete tag locally

git push origin :refs/tags/<name> — delete tag remotely

### Logs and History

git log --graph --oneline --all — graph view

git log --stat — show changes in each commit

git log --pretty=oneline — compact view

git log --pretty=format:"%h - %an, %ar : %s" — custom log format

git shortlog -sn — contributors list

git reflog — complete action history

git blame <file> — show who edited each line

git annotate <file> — similar to blame

git show-branch — show branch history

git whatchanged — show commits and changes

### Advanced

git bisect start — start binary search for bug

git bisect bad — mark commit as bad

git bisect good — mark commit as good

git bisect reset — finish bisect

git clean -fd — delete untracked files

git clean -n — preview untracked delete

git submodule add <url> — add submodule

git submodule update --init — initialize submodules

git submodule foreach git pull — update submodules

git archive --format=zip HEAD > file.zip — export project

### Collaboration & Workflow

git fetch --all — fetch all branches

git pull --rebase — pull with rebase

git push --force — force push

git push --force-with-lease — safe force push

git rebase -i HEAD~n — interactive rebase

git merge --squash <branch> — squash merge

git rebase --abort — abort rebase

git rebase --continue — continue rebase

git merge --abort — abort merge

git cherry — show unmerged commits

### Misc

git help <command> — show help

git config --list — show config

git config --global user.name "Name" — set username

git config --global user.email "Email" — set email

git config core.editor "code --wait" — set editor

git init --bare — create bare repo

git archive <branch> — archive branch

git fsck — check integrity

git gc — clean up repository

gitk — open Git GUI

Key Points ^-^

100 commands cover 90% of daily and advanced Git usage

Don’t memorize, use this as a reference

Git is about save points, branches and history merging