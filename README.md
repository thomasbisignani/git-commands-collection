# git-commands-collection
A collection of Git commands and aliases

### Commands

Logs

| Command                   | Description                                        |
| ------------------------- | ---------------------------------------------------|
| `git log -S "foobar"`     | Search the string "foobar" in all diff             |
| `git log -G "foo.*"`      | Search the regex "foo.*" in all diff               |
| `git log --grep="foobar"` | Search the string "foobar" in all commits messages |
| `git log --reverse`       | Reverse the order of the log output                |
| `git log --no-merges`     | Hide the merge commits from the log output         |


Branching

| Command                   | Description                                                                      |
| ------------------------- | ---------------------------------------------------------------------------------|
| `git checkout -`          | Checkout the last branch where you were. _(Note : Alias of `git checkout @{-1}`)_|

Diff

| Command                   | Description                                             |
| ------------------------- | --------------------------------------------------------|
| `git diff --cached`       | Show the changes between the index and the current HEAD |

### Aliases

```bash
[alias]
	# Basics
	co = checkout
	st = status
	wtf = status
	br = branch
	a = add
	
	# Log
	lg = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative
	last = log -1
	
	# Resetting
	undo git reset --soft HEAD^
