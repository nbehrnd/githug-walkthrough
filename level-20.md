
# Level 20 commit_in_future

> Commit your changes with the future date (e.g. tomorrow).
> 
> Commit your changes with the future date (e.g. tomorrow).

It's a strange task to set a commit date in the future, but Git is a time machine that only goes to the past, not the future, and it only manages what has happened, so it doesn't make sense to set a commit date at some point in the future! If you're testing the use of the `--date' parameter on the `git commit` command, it makes sense to set the commit date to the past, such as yesterday or last week.

The command to set the commit time is as follows:

```
$ git commit
$ git commit --date="2016-10-10T12:01:01"
$ git commit --date="10 minutes ago"
$ git commit --date="noon yesterday"
$ git commit --date="last friday"
```

Command 1 has no `--date` parameter, so it defaults to using the current time as the commit time; command 2 sets the commit time to "12:01:01 on October 10, 2016"; command 3 sets the commit time to "10 minutes ago "; the commit time of the 4th command is set to "12:00 noon yesterday"; and the commit time of the 5th command is set to "the present moment of last Friday". The 2nd command sets the absolute time, and the last 3 commands set the relative time.

The screen of level 20 is as follows:

! [Level 20 commit_in_future](images/level-20-commit-in-future.png)
