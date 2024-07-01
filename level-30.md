
# Level 30 blame

> Identify who put a password inside the file `config.rb`.

When a bug or vulnerability is exposed you need to locate the code and want to
identify the origin of the particular section. For each line of the code, Git
can report its author by the special command

```shell
git blame your-file
```

The listing reports the line of code altogether with the commit hash, the time
of the commit, and the author's name.

The level 30 pass screen is as follows:

![level 30 blame](images/level-30-blame.png)
