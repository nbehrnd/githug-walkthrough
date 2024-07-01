
# Level 24 remote

> This project has a remote repository. Identify it.

We spend most of our time working with local repositories, and there are not
many commands related to remote repositories. For example, in the previous 23
levels, only 3 of them (level 5, 6, and 18) dealt with remote repositories. The
next 5 levels will focus on learning about remote warehouses.

Let's start by describing an application scenario. You and others are
developing a project at the same time, we all clone the files from the central
repository to local ones, and then proceed to work separately. If your partner
writes a function that you can use, you can pull the function into your
repository, i.e. then you connect to a second remote repository (your partner's
repository). This bypasses the central repository while you communicate
directly and privately, which is why Git is known as a *distributed* version
management system.

Every developer can connect to multiple remote repositories. But as URLs are
long and hard to remember, Git allows you to name each remote repository to
improve efficiency.

To see which remote repositories your project is connected to, use the
following command:

```shell
git remote
```

The level 24 pass screen looks like this:

![level-24 remote](images/level-24-remote.png)
