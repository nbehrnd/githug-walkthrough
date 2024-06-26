
# Level 30 blame

> Someone has put a password inside the file 'config.rb' find out who it was.
> 
> Someone has put a password inside the file 'config.rb' find out who it was.

When a bug or vulnerability is exposed and you want to find out where it came from, you first need to locate the code, and then you need to locate who introduced the bug; Git keeps detailed update logs, so you can locate the developer with a special command provided by Git:

``
$ git blame your-file
```

In the result all the code of the specified file will be listed, and to the left of each line of code will be listed its HASH value, developer and time when it was last updated. With this information you can analyze who edited each line of code.

The level 30 pass screen is as follows:

! [level 30 blame](images/level-30-blame.png)
