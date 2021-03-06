---
title: Setup Git shortcuts (aliases)
---

I like to type short commands for commands I use very often. If you use Git, then you probably use that command a lot.

I have some shortcuts setup for git like this:

 * `git co` for `git checkout`
 * `git st` for `git status` (not stash)
 * `git ci` for `git commit`

On Mac you can edit your `.gitconfig` file by typing `nano ~/.gitconfig` and add the following:

```
[alias]
  co = checkout
  ci = commit
  st = status
  br = branch
  hist = log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short
  type = cat-file -t
  dump = cat-file -p
```

If you even want the `git` command shorter, then you can make an alias in your ~/.bash_profile file by typing `nano ~/.bash_profile` and adding the following:

```bash
alias g='git'
```

Now you can use git like this: `g co -b feature/new-branch` (creates a new branch).

Source: [http://githowto.com/aliases](http://githowto.com/aliases).
