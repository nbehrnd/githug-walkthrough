
# Level 20 commit_in_future

> Commit your changes with the future date (e.g. tomorrow).

It's a strange task to set a commit date in the future, but Git is a time
machine. If you're testing the use of the `--date` parameter of the `git
commit` command, it can be sensible to set the commit date to a date in the
past, such as yesterday or last week.

The command to set the commit time is as follows:

```shell
git commit
git commit --date="2016-10-10T12:01:01"
git commit --date="10 minutes ago"
git commit --date="noon yesterday"
git commit --date="last friday"
```

Command 1 has no `--date` parameter and defaults to the current time as the
commit time. Command 2 sets the commit time to "12:01:01 on October 10, 2016".
Command 3 sets the commit time to "10 minutes ago" while the commit time of the
4th command is set to "12:00 noon yesterday". Conversely, the commit time of
the 5th command is set to "the present moment of last Friday". Note taht the
2nd command sets the absolute time, while the last 3 commands set a relative
time.

The screen of level 20 is as follows:

![Level 20 commit_in_future](images/level-20-commit-in-future.png)
