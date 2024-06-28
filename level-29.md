
# Level 29 diff

> Since your last commit, file `app.rb` was modified. Find out which line has
> changed.

If a file in the repository has been edited, its status changes to `modified`.
You can use the following command to see the details of what has been changed:

```shell
git diff
git diff your-file
```

The first command lists the details of all the files that have been modified.
The second command lists the modified details of the specified file.

For example, you have a file `a.txt` with the following content:

```
a1
a2
a3
a4
a5
a6
a7
a8
a9
```

Then you change entry `a5` into `bbb5`, the content becomes:

```
a1
a2
a3
a4
bbb5
a6
a7
a8
a9
```

Then `git diff` looks like this.

![result of git diff](images/level-29-diff-git-diff-result.png)

Where `@@ -2,7 +2,7 @@` means that the changes were made from line 2 to line 7,
and then lists the contents of lines 2 to 7 (actually, only line 5 was changed,
but it lists the first 3 lines and the next 3 lines of that line). The red
`-a5` and green `+bbb5` indicate that `a5` has been changed to `bbb5`.

The screen for level 29 is as follows:

![Level 29 diff](images/level-29-diff.png)
