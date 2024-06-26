
# Level 53 restore

> You decided to delete your latest commit by running `git reset --hard HEAD^`. (Not a smart thing to do.) You then change your mind, and want that commit back.  (Not a smart thing to do.) You then change your mind, and want that commit back. Restore the deleted commit.
>Restore the deleted commit. 
> You decide to delete the last commit with `git reset --hard HEAD^`. (Not a smart thing to do.) You then change your mind, and want that commit back. Please restore the deleted commit.

Let's start by checking the commit log and find that there were 2 commits:

``
$ git log --pretty=oneline
1dc1ecdd071fd2a5baa664dce42a48b13d40cdae First commit
e586f55fde799d2b390d8a74d771db75279841f3 Initial commit
``

Look at the operation log again:

```
$ git reflog
1dc1ecd HEAD@{0}: reset: moving to HEAD^ f766953 HEAD@{0}: reset: move to HEAD
f766953 HEAD@{1}: commit: Restore this commit
1dc1ecd HEAD@{2}: commit: First commit
e586f55 HEAD@{3}: commit (initial): Initial commit
```

Oh, and there was a third commit, but it was removed by `git reset --hard HEAD^`. `git reset --hard HEAD^` is used to remove the last commit and return the workspace to the state it was in when the last commit was made, as you can also see by looking closely at the log above, where "HEAD@{2}" and "HEAD@{0}" have the same hash value.

If we want to undo this command itself, that is, restore to the state before executing this command, we can use the following command form:

``
$ git reset --hard hash-code
```

The hash-code in the above command is the hash of the commit you're reverting to. After running this command, a commit log will be added to the commit log, and a "reset: moving to hash-code" log will automatically be added to the operations log.

The level 53 pass screen is as follows:

! [level 53 restore](images/level-53-restore.png)
