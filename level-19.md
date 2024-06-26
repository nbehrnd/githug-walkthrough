
# Level 19 commit_amend

> The 'README' file has been committed, but it looks like the file 'forgotten_file.rb' was missing from the commit. Add the file and amend your previous commit to include it.
>Add the file and amend your previous commit to include it. 
> The file 'README' has been committed, but it looks like the file 'forgotten_file.rb' was missing from the commit. Amend your previous commit to include it.

The solution is to add the forgotten file to the staging area with ``git add`` and then append it to the last commit with ``git commit`` with the ``--amend`` parameter, with the following syntax:

```
$ git commit --amend
$ git commit --amend -m "new message"
$ git commit --amend -C HEAD
```

The first command brings up an editor for you to edit the commit note; the second command replaces the original commit note with "new message"; and the third command uses the original commit note directly, where `-C` means use the note that was already committed and `HEAD` means the most recent commit, which together means use the most recent commit note.

The screen for level 19 is shown below:

! [level-19 commit_amend](images/level-19-commit-amend.png)
