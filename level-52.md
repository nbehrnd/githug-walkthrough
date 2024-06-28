
# Level 52 revert

> You have committed several times but want to undo the middle commit. All
> commits have been pushed, so you can't change existing history.

We've used the `git rebase -i` command to change the history of commits to
cancel one of the multiple commits. But that's only if it hasn't been pushed to
the server yet. If it has, you can't change the existing history. You have to
figure out another way to do it.

Git provides the `revert` tool as the inverse of a commit. For example, if a
commit creates a new file, then Git creates an other commit to delete that
file. The syntax is as follows:

```shell
git revert hash-code
git revert hash-code --no-edit
```

where `hash-code` is the hash of the commit you want to cancel. The `--no-edit`
flag instructs Git to write a commit message; without this parameter Git will
automatically call a text editor and ask you to write a message.

The screen for level 52 is shown below:

![level 52 revert](images/level-52-revert.png)
