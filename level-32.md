
# Level 32 checkout

> Create and switch to a new branch called my_branch. You will need to create a branch like you did in the previous level.

In the previous level, we created a branch, but didn't switched to the new branch. If you look closely, you'll see that the `git branch` statement results in a `*` sign in front of `master`, which indicates the branch you're currently on.

The statement to switch branches are:

```shell
git checkout branch-name
git checkout -b branch-name
git checkout -b -
```

The first statement is used to switch to the specified branch already existing. The second statement adds the `-b` parameter to create a branch and switch to that new branch; it is equivalent to executing `git branch branch-name` and `git checkout branch-name`. The third statement is used to switch to the branch just previously used, which is handy when you're constantly switching back and forth between two branches.

I don't know if you remember, but we used this command in level 23:

```shell
git checkout your-file
```

What it does is undo changes to a file. Although formally this command is very similar to the one in this level, the function is completely different because the arguments have different meanings, one is a filename and the other is a branch name.

The pass screen for level 32 is as follows:

![level-32 checkout](images/level-32-checkout.png)
