# (Force) Push That Branch

### What is a force push anyway?
![Obi Wan Wreckin' Droids](http://imgur.com/Pebszrd.gif)

Yeah - it's basically that. Except to your Git Repo. It's powerful and destructive, but sometimes it's the tool for the job.

### The Sudo of Git Branches
That little `-f` flag tells git to forcefully make your change. Even if Git thinks it's a bad idea. Even if your teammates think it's a bad idea. Git does the deed, rewrites the remote branch's history to be what you want, and creates a ticking time bomb for **anyone else** who has the branch.

The forcefully part means Git will rewrite your repo's history to make the remote branch's history match your local branch's history. The time bomb occurs because if someone else has that branch with the un-re-written history, Git will be confused when trying to compare their branch to the remote. 

### Why would I ever want to do that?
Remember how we use feature branches? And only 1 developer uses his or her feature branch? Well if no one else has pulled your feature branch, rewriting that branch's history is awesome.

Make a few frivolous commits? Rewrite them out of existence and don't worry about.

About to make a pull request and want a nice, clean, simple history of changes? Squash those commits and rewrite that branch. No one is looking.

Accidentally commit to master, realized it days later, and want to make it like it never even happened? **STOP. NEVER FORCE PUSH A BRANCH THAT YOU DON'T OWN.**

### In doubt about whether or not you should use `-f`?
Try reviewing this diagram which may be helpful.
![An awesome diagram](http://imgur.com/WSG4rAU.png)


