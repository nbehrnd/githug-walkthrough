
# Level 50 stage_lines

> Stage only the changes belonging to the first feature. belonging to the first feature.
>Stage_lines 
> You've made changes within a single file that belong to two different features, but neither of the changes are yet staged. Stage only the changes belonging to the first feature. Only the changes belonging to the first feature are committed to the staging area.

You can add files to the staging area with the ``git add`` command, but if you don't want to commit all of the changes in a file to the staging area, or if you only want to commit part of a file to the staging area, then you need to add the ``edit`` parameter:

```
$ git add your-file --edit
```

Git will then automatically open a text editor, and the edited content will be the result of the `git diff` command. At this point, you can edit the differences between the two files, keeping only the differences that you want to commit to the staging area and deleting the ones that you don't want to commit to the staging area, and then save and exit, and Git will commit the content to the staging area according to the differences that you've edited.

For example, in this pass, the file's diff is:

``
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

As you can see from the last 2 lines, the added code corresponds to 2 different features. If we only want to submit the code for the 1st feature, just delete the last line.

The screen for level 50 is as follows:

! [level-50 stage_lines](images/level-50-stage-lines.png)
