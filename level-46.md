
# Level 46 squash

> You have committed several times but would like all those changes to be one commit.
> 
> You have committed several times but would like all those changes to be one commit.

Following up on the previous level, to merge several times into one commit, you can use the ``squash`` command with ``git rebase -i``.

First, check the commit log:

```
$ git log --pretty=oneline
55d9ec9d216767dd1e080c32f5bcff1b3c62ab5b Updating README (squash this commit into Adding README)
749b65067db05a02515c580ad8e791306ff02305 Updating README (squash this commit into Adding README)
1ac3ed61a0ae302cf76dc6f3a37e56e2b5f750f9 Updating README (squash this commit into Adding README)
606be40cc9e5c684cab87c22c37a9d0225308761 Adding README
994f2b3a2df48ef4a406a5c62b4b6f6c8c1fac03 Initial Commit
```

From the query results, we can see that after adding the README, we have made 3 more changes to it.

Find the hash value "994f2b3a2df48ef4a4" in the log below "Adding README" and execute the ```reabse``` command:

```
$ git rebase -i 994f2b3a2df48ef4a4
```

The system automatically opens a text editor to display the history log:

```
pick 606be40 Adding README
pick 1ac3ed6 Updating README (squash this commit into Adding README)
pick 749b650 Updating README (squash this commit into Adding README)
pick 55d9ec9 Updating README (squash this commit into Adding README)
```

Change the "pick" command in front of each of the last 3 logs to "squash":

```
pick 606be40 Adding README
squash 1ac3ed6 Updating README (squash this commit into Adding README)
squash 749b650 Updating README (squash this commit into Adding README)
squash 55d9ec9 Updating README (squash this commit into Adding README)
```

Save and exit, and the system automatically opens the editor again with the merged update instructions:

```
# This is a combination of 4 commits.
# The first commit's message is.
Adding README

# This is the 2nd commit message.

Updating README (squash this commit into Adding README)

# This is the 3rd commit message: Updating README (squash this commit into Adding README)

Updating README (squash this commit into Adding README)

# This is the 4th commit message: Updating README (squash this commit into Adding README)

Updating README (squash this commit into Adding README) # This is the 4th commit message.
```

You can edit the merged update message here, then save and exit. check the logs again, and you'll see that all 3 "Updating README" commits have been merged into "Adding README".

``
$ git log --pretty=oneline
3e8c0e3a729a9d5f959214a2267c481ff0197722 Adding README
994f2b3a2df48ef4a406a5c62b4b6f6c8c1fac03 Initial Commit
``

The level 46 pass screen is below:

![Level 46 squash](images/level-46-squash.png)
