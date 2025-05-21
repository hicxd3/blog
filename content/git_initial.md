
+++
date = '2024-10-03T18:53:24+03:00'
title = 'Initial Git Setup'
categories = [ "git" ]
+++

### Set User Name

Specifies the user name that will be used for commits. Use Latin characters. If the name is one word, quotes are optional.

```bash
git config --global user.name "Cxd3"
```

### Set Email

Specifies the user's email address. Use the same address registered with GitHub.

```bash
git config --global user.email "hi@cxd3.com"
```

### View Configured Settings

You can check settings in the config file, but this method is faster.

```bash
git config --list
```

### Working with a Repository

#### Create a New Repository

Initialize git in a local folder:

```bash
git init
```

#### Clone a Repository from GitHub

The project will be cloned into the current directory.

```bash
git clone [repository link]
```

#### Link Local Repo with GitHub

```bash
git remote add origin [repository link]
```

### Working with Changes

#### Pull Changes

This command fetches all updates from the GitHub project.

```bash
git pull
```

#### Check File Status

Shows which files were added, modified, or deleted — excluding committed ones.

```bash
git status
```

Example output:

```bash
➜  cxd3 git:(main) ✗ git status
On branch main
Your branch is up to date with 'origin/main'.
```

#### Stage Files

This command stages all changes. To stage a single file, specify the filename instead of a dot.

```bash
git add .
```

#### Commit Changes

This command records the staged changes. No local save occurs until this is done.

```bash
git commit -m "Commit message"
```

#### View Commit History

Shows the commit history. A common option is `--oneline`, which gives a brief view.

```bash
git log
```

#### Push Changes

Sends all committed changes to GitHub.

```bash
git push
```

#### Discard Unstaged Changes

```bash
git restore [file name]
```

#### Discard Staged Changes

```bash
git reset --hard
```

#### Delete a Commit

```bash
git revert [commit hash]
```
