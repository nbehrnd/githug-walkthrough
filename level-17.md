
# Level 17 tag

> We have a git repo and we want to tag the current commit with 'new_tag'.
> 
> Add a tag called 'new_tag' to the current commit in the repository.

Think of developing a project as a journey. If each commit is a telephone pole swinging out the window, then the tag is the station where you can stop and drive to the end of the line, or take a break to look at the scenery and keep going. Lens back to the 17th level, the above analogy is the difference between commit and tag, commit is fine-grained, programmer-oriented, each write a function, each fix a bug, you can submit a commit, and tag is coarse-grained, user-oriented, generally only in the increase or optimization of a user-perceivable function, only to play a tag, software version number is the most common form of tag. The version number of software is the most common form of tag, a new version number means that a new release package should be released to the public.

The command for tagging is as follows:

```
$ git tag your-tag
$ git tag your-tag a38862a5a860
$ git tag
$ git tag -d your-tag
```

Command #1 tags the most recent commit; command #2 tags a specific commit, followed by the commit's hash value or the first few digits of the hash value; command #3 lists all the tags; and command #4 deletes the tags.

The level 17 pass screen is as follows:

! [level-17 tag](images/level-17-tag.png)

