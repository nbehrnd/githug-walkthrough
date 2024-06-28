
# Level 13 stash

> You've made some changes and want to work on them later. You should save
> them, but don't commit them.

Imagine a scenario where you are writing a new method for a class. You are
halfway through, when an urgent task comes up that requires you to modify
another method of the class and then commit it. Now you are faced with the
problem that a new task comes in before the job at hand is done, and it is
dealing with the same file!

Let's think about how an operating system handles this situation: when an
external interrupt arrives, the system hangs the current process, processes the
interrupt, and then resumes the previously hung process after processing the
interrupt. The `git stash` command does something similar. It "hides" the
current environment in a temporary area, then restores the working environment
to the state of the last commit, so that you can jump out of that state and
work on urgent tasks in a clean working environment, and then restore the
previous state with the `git stash pop` command to restore the previously
"stashed" working environment.

The relevant commands are as follows:

```shell
git stash
git stash list
git stash pop
```

The first command "hides" the current environment; the second command lists the
"hidden" environments; the third command restores the "hidden" environments.

The screen of level 13 is as follows:

![Level 13 stash](images/level-13-stash.png)
