
# Level 31 branch

> To work on a piece of code that has the potential to break things, create the branch test_code.

The next 10 levels are all about branches.

A safe development should not affect the mainline currently used "in production": you create a branch based on the mainline, then apply and test changes in the feature branch. Only eventually you should merge the branch into the mainline. In fact, it is common to work on a local branch because in a team, you and your partners share the mainline.

The common commands for branching are as follows:

```shell
git branch branch-name
git branch
```

The first statement is used to create a branch where `branch-name` is the name of the branch you want to create. The second command lists all the branches.

The level 31 pass screen is as follows:

![level-31 branch](images/level-31-branch.png)
