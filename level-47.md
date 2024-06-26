
# Level 47 merge_squash

> Merge all commits from the long-featured-branch as a single commit.
> 
> Merge the branch named long-feature-branch into the trunk by merging multiple commits from the branch into a single commit on the trunk.

In level 38 we had learned about ``merge`` merge, which has the syntax:

```
$ git merge branch-name
```

If the branch has been committed multiple times, then after merging with the above statement, the logs of the trunk will also show multiple commits. To conform to this level, merge multiple commits on a branch into a single commit on the trunk, add a ```squash``` parameter, as follows:

```
$ git merge branch-name --squash
```

Without the ```squash``` parameter, the system will silently do a ```commit``` after the merge, and with the ```squash``` parameter, it will not automatically ```commit```, and you will need to manually execute the ```commit``` command with a commit note.

The level 47 pass screen is as follows:

! [level-47 merge_squash](images/level-47-merge-squash.png)
