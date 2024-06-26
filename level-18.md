
# Level 18 push_tags

> There are tags in the repository that aren't pushed into remote repository. push them now.
>
> There are tags in the repository that aren't pushed into the remote repository.

By default, tags are not pushed to the remote repository by the `git push` command, which means that tags that you have tagged locally will not be seen by anyone else if you do not specify that they should be pushed to the server.

The command to push a tag to the server is as follows:

``
$ git push --tags
```

Once this command is executed, when someone reads from the remote repository using `git clone` or `git pull`, they will see the tags you've pushed.

The level 18 pass screen looks like this:

! [level-18 push_tags](images/level-18-push-tags.png)
