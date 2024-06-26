
# Level 49 bisect

> A bug was introduced somewhere along the way. You know that running "ruby prog.rb 5" should output 15. You can also run "make test".  What are the first 7 chars of the hash of the commit that introduced the bug.
>What are the first 7 chars of the hash of the commit that introduced the bug. 
> A bug was introduced during development. it is known that running "ruby prog.rb 5" should output 15. you can also run "make test". You need to determine the first 7 bits of the hash of the commit that introduced the bug.

As you iterate through your program, you'll want to know when the bug was introduced, in addition to locating the buggy piece of code, so you can use Git's `bisect` utility to find out which commit introduced the bug. `bisect` does this bisectively, just as you would bisect an array element.

Running `make test` tests whether the program executed correctly by executing the "ruby prog.rb 5" statement and then analyzing the output to see if it is equal to 15, and displaying `make: *** [test] Error 1` if it is not.

Let's look at the commit history, which totaled 20 commits:

``
$ git log --pretty=oneline
12628f463f4c722695bf0e9d603c9411287885db Another Commit
979576184c5ec9667cf7593cf550c420378e960f Another Commit
028763b396121e035f672ef5af75d2dcb1cc8146 Another Commit
888386c77c957dc52f3113f2483663e3132559d4 Another Commit
bb736ddd9b83d6296d23444a2ab3b0d2fa6dfb81 Another Commit
18ed2ac1522a014412d4303ce7c8db39becab076 Another Commit
5db7a7cb90e745e2c9dbdd84810ccc7d91d92e72 Another Commit
7c03a99ba384572c216769f0273b5baf3ba83694 Another Commit
9f54462abbb991b167532929b34118113aa6c52e Another Commit
5d1eb75377072c5c6e5a1b0ac4159181ecc4edff Another Commit
fdbfc0d403e5ac0b2659cbfa2cbb061fcca0dc2a Another Commit
a530e7ed25173d0800cfe33cc8915e5929209b8e Another Commit
ccddb96f824a0e929f5fecf55c0f4479552246f3 Another Commit
2e1735d5bef6db0f3e325051a179af280f05573a Another Commit
ffb097e3edfa828afa565eeceee6b506b3f2a131 Another Commit
e060c0d789288fda946f91254672295230b2de9d Another Commit
49774ea84ae3723cc4fac75521435cc04d56b657 Another Commit
8c992afff5e16c97f4ef82d58671a3403d734086 Another Commit
80a9b3d94237f982b6c9052e6d56b930f18a4ef5 Another Commit
f608824888b83bbedc1f658be7496ffea467a8fb First commit
```

First start the `bisect` lookup process:

```
$ git bisect start
$ git bisect good f608824888b
$ git bisect bad 12628f463f4
Bisecting: 9 revisions left to test after this (roughly 3 steps)
[fdbfc0d403e5ac0b2659cbfa2cbb061fcca0dc2a] Another Commit
``

Lines 2 and 3 define the scope of the `bisect` lookup, with `git bisect good` and `git bisect bad` indicating that the current program passes or fails the test, followed by the hash of the first commit after line 2, and followed by the hash of the last commit after line 3, indicating that the lookup scope is all 20 commits. Git then locates the commit in the middle, which has a hash of "fdbfc0d403e5a", and calculates that there are 9 more commits remaining, which is about 3 more binary lookups.

At this point, we test the program and it passes, so we feedback ``good``:

``
$ make test
ruby prog.rb 5 | ruby test.rb
$ git bisect good
Bisecting: 4 revisions left to test after this (roughly 2 steps)
[18ed2ac1522a014412d4303ce7c8db39becab076] Another Commit
``

Git continues with the binary lookup, this time locating the hash "18ed2ac1522a01", we test the program again and the test doesn't pass, so we feedback ``bad``:

``
$ make test
ruby prog.rb 5 | ruby test.rb
make: *** [test] Error 1
$ git bisect bad
Bisecting: 2 revisions left to test after this (roughly 1 step)
[9f54462abbb991b167532929b34118113aa6c52e] Another Commit
```

That's it, after a few rounds of testing, when Git gives the following message, it means it's found:

``
18ed2ac1522a014412d4303ce7c8db39becab076 is the first bad commit
```

Here is a review of the find process:

``
12628f463f4c72 Another Commit
979576184c5ec9 Another Commit
028763b396121e Another Commit
888386c77c957d Another Commit
bb736ddd9b83d6 Another Commit
18ed2ac1522a01 Another Commit 2nd bad
5db7a7cb90e745 Another Commit 4th good
7c03a99ba38457 Another Commit
9f54462abbb991 Another Commit 3rd good
5d1eb75377072c Another Commit
fdbfc0d403e5ac Another Commit 1st good
a530e7ed25173d Another Commit
ccddb96f824a0e Another Commit
2e1735d5bef6db Another Commit
ffb097e3edfa82 Another Commit
e060c0d789288f Another Commit
49774ea84ae372 Another Commit
8c992afff5e16c Another Commit
80a9b3d94237f9 Another Commit
f608824888b83b First commit
``

The level 49 pass screen is as follows:

! [Level 49 bisect](images/level-49-bisect.png)
