
# Level 34 checkout_tag_over_branch

> You need to fix a bug in the version 1.2 of your app. Checkout the tag `v1.2` (Note: There is also a branch named `v1.2`).
> 
> To fix a bug in the version 1.2 of your app, checkout the tag `v1.2` (Note: There is also a branch named `v1.2`).

If there is a tag with the same name as the branch, say 'v1.2', should I switch to the branch or the tag when I run the ```git checkout v1.2``` command? The answer is to switch to the branch.

If you want to switch to the tag, you need to specify it as follows:

```
$ git checkout tags/tag-name
```

The pass screen for level 34 looks like this:

! [level-34 checkout_tag_over_branch](images/level-34-checkout-tag-over-branch.png)
