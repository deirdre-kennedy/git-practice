# Practice makes perfect

## Commands Used

- git init: create a new git repository
- git status: compare any changes made in working directory vs staging area and current branch
- git add: add changes form working dir to staging area
- git commit: changes from staging area to current branch
- git config: set or get configuration
- git log: looking at older commits (show history) aka log
- git branch <branch-name>: creates new branch
- git checkout <branch-name>: checkout branch (update HEAD and apply changes to working directory)
- (shortcut): git checkout -b <branch-name>
- git merge: merge changes from different branches
- git remote add <remote> <url>: add a new <remote> at <url>
- git remote -v: list remote repos
- git push -u <remote> <branch>: push <branch> to <remote>, and set default upstream for <branch>
- git fetch: fetch changes from remote repo
- git push: fetch and then merge

## Commit messages

Default editor is vim (this can be changed)
  - `i` to enter *insert* mode
  - Type commit message
  - `Esc` -> `:wq` -> `Enter` to write message and quit
Or use `git commit -m "<message>"`

- First line should be clear, accurate, and concise
- Use proper spelling, grammar, and punctuation
- Don't end with a `.`

For more advice, see: https://chris.beams.io/posts/git-commit/

## Merging

Merging means to bring the changes from one branch into another.

- A fast-forward merge happens when the target branch was branched from the current one, and there are no new changes to the current branch since then.
- An Automatic merge happens when the two histories have diverged, but git is able to reconcile them into one set of changes. This creates a new commit on the current branch.

## What's a remote?

A remote repo is one hosted somewhere other than our local machine. We can add remotes with `git remote add`, and set up *tracking branches* to track differences between our local and remote repositories.

We push to remotes with `git push`, and fetch from them with `git fetch`. We can also fetch and merge in one set with `git pull`.