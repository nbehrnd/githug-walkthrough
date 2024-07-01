
# Level 50 stage_lines

> You've made changes within a single file that belong to two different
> features, but neither of the changes are yet staged. Stage only the changes
> belonging to the first feature.

You can add files to the staging area by `git add`. However if you don't want
to add all edits of a file into the staging area, or if you only want to commit
a part of a file, then you need to add the `--edit` parameter:

```shell
git add your-file --edit
```

Git then automatically opens a text editor; the edited content will be the
result of the `git diff` command. At this point, you can edit the differences
between the two files to keep only the differences that you want to commit to
the staging area and to delete the ones that you don't. After save and exit,
Git will commit the content to the staging area according to your edits.

In this level, the file's diff is:

```shell
$ git diff feature.rb
diff --git a/feature.rb b/feature.rb
index 1a271e9..4a80dda 100644
--- a/feature.rb
+++ b/feature.rb
@@ -1 +1,3 @@
 This is the class of my feature
+This change belongs to the first feature
+This change belongs to the second feature
```

As you can see from the last 2 lines, the added code corresponds to 2 different
features. If we only want to submit the code for the 1st feature, just delete
the last line.

The screen for level 50 is as follows:

![level-50 stage_lines](images/level-50-stage-lines.png)
