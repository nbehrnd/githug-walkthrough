
# Level 23 checkout_file

> A file has been modified, but you don't want to keep the modification. Checkout the 'config.rb' file from the last commit.
>Checkout the 'config.rb' file from the last commit.
> A file has been modified, but you don't want to keep the modification. Checkout the 'config.rb' file from the last commit.

This is still an undo operation. Use this command if you want to abandon what has been modified in your working directory:

``
$ git checkout your-file
```

Git will overwrite the file with the same name in your working directory with the last commit. However, you must be careful with this operation, because it cannot be undone, and you won't be able to get back what you've changed after it's executed.

The screen for level 23 looks like this:

! [level-23 checkout_file](images/level-23-checkout-file.png)
