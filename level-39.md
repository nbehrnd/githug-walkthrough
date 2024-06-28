
# Level 39 fetch

> Looks like a new branch was pushed into our remote repository. Get the
changes without merging them with the local repository.

In level 26 we used `git pull` to pull updates from a remote repository into
the local repository. This command actually implies two consecutive actions,
`git fetch` and `git merge`. If you just want to grab the data without intent
to merge, you can't use `git pull`. To constrain Git to the first action, use
`git fetch` with the following syntax:

```shell
git fetch
git branch -r
git log remote-name/branch-name
```

The first statement grabs the data from the remote repository locally, but does
not merge it into the local branch. The second statement provides a list of the
remote branches. The third statement looks at the log of the remote branch and
here requires both the repository name and the remote branch name as arguments.

Level 39 passes with the following screen:

![level-39 fetch](images/level-39-fetch.png)
