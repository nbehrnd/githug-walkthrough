
# Level 42 repack

> Optimise how your repository is packaged ensuring that redundant packs are
> removed.

As we mentioned in level 1, when a Git project is initialized, Git creates a
hidden subdirectory `.git` with files to manage the repository. In the Git
world, a file is a Git object, a commit is a Git object, and they are stored in
the path of `.git/objects/ directory`:

```shell
$ ls .git/objects/
4d a0 e6 info pack
```

The first three of these directories have directory names that are two numeric
letters long, and each holds one object. The more you do in Git, the more Git
objects you generate. To optimize the efficiency of your repository, you can
pack the objects manually:

```shell
git repack
git repack -d
```

The first command packs objects together, and the second command removes
objects that have been invalidated after packing. After executing the repack
command, 3 files are created in the `.git/objects/pack/` directory:

```shell
$ ls .git/objects/pack/
pack-b7b37f445a40715c249bf8c0df9631e9fd6c8f4b.idx
pack-b7b37f445a40715c249bf8c0df9631e9fd6c8f4b.pack
pack-b7b37f445a40715c249bf8c0df9631e9fd6c8f4b.rev
```

In this listing, `.pack` is the package file and `.idx` is the package index
file.

The level 42 pass screen is as follows:

![level-42 repack](images/level-42-repack.png)
