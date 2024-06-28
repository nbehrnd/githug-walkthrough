
# Level 45 rename_commit

> Correct the typo in the message of your first (non-root) commit.

In the course of using Git, you will inevitably have to rewrite your commits. Git provides a very powerful tool for modifying your history, so let's take this level as an example of how to do it in detail. Levels 46 and 48 explore this further.

Let's start by looking at the commit log:

```shell
$ git log --pretty=oneline
771b71dca888e80d2bf716672b1475e85a27d695 Second commit
06973a37415e520eff0bace38181f131698cd888 First coommit
37d84aed48418346c4567bb863a0eba4617ba5b1 Initial commit
```

Among the 3 commits, note that the commit with the hash value "06973a37415e520eff" has a misspelled commit message: "First coommit".

The syntax of the command to modify the commit history is:

```shell
git rebase -i hash-code
```

We've already introduced the `git rebase` command at level 40 to merge branches. The optional `-i` parameter is to start an interactive mode to edit the commit history. It is followed by a hash of a particular commit log, indicating that you want to modify the commit history before that log.

Now, find the hash value "37d84aed48418346c4" for the log one entry below "First coommit" and enter the following command:

```shell
git rebase -i 37d84aed48418346c4
```

This will launch the text editor and display the following:

```
pick 06973a3 First coommit
pick 771b71d Second commit
```

These two lines are the *history log*. The difference between (standard) `git log` and `history log` is that `git log` displays the logs from back to front in terms of update time, whereas the `history log` here it displays the logs from front to back. Each line is preceded by a command word that indicates a future action on this update:

* "pick", to perform this commit;
* "reword", to execute this commit with an edited commit message;
* "edit", to modify this commit, such as appending the file again or modifying it;
* "squash", to merge the content of this commit into the last commit, and the content of the remarks into the last commit;
* "fixup", is similar to "squash", but discards the contents of this commit;
* "exec", executes a command from the command line;
* "drop", to delete this commit.

This level will use the "reword" command. Change "pick" to "reword" in front of line 1 (note that you don't have to change the contents of the memo after the hash) as follows:

```
reword 06973a3 First coommit
pick 771b71d Second commit
```

After save and exit, Git immediately opens the editor again, showing the following:

```
First coommit

# Please enter the commit message for your changes.
```

At this point, you edit "coommit" to "commit", save and exit. When you check the log again, you'll see the contents of the notes in the history log were changed.

The level 45 pass screen is as follows:

![Level 45 rename_com
