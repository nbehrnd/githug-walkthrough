
# Level 16 log

> You will be asked for the hash of most recent commit. You will need to investigate the logs of the repository for this.
>You will need to investigate the logs of the repository for this. 
> You will be asked for the hash of most recent commit. You will need to investigate the logs of the repository for this.

This level examines the ability to read the results of the log query.

Each `git commit` command leaves a log of updates in the repository. You can view the history of the logs with the `git log` command. The query looks at all the updates in reverse chronological order of when they were committed, and each log contains a 40-bit hash value, the author's name, email address, and the date of the commit with a description:

```
$ git log
commit 30fef820b410142d3ded8c0908cd1dcb4c0cade0
Author: comehope <comehope@163.com>
Date: Tue Nov 22 17:30:24 2016 +0800

    THIS IS THE COMMIT YOU ARE LOOKING FOR!
    
$ git log --pretty=oneline
411bf644d492f6106acda662612dbc627f951769 THIS IS THE COMMIT YOU ARE LOOKING FOR!
```

The 2nd statement adds the ```---pretty=oneline``` parameter to indicate that it displays the logs in a compact format, showing one commit per line and listing only the hash value and description of the commits, making it easy to quickly view multiple logs.

The level 16 pass screen is as follows:

! [level-16 log](images/level-16-log.png)
