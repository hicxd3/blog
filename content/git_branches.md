+++
date = '2024-10-03T18:53:24+03:00'
title = 'Git Branch Commands'
categories = [ "git" ]
+++

Working with branches is a common task in Git version control. You’ll often need to create, switch, delete, and merge branches.

### Create a branch

This command creates a new branch and immediately switches to it:

```bash
git switch --create [branch-name]
```

### Switch between branches

This command switches to an existing branch.  
Alternatively, you can use `git checkout` to both create and switch branches.

```bash
git switch [branch-name]
```

### List all local branches

```bash
git branch
```

### Rename a branch

```bash
git branch -m [old-branch-name] [new-branch-name]
```

### Push a branch to GitHub

```bash
git push origin [branch-name]
```

### Delete a local branch

```bash
git branch --delete [branch-name]
```

### Delete a remote branch on GitHub

```bash
git push --delete origin [branch-name]
```

### Merge a branch

```bash
git merge [branch-name]
```

### Rebase commits

This command reapplies commits from your current branch onto another branch:

```bash
git rebase [branch-name]
```

### Cherry-pick commits

Use this to apply specific commits from another branch.  
Often used with `git merge` and `git rebase` to maintain a linear commit history.

```bash
git cherry-pick
```
