
# Level 54 conflict

> You need to merge mybranch into the current branch (master). But there may be
> some incorrect changes in mybranch which may cause conflicts. Solve any
> merge-conflicts you come across and finish the merge.

We learned about the `git merge` command in level 38. But it's not uncommon to
have merge conflicts in the course of your work. A conflict occurs when both
the merging branch and the branch being merged modify the same line of code in
the same file. Git asks you to intervene and decide whether to keep your code,
someone else's code, or both.

When a conflict occurs, Git gives you the following message:

```shell
$ git merge mybranch
Auto-merging poem.txt
CONFLICT (content): Merge conflict in poem.txt
Automatic merge failed; fix conflicts and then commit the result.
```

This message tells you that automatic merge failed, and that you need to
manually fix conflicts and then commit the result. In this case, the conflict
is in line 2 of a file called `poem.txt`.

At this point you can edit the file with the conflict, which looks like this:

```
Humpty dumpty
<<<<<<< HEAD
Categorized shoes by color
=======
Sat on a wall
>>>>>>> mybranch
Humpty dumpty
I'm not sure if I'm going to be able to do it.
```

The area between the 7 left pointing brackets `<<<<<<<` and the 7 right
pointing brackets `>>>>>>>` is the conflicting section. The 7 equals signs in
the middle `=======` separate the conflicting code: the section above is your
code (usually the mainline code), and the below the line is someone else's code
(usually the code from the development branch). Just edit this section; keep
what you want, delete what you don't want. Save the edit, exit, and submit this
commit anew.

The level 54 pass screen is as follows:

![Level 54 conflict](images/level-54-conflict.png)
