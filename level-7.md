
# Level 7 ignore

> The text editor 'vim' creates files ending in `.swp` (swap files) for all files that are currently open. We don't want them creeping into the repository. Make this repository ignore those swap files which are ending in `.swp`.

When you're developing, you'll often have editors, IDEs, compilers, or other programs that automatically create temporary files, log files, or whatever, which aren't considered source code and hence shouldn't be managed by Git.

The `.gitignore` file stored in the root directory of your repository is used to configure rules for ignoring files. It is a text file with one rule per line, and examples of common rules are as follows:

```
# Ignore the file named foo.txt.
foo.txt

# Ignore all *.log files
*.log

# With the exception of important.log, which is not ignored.
!imprtant.log
```

Level 7 passes with the following screen:

![level-7 ignore](images/level-7-ignore.png)
