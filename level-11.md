
# Level 11 rm

> A file has been removed from the working tree, but not from the repository.
> Identify this file and remove it.

If a file is useless and you want to delete it, don't use the `rm` command.
Instead, use the Git-wrapped `git rm` command -- otherwise the Git repository
won't know that you deleted the file and won't be able to track changes to the
file.

The level 11 pass screen looks like this:

![level-11 rm](images/level-11-rm.png)
