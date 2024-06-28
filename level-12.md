
# Level 12 rm_cached

> A file has accidentally been added to your staging area. Identify and remove it from the staging area. *NOTE* Do not remove the file from the file system, only from git.

Sometimes the files we add to the staging area with the `git add` command contain files that should not have been added. If you want to undo the addition, you have to do the reverse of `git add`. The undo with `git rm` now deploys the `--cached` parameter:

```shell
git rm --cached your-file
```

The level 12 pass screen looks like this:

![level-12 rm_cached](images/level-12-rm-cached.png)
