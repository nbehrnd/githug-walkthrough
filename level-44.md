
# Level 44 grep

> Your project's deadline approaches, you should evaluate how many TODOs are
left in your code.

Similar to Linux's `grep` command, Git provides a `grep` command for a search
in the source code:

```shell
git grep keyword
git grep -n keyword file-name
git grep -ic todo *.md
```

The first command looks for the specified `keyword` under the current project.
The second command reports the line number of `keyword` in the specified file.
Indiscriminate of usage of upper/lower case (`-i`), the third command queries
each `*.md` file for `todo` (as well as `TODO`, and `Todo`, etc.). The file and
its count will be reported if the string was found at least once.

The level 44 pass screen is as follows:

![level-44 grep](images/level-44-grep.png)
