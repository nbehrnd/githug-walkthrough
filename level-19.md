
# Level 19 commit_amend

> The 'README' file has been committed, but it looks like the file
> 'forgotten_file.rb' was missing from the commit. Add the file and amend your
> previous commit to include it.

The solution is to add the forgotten file to the staging area with `git add`
and then append it to the last commit by `git commit` with the `--amend`
parameter:

```shell
git commit --amend
git commit --amend -m "new message"
git commit --amend -C HEAD
```

The first command brings up an editor for you to edit the commit message. The
second command replaces the original commit message with "new message". The
third command uses the original commit message directly, where `-C` reuses the
already commited message and `HEAD` refers to the most recent commit, i.e.
equivalent to reuse the most recent commit message.

The screen for level 19 is shown below:

![level-19 commit_amend](images/level-19-commit-amend.png)
