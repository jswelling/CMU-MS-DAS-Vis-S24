# Version Control, Git, and GitHub



## Why are we doing this?

* Because everone does version control.  Learning some good tools makes life easier.
* Because GitHub is the biggest and most popular repository of open source tools out there.
* Because the resources for this class are on GitHub too.



## Goals

* Be able to push and pull updates
* Be able to build venvs from requirements.txt
* Be able to create PRs

## Challenges

* Windows
* People need ssh keys now
* Everything is written in terms of command line stuff



## Why Version Control?

* Because life without it quickly becomes a nightmare.
* Because science gets done in teams, and you don't want to mess up your team.
* Because writing papers involves making little side trips in the code (branches).
* Because bugs will happen, and you need to find where they were introduced.
 * Ideally there are also regression tests, but that's not for today.


## Also, *Provenance*

The provenance of data is the history of where
it came from, and how to reproduce it.

Good science requires good provenance! (And
publishing papers without going crazy does
too).

Part of the provenance of data is the _exact_ code
used to generate/process it, so version
control is a critical part of provenance.



## A Little History
Well, *my* history anyway.

Stage 1: "I just keep copies of my old code".

Stage 2: Revision Control System (circa 1982).
Pretty much like stage 1.

Stage 3: Concurrent Versions System (1986).
Scripts on top of RCS

Stage 4: Subversion (or SVN, 2000)

Stage 5: Git


## Is Git The Answer?

Well, it's the dominant answer _for now_.

There are competitors, like [Mercurial](https://www.mercurial-scm.org/).

Git is also still gaining new features.  We'll have to wait and see.



## Git can be confusing when you're not used to it
[![XKCD on Git](images/xkcd_git.png)](https://xkcd.com/1597/)




## There are lots of docs and tutorials available




## Things To Remember

Git has a lot of potential patterns of use
(unfortunately). Which one is the tutorial
describing?

Remember that there can be *lots* of live
branches in your personal local repo. Your
actual code directory only shows one of them.
Changing branches will change which code is visible.




# Order Of Discussion
1. Big features of the architecture
2. Setting up a repo
3. Editing within the repo
4. Sharing your code
 * With your group
 * With a primary developer

And we'll include some experiments.




## Order Of Discussion
1. Big features of the architecture
 * It's all about a connected graph of commits.
 * The graph can have remote connections (more on this later).
 * Your source files only show one node at a time, but your git environment knows all the nodes and can switch back and forth.
 * Files need to be added to the index before they can be committed.



## A Network Of Commits

![Commits form a connected graph](images/git_history_graph.png)




## Git has and Index State

![Git Index State](images/git_index_state.png)




## Managing Indexed State

`git add` to add a file to the index (stage it)

`git rm` to remove an already-indexed file

`git status` to check what's what

`git commit` to create a new commit including all staged files




## Order Of Discussion
1. ...
2. Setting up a repo

To clone this class:

`git clone https://github.com/jswelling/CMU-MS-DAS-Vis-S24`

To create a local repo with no GitHub partner:

`git init`



## Order Of Discussion
1. ...
2. ...
3. Editing within the repo

`git add` to add new code to the index

`git commit` to turn the index into a node on the graph

`git reset` to revert to the node you were editing

`git checkout` to jump to any node




## Order Of Discussion
1. ...
2. ...
3. ...
4. Sharing Your Code

`git clone` we already learned

`git pull` to get remote updates
* Equivalent to `git fetch` plus `git merge`

`git push` to send your updates to the team




# Experiments!




## Other Useful Commands

```
git branch

git merge

git diff --stat

git diff

git log --graph

git rebase

git bisect
```