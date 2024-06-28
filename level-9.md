
# Level 9 status

> Among the files in this repository, which of them is untracked?

Git manages files in a variety of states. You often need to check the state of a file before deciding what to do or how to do it next. Hence it's as important as the Linux `ls` command, which is the starting point for almost all operations.

The command to check the status of a repository is:

```shell
git status
git status -s
```

The first command indicates viewing in detailed format while the second command provides the information in a compact format. The default detailed format contains the following:

* untracked: Files that are newly created in the repository, or copied into the repository from somewhere else, have a status of "untracked", and they are displayed in red in the "Untracked files" paragraph of the query result.

* modified: Files that have been edited have a status of "modified" and are shown in red in the "Changes not staged for commit" section of the query.

* staged: Files added to the staging area by the `git add` command become "staged" and are displayed in green in the "Changes to be committed" section of the query.

If you're confused by the statuses above, go back to level 3 and take a closer look at the "Git File Lifecycle" diagram.

Levels 9 and 10 test your ability to read the results of a git status query, with level 9 asking you to identify files in untracked status from the results.

The screen for level 9 looks like this:

![level-9 status](images/level-9-status.png)
