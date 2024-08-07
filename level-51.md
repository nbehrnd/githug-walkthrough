
# Level 51 find\_old\_branch

> You have been working on a branch but got distracted by a major issue. Switch
> back to that branch even though you forgot the name of it.

This happens all the time; the dumb solution is to check-out each branch, to
read their logs trying to remember what you were working on. On the other hand,
Git provides you with `reflog`, a tool to trace the history of your work with
Git:

```shell
$ git reflog
894a16d HEAD@{0}: commit: commit another todo
6876e5b HEAD@{1}: checkout: moving from solve_world_hunger to kill_the_batman
324336a HEAD@{2}: commit: commit todo
6876e5b HEAD@{3}: checkout: moving from blowup_sun_for_ransom to
solve_world_hunger
6876e5b HEAD@{4}: checkout: moving from kill_the_batman to blowup_sun_for_ransom
6876e5b HEAD@{5}: checkout: moving from cure_common_cold to kill_the_batman
6876e5b HEAD@{6}: commit (initial): initial commit
```

As you can see, not only are the `git commit` operations related to the file
recorded, but also your `git checkout` operations. So now you know how you were
previously moving between branches.

The screen for level 51 looks like this:

![Level 51 find_old_branch](images/level-51-find-old-branch.png)
