
# Level 38 merge

> We have a file in the branch 'feature'; Let's merge it to the master branch.
> 
> We have a file in the branch 'feature'; Let's merge it to the master branch.

Once we have finished modifying and testing in the branch, we can merge the branch to the master, which is done with the command:

``
$ git merge branch-name
```

Before executing this command, switch to the mainline (usually the master branch) and take the name of the branch you want to merge into as an argument.

After the merge, the contents of files modified on the branch will be reflected on the master, and the branch's modification log will be added to the log.

If you encounter a conflict where the mainline and the branch have modified the same line of code, a conflict will occur, and we will learn how to resolve the conflict later in the level.

The level 38 pass screen is as follows:

! [Level 38 merge](images/level-38-merge.png)
