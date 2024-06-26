
# Level 45 rename_commit

> Correct the typo in the message of your first (non-root) commit.
> 
> Correct the typo in the message of your first (non-root) commit.

In the course of using Git, you will inevitably have to rewrite your commits. Git provides a very powerful tool for modifying your history, so let's take this level as an example of how to do it in detail, and then do two more exercises on levels 46 and 48.

Let's start by looking at the commit log:

``
$ git log --pretty=oneline
771b71dca888e80d2bf716672b1475e85a27d695 Second commit
06973a37415e520eff0bace38181f131698cd888 First coommit
37d84aed48418346c4567bb863a0eba4617ba5b1 Initial commit
``

There have been a total of 3 commits, note that the commit with the hash value "06973a37415e520eff" has the 2nd word in the commit note "First coommit" misspelled.

The format of the command to modify the commit history is:

``
$ git rebase -i hash-code
```

We've already touched the ```git rebase``` command at level 40, when we used it to merge branches. But with the ```-i``'' parameter, the purpose is to modify the commit history. This is followed by a hash of a particular commit log, indicating that you want to modify the commit history before that log.

Now, find the hash value "37d84aed48418346c4" for the log one entry below "First coommit" and enter the following command:

``
$ git rebase -i 37d84aed48418346c4
```

This will launch the text editor and display the following:

```
pick 06973a3 First coommit
pick 771b71d Second commit
```

These two lines are the history log, but the difference between `git log` and `git log` is that `git log` displays the logs from back to front in terms of update time, whereas here it displays the logs from front to back. Each line is preceded by a command word that indicates what action to perform on this update, and there are the following commands:

* "pick", which indicates to perform this commit;
* "reword", which indicates to execute this commit, but to change the contents of the remarks;
* "edit", indicating that this commit can be modified, such as appending the file again or modifying it;
* "squash", means merge the content of this commit into the last commit, and the content of the remarks into the last commit;
* "fixup", which is similar to "squash", but discards the contents of this commit;
* "exec", executes a command from the command line;
* "drop", which deletes this commit.

This level will use the "reword" command to accomplish the task. Change "pick" to "reword" in front of line 1 (note that you don't have to change the contents of the memo after the hash) as follows:

``
reword 06973a3 First coommit
pick 771b71d Second commit
```

Next, save and exit, and immediately the system will open the editor again, showing the following:

```
First coommit

# Please enter the commit message for your changes.
```

At this point, you change "coommit" to "commit", save and exit, and then check the log again, and you'll see that the contents of the notes in the history log have changed.

The level 45 pass screen is as follows:

! [Level 45 rename_com
