
# Level 18 push_tags

> A tag in the local repository isn't pushed into remote repository. Push it
> now.

By default, the `git push` command doesn't push a tag. To render them visible
to anyone else accessing the remote repository, you have to specify that they
should be pushed to the server.

The command to push a tag to the server is

```shell
git push --tags
```

Once this command is executed, anyone accessing the remote repository with `git
clone` or `git pull` will see the tags you've pushed.

The level 18 pass screen looks like this:

![level-18 push_tags](images/level-18-push-tags.png)
