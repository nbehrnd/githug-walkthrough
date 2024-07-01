
# Level 3 add

> There is a file in your folder called `README`, add it to your staging area.

Now that your repository is initialized and your user information is set up,
it's time to manage your files. Let's take a look at the Git file lifecycle:

![Git file lifecycle](images/git-file-lifecycle.png)

Files in your working directory are not automatically managed by Git. Instead,
you have to add them to the staging area with the `git add` command. The
staging area can hold multiple files. For example, if you are developing a web
site, you want to write an html file, a css file, and a js file, which you can
add one by one to the staging area. By the `commit` command to commit them to
the local repository (the commit area in the picture). The above process is
what you'll be tested on in levels 3 and 4.

The command to add files to the staging area looks like this:

```shell
git add README
git add *.md
git add -A
```

While the first command specifically adds the `README` file to the staging
area, the second command adds all files with the `.md` file extension. By the
third command all files not yet considered are added to the staging area.

The screen of level 3 is as follows:

![level-3 add](images/level-3-add.png)
