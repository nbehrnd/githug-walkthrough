
# Level 38 merge

> We have a file in the branch 'feature'. Let's merge it with the master branch.

Once we have finished modifying and testing in the branch, we can merge the
branch to the master, which is done with the command:

```shell
git merge branch-name
```

Before executing this command, switch to the mainline branch (often called
`main`, or `master`) and take the name of the branch you want to merge into as
an argument.
After the merge, the contents of files modified on the branch will be reflected
on the mainline, and the branch's modification log will be added to the log.

If the mainline and the feature branch to merge describe the same line of code
differently, Git will indicate a merge conflict. Which version of the local
source code should now be retained? We will learn how to resolve such a
discrepancy in level 54.

The level 38 pass screen is as follows:

![Level 38 merge](images/level-38-merge.png)
