
# Level 21 reset

> There are two files to be committed. The goal was to add each file as a separate commit, however both were added by accident. Unstage the file `to_commit_second.rb` using the reset command (don't commit anything).

This level is very similar to level 12 in that it's all about removing files from the staging area. You can even use the `git rm --cached` command from level 12 to accomplish this task, but if you can do it with what you already know, why do you need to set up a special level for this?

Recall the "Git File Lifecycle" diagram from level 3 (it's a really important diagram, and we recalled it once in level 9). A file in your working directory can have two states: `untracked`, which means it's a new file that didn't exist in the repository before, or `modified`, which means it's a file that already exists in the repository and has been modified.

No matter which state they are in, the command to add them to the staging area is `commit add`, but this command actually contains two possible meanings: adding a file to the repository, or modifying an existing file in the repository.  Hence, the operation of removing a file from the staging area corresponds to two scenarios, one is to remove the *new file* from the staging area, and the other is to remove the *modified file* from the staging area. Level 12 and this level are designed to examine these two scenarios, with Level 12 focusing on the first scenario and this level on the second.

The command to remove a modified file from the staging area is:

```shell
git reset your-file
```

The pass screen for level 21 is as follows:

![level-21 reset](images/level-21-reset.png)
