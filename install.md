# Githug installation and usage

First install [git](https://git-scm.com/) and
[ruby](https://www.ruby-lang.org/). `githug` itself is programmed in Ruby and is
is installed via the [rubygems repository](https://rubygems.org/) by

```shell
gem install githug
```

Once installed, enter the command `githug` in a folder easily accessible to you.
Initially, you'll be prompted with

> No githug directory found, do you wish to create one?

which you should reply by `y` and then confirm by `Enter` to create a new local
directory `git_hug`. At every level, `githug` uses this special directory to
provide the (if necessary, refreshed) data to work with. There is a brief
outline about the task ahead. The number of stars indicate the difficulty.

Just switch to the `git_hug` directory and get ready to break in.

![githug initialization](images/githug-initialization.png)

Learn the 4 internal commands of `githug` between break-ins:

* `githug play`: break in, i.e. verify that you have completed the tasks
  required by the level. If you have, you will automatically jump to the next
  level. Since this is the most commonly used command, it can be abbreviated to
  `githug`, omitting the `play` at the end.
* `githug hint`: if you don't have a clue about a certain task, you can get some
   inspiration from this hint.
* `githug reset`: Normally, you advance toward the next level by one `git`
  related command. However, if you messed up the file(s) and now want start at
  this specific level (e.g., `githug reset 18`) with a pristine slate, or just
  venture out a different idea to address the problem, use this command to reset
  the relevant files.
* `githug levels`: see the names of each of the 56 levels.

The image below shows the effect of running the `githug play` and `githug hint`
commands:

![githug play and githug hint](images/githug-play-and-githug-hint.png)

Since level 1 is not yet passed, the warning

> Sorry, this solution is not quite right!

indicates the task wasn't  quite solved yet (it is given in red).  The later
command prompts you a hint, i.e.

> You can type `git --help` or  `git` in your shell to get a list of available
> git commands.
