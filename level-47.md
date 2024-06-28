
# Level 47 merge_squash

> Merge all commits from the long-featured-branch as a single commit.

In level 38 we had learned about a merge by `merge` with the syntax:

```shell
git merge branch-name
```

If a feature branch contains multiple commits, the logs of the trunk will
equally show multiple commits after a merge with the above statement because
Git implicitly launches a `commit` after the merge. The `squash`option, i.e.

```shell
git merge branch-name --squash
```

prevents such an automatic `commit` and indeed, the commiter is required to
issue an explicit `commit` (with an optional commit message).

The level 47 pass screen is as follows:

![level-47 merge_squash](images/level-47-merge-squash.png)
