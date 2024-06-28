
# Level 40 rebase

> We are using a git rebase workflow and the feature branch is ready to go into
master. Let's rebase the feature branch onto our master branch.

We used the `git rebase` command once in level 28, so let's go over it again.

Both `git rebase` and `git merge` are used for merging, and they have their
advantages and disadvantages. Hence, some teams will agree that merging can
only be done with either `git merge`, or `git rebase`. If you agree that you
can only merge with `git rebase`, this is referred to as a "git rebase
workflow".

When merging branches with `git rebase`, the merged logs are not organized by
the commit time of each branch, but rather, the logs of one branch are arranged
on top of the logs of the other branch. Thus, despite they were developed in
parallel, and commits were staggered during the development process,
eventually, they look as if they were developed in sequential order.

Take this question as an example. Here, branch `master` is the main thread, and
branch `feature` is derived from `master`. After that, `master` commits once
(commit message "add content"), while `feature` also commits (commit message
"add feature") as illustrated below:

```
init commit ---- ---- add content (on master)
     \
      + ---- add feature (on feature)
```

After a rebase on branch on `master`, i.e.

```shell
git checkout master
git rebase feature
```

the logs of `master` will read commit "add content" on top of "add feature" i.e.

```
init commit ---- add feature ---- add content
```

On the other hand, after a rebase on branch `feature` i.e.

```shell
git checkout feature
git rebase master
```

the commit "add feature" will be on top of "add content":

```
init commit ---- add content ---- add feature
```

The level 40 pass screen looks like this:

![level-40 rebase](images/level-40-rebase.png)
