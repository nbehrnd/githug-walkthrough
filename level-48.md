
# Level 48 reorder

> You have committed several times but in the wrong order. Please reorder your commits.

In levels 45 and 46, we used the `git rebase -i` command to change the commit messages in the history log while merging multiple commits into one.

Let's start by checking the commit log:

```shell
$ git log --pretty=oneline
3baec3ba260f841e097675e4ae6661a86e3dba50 Second commit
a5f696b57d524c83b9fbb094b013590e4ff3d43d Third commit
19f3b096c2765ab79d9b07a5bed3a4ebb83ebf6a First commit
f0c159847ae93dabc8fd23766b40cf0cc21b315d Initial Setup
```

The above query shows that the order of "Second commit" and "Third commit" is reversed. Let's find the hash "f0c159847ae93" of the last log and enter the following command:

```shell
git rebase -i f0c159847ae93
```

Git automatically opens the text editor to display the history log:

```
pick 19f3b09 First commit
pick a5f696b Third commit
pick 3baec3b Second commit
```

Reorder the contents of lines 2 and 3, i.e. like this:

```
pick 19f3b09 First commit
pick 3baec3b Second commit
pick a5f696b Third commit
```

After save and exit, Git will re-execute the commits in the adjusted sequence. Check the logs again and see that the sequence has been adjusted.

```shell
$ git log --pretty=oneline
58fe3005755a19d18c017973517dfaca1b1ae648 Third commit
e0e8d4428578fb7b1284b1c7902e435e9bd571c4 Second commit
19f3b096c2765ab79d9b07a5bed3a4ebb83ebf6a First commit
f0c159847ae93dabc8fd23766b40cf0cc21b315d Initial Setup
```

The level 48 passing screen is as follows:

![Level 48 reorder](images/level-48-reorder.png)
