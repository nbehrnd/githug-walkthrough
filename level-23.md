
# Level 23 checkout_file

> A file has been modified, but you don't want to keep the modification.
> Checkout the `config.rb` file from the last commit.

This is still an undo operation. Use this command if you want to abandon what
has been modified in your working directory:

```shell
git checkout your-file
```

Git will overwrite the specified file in your branch with its form of the most
recent commit. However, be careful with this operation because it cannot be
undone.

The screen for level 23 looks like this:

![level-23 checkout_file](images/level-23-checkout-file.png)
