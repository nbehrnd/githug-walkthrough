
# Appendix B Common Linux Commands

When you use Git on the command line, you need to manipulate files and
directories in addition to executing Git commands. Here are some common Linux
commands:

## Viewing Files

> ls

## View hidden files

> ls -a

## Create a directory

> mkdir name

## Delete directory

> rmdir name

You cannot delete a non-empty directory

## Delete non-empty directories

> rm -rf dir-name

## Moves files/directories, can also be used to rename files/directories

> mv source target

## Copy a file or directory

> cp source target

## View the contents of a text file

> cat your-file-name.txt

## Search for text from a text file

> grep 'TODO' \*
>
> grep 'TODO' app.rb
