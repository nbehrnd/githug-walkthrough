
# Level 28 push

> Your local master branch has diverged from the remote origin/master branch. Rebase your commit onto origin/master and push it to remote.
>Rebase your commit onto origin/master and push it to remote. 
> Your local master branch has diverged from the remote origin/master branch. rebase your commit onto origin/master and push it to remote.

When you're developing with other partners, you both clone your files locally from the remote repository, then split up your development, and then split up your push to the remote repository with the following push command:

```
$ git push remote-name branch-name
$ git push -u remote-name branch-name
$ git push
```

The first command pushes a local file to a remote repository. remote-name is the name of the remote repository, and branch-name is the name of the branch; if you haven't renamed them, their default names are origin and master, respectively; the second command adds a `-u` parameter to make Git remember remote-name and branch-name, so you don't have to write them again. branch-name, so you don't have to write them again; and the third command is the push command after the `-u` parameter, so you don't need any more parameters.

In multi-developer development, there is a priority for pushing, according to Git's rules, when you push, if someone has already pushed before you, if you push again, you will get a "non-fast forward" message, which translates to "can't fast-forward". There are at least 2 ways to fix this:

First, you can use the `git pull` command to merge the latest code from the remote repository into your local repository, and then commit it. The local commits will be mixed with the remote commits in chronological order.

Second, you can use the `git rebase` command to schedule the local repository after the remote repository, so that all commits from the local repository are scheduled after the last commit from the remote repository.

The test in this level is to solve the problem by using the `git rebase` method.

The scenario for this level is that the local repository has 3 updates (named First commit, Second commit, Third commit), the remote repository has 1 update (named Fourth commit), and after the rebase and push, the remote repository will have 4 updates.

The screen for level 28 is as follows:

! [level-28 push](images/level-28-push.png)
