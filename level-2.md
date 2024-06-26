
# Level 2 config

> Set up your git name and email, this is important so that your commits can be identified.
> 
> Set up your username and email address.

The first thing to do after your repository has been initialized is to set up your username and email address. This information is used for every subsequent Git commit, and is used to keep track of who committed the code.

Configuration information is divided into global and local (i.e., the current repository's configuration), and is maintained using the `git config` command, with the `--global` parameter for reading and writing the global configuration, and the `--local` parameter for reading and writing the local configuration. (Note: There is also a layer of system configuration, but it is rarely used and is not discussed here.)

To view the specified configuration information use the `--get` parameter, e.g.:

```
$ git config --get --local user.name
$ git config --get --global user.name
$ git config --get user.name
```

The first command looks at the locally configured user name, the second command looks at the globally configured user name, and the third command looks at the highest-priority user name, and reads the local configuration entry if there is one, or the global configuration entry if there is no local configuration entry.

Add configuration information with the `--add` parameter, for example:

```
$ git config --add --local user.name your-name
$ git config --add --global user.name your-name
$ git conifg --add user.name your-name
```

The first command adds the user name to the local configuration, the second command adds the user name to the global configuration, and the third command is the same as the first command, also adding the user name to the local configuration.

Having mastered the above methods of reading and writing configuration information, and knowing that the keys for the username and email address are user.name and user.email, respectively, completing this level is a simple task:

! [level 2 config](images/level-2-config.png)
