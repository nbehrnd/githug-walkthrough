
# Level 43 cherry-pick

> Your new feature isn't worth the time and you're going to delete it. But it
> has one commit that fills in the `README` file, and you want this commit to be
> on the master as well.

After multiple commits in a feature branch, you might not want to merge all
commits into the mainline. If you want to commit only one specific commit into
the mainline, then you can use the following command:

```shell
git cherry-pick hash-code
```

where `hash-code` is the HASH value of the specific commit. `cherry-pick`
translates to cherry picking. Think of a branch as a tree, where multiple
commits make the tree full of fruits; so the `cherry-pick` command is to pick
one of the fruits.

The pass screen for level 43 looks like this:

![Level 43 cherry-pick](images/level-43-cherry-pick.png)
