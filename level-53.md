
# Level 53 restore

> You decided to delete your latest commit by running `git reset --hard HEAD^`
(not a smart thing to do). Now you changed your mind and want that commit back.
Restore the deleted commit.

Let's start to inspect the commit log; there are 2 commits:

```shell
$ git log --pretty=oneline
1dc1ecdd071fd2a5baa664dce42a48b13d40cdae First commit
e586f55fde799d2b390d8a74d771db75279841f3 Initial commit
```

Look at the operation log again:

```shell
$ git reflog
1dc1ecd HEAD@{0}: reset: moving to HEAD^ f766953 HEAD@{0}: reset: move to HEAD
f766953 HEAD@{1}: commit: Restore this commit
1dc1ecd HEAD@{2}: commit: First commit
e586f55 HEAD@{3}: commit (initial): Initial commit
```

Oh, there was a third commit, but it was removed by `git reset --hard HEAD^` to
revert the state of the workspace. Note `HEAD@{2}` and `HEAD@{0}` actually
share a hash value.

If we want to undo this command itself, that is, restore to the state before
executing this command, we can use the following command form:

```shell
git reset --hard hash-code
```

The `hash-code` in the above is the hash of the commit you're reverting to.
After running this command, Git adds a commit with the message "Restore this
commit" to the commit log, and an other "reset: moving to hash-code" to the
operations log.

The level 53 pass screen is as follows:

![level 53 restore](images/level-53-restore.png)
