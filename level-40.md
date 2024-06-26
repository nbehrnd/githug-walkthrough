
# Level 40 rebase

> We are using a git rebase workflow and the feature branch is ready to go into master. Let's rebase the feature branch onto our master branch.
> 
> We are using a git rebase workflow and the feature branch is ready to go into master. rebase the feature branch onto our master branch.

We used the ``git rebase`` command once in level 28, so let's go over it again.

Both ``git rebase`` and ``git merge`` are used for merging, and they have their advantages and disadvantages, so some teams will agree that merging can only be done with ``git merge`` or ``git rebase``, and if you agree that you can only merge with ``git rebase``, this is referred to as a ''git rebase workflow''. git rebase workflow'. When merging branches with ```git rebase``, the merged logs are not organized by the commit time of each branch, but rather, the logs of one branch are arranged on top of the logs of the other, so that even though they were developed in parallel, and commits were staggered during the development process, they look as if they were developed in sequential order.

Take this question as an example. master is the main thread, and the feature branch is created from master. After that, master commits once, with a commit description of "add content", and feature also commits once, with a commit description of "add feature", then execute the following command on master:

``
$ git rebase feature
```

Then the master's logs will read "add content" on top of "add feature".

On the other hand, if you run the following command on the feature:

```
$ git rebase master
```

then the feature's log will be "add feature" over "add content".

The level 40 pass screen looks like this:

! [level-40 rebase](images/level-40-rebase.png)
