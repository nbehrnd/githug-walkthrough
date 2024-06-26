
# Level 24 remote

> This project has a remote repository. Identify it.
> 
> This project has a remote repository. Identify it.

We spend most of our time working with local repositories, and there are not many commands related to remote repositories. For example, in the previous 23 levels, only 3 of them, level 5, level 6, and level 18, dealt with remote repositories. The next 5 levels will focus on learning about remote warehouses.

Let's start by describing an application scenario. You and others are developing a project at the same time, we all clone the files from the central repository to the local, and then work separately, at this time you only connected to a remote repository - the central repository. If your partner writes a function that you can use, you can pull the function into your repository, and then you connect to a second remote repository, your partner's repository, which bypasses the central repository and allows you to communicate directly and privately, which is why Git is known as a distributed version management system. This is why Git is called a distributed versioning system.

Every developer can connect to multiple remote repositories, but URLs are long and hard to remember, so Git allows you to name each remote repository to improve efficiency.

To see which remote repositories your project is connected to, use the following command:

```
$ git remote
```

The level 24 pass screen looks like this:

! [level-24 remote](images/level-24-remote.png)
