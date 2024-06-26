
# Level 39 fetch

> Looks like a new branch was pushed into our remote repository. Get the changes without merging them with the local repository 
Get the changes without merging them with the local repository. > 
> Looks like a new branch was pushed into our remote repository. Get the changes without merging them with the local repository.

In level 26 we used ```git pull``` to pull updates from the remote repository to the local repository, and this command actually implies two consecutive actions, ``git fetch``` and ``git merge``. If you're just grabbing data and not merging it, you can't use ``git pull``, but just use the first action, ``git fetch``, with the following syntax:

```
$ git fetch
$ git branch -r
$ git log remote-name/branch-name
```

The first statement grabs the data from the remote repository locally, but does not merge it into the local branch; the second statement looks at the list of remote branches; if there is a new branch in the remote repository, you can find out the name of the new branch if you look at it after ``git fetch`` and then use ``git branch -r``, which in this case is called 'new_branch'; and the third statement looks at the log of the remote branch, which is much more useful than looking at the local log. statement is used to view the log of the remote branch, which takes two more arguments than the ``git log`` statement to view the local log: the remote repository name and the remote branch name.

Level 39 passes with the following screen:

! [level-39 fetch](images/level-39-fetch.png)
