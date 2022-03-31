# git-squash
Custom command for git to squash the most recent n commits into the previous.
Will show the commit messages of the commits to be squashed, and ask for confirmation before proceeding.

## Installation

Place the file `git-squash` in `/usr/local/bin` (or another directory that presented in the PATH variable) and make it executable.
Git will find it, and make it behave like any other git command.

## Usage:
For example you have a feature branch A you want to squash before merging it to branch B. 
Then you need to checkout A and then enter in terminal at repository directory this command:
```
git squash B
```
Another example if have a feature branch A you want to squash it to specific commit with hash (a1b23f4e for example).
Then execute:
```
git squash a1b23f4e
```
This command will leave default commit message containing description of all squashed commits. If you don't need it just use `git commit --amend` command to edit message as you wish. 
Or simply use `git reset --soft` and `git commit` after that without using `--squash` feature.