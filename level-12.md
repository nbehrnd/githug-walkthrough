
# Level 12 rm_cached

> A file has accidentally been added to your staging area, find out which file and remove it from the staging area. \*NOTE\* Do not remove the file from the file system, only from git.
> 
> Do not remove the file from the file system, only from git. > A file was accidentally added to your staging area, find out which file and remove it from the staging area. \*Note\* You don't remove the file from the file system, only from git.

Sometimes the files we add to the staging area with the `git add` command contain files that should not have been added, so if you want to undo the addition, you have to do the reverse of `git add`. If you want to undo an addition, you have to do the inverse of `git add`. Git is a real tool.

Undoing a staging area addition is still done with `git rm`, but with a `-cached` parameter, as shown below:

``
$ git rm --cached your-file
```

The level 12 pass screen looks like this:

! [level-12 rm_cached](images/level-12-rm-cached.png)
