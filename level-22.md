
# Level 22 reset_soft

> You committed too soon. Now you want to undo the last commit, while keeping the index.
>Now you want to undo the last commit, while keeping the index. 
> You committed too soon. Now you want to undo the last commit, while keeping the index.

This is another undo operation, undoing the last ``git commit`` command, with the following syntax:

```
$ git reset --soft HEAD^
```

The `git reset` command has a number of complex parameters, which I won't go into here, including `--soft HEAD^`, which means that the last commit is undone and that neither the staging area nor the working directory is affected.

The `git commit --amend` command in level 19 is the equivalent of `git reset --soft` followed by `git commit`.

When you look at the logs after executing this command, you will see that the last commit has disappeared.

The level 22 pass screen looks like this:

! [level-22 reset_soft](images/level-22-reset-soft.png)
