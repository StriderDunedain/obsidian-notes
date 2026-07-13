---
tags:
  - cs/util
date: 2025-10-29
updated: 2026-07-08
"created ": 2026-06-24
---
## Commands:
1. Show *settings* & where they are comig from: `git config --list --show-origin`. Can set a global variable (`user.name, user.email, core.editors`)
2. Get *help*: `git help <command>`, or `git <command> --help`, or `man git-<command>`
3. *Initialize* a git repository: `git init`
4. Show smol *status*: `git status -s`
5. *Clone* into specific directory: `git clone ... <dir_name>`. Optionals:
	1. `-o <remote name>` sets remote name (i.e. not `origin/master` but `my/master`)
6. `git diff`: shows difference between last commit & **unstaged** files (pass `--staged` | `--cached` to also take them into account)
7. `git commit`: without params opens an IDE to type in the commit message (pass `-a -m` to skip staging area)
8. `git rm`: removes the file from staged (?)
9. `git mv`: (?)
10. `git log`: shows commit history. Optionalities (others at ProGit on pg 44-45):
	1.  `-p` adds git diff output
	2. `-3` limits the output
	3. `--stat` abbreviated commit
	4. `--pretty` formats the output (options: `oneline` or `format="<dt format>"` for further look at ProGit on pg 43)
	5. `--graph` outputs log as an ascii graph
	6. `--since` & `--until` params
	7. `--grep` is basically ctrl+F
	8. `-S` pickaxe of git - searches for changes in said string
11. `git commit --amend` u know what it does ("takes your staging area and uses it for the commit")
12. `git reset HEAD <file>` / `git restore` ! Danger Zone ! Unstages a file | reverts file to a previous state
13. `git checkout -- <file>` ! Danger Zone ! Reverts file to how it looked in the last commit completely & finally erasing its current content
14. `git remote` shows remote repos (`origin` is default). Optionals:
	1. `-v` shows urls of remote repos
	2. `add <shortname> <url>` adds new remote repo (shortname can then be called upon to fetch / push to that url)
	3. `show <remote>` inspects the remote repo
	4. `rename <shorthand> <new shorthand name>` renames the shorthand
	5. `remove` / `rm`  + `shorthand` removes shorthand
	6. `show <remote>` / `git ls-remote <remote>` lists all remote branches
15. `git fetch` / `git pull` the former gets all data from remote repo and **doesn't** merge it, the latter **does**. `fetch --all` get all data from remote
16. `git fetch <remote>` synchronizes state of remote with your local state
17. `git push <remote> <branch>` u get it. Optionals:
	1. `<tag>` also push a tag
	2. `--tags` pushes all local tags that are not on remote 
	3. `--delete <obj>` deletes obj from remote (tag / branch)
	4. `--set-upstream` / `--set-upstream-to` / `-u` + `<remote> <associated branch name>` sets remote association for local branch
	5. `@{upstream}` / `@{u}` shortcut (really?) for remote branch name
18. `git tag` lists tags in alphabetical order. Optionals:
	1. Tags can be *lightweight* or *annotated* - the former is just a string but the latter is more of a whole commit. Tags are *unique* and are **not** pushed to remotes by default
	2. `-l` / `--list` +  `"<pattern>"` outputs all matching tags
	3. `-a <tag> -m "<message>"` creates an *annotated* tag
	4. `<tag>` creates a *lightweight* tag
	5. `-d <tag>` deletes a tag
	6. To delete tag from remote, see `git push`
19. `git show <tag>` outputs detail of a tag
20. `git checkout` jumps between branches. Optionals:
	1.  `-b <branch> <tag>` in case of editing existing commit with tag - better create a new branch (be carefult - might be dangerous)
	2. `-b <local branch> <remote branch>` sets up tracking for remote branch with local name different
	3. `--track <remote branch>` sets up tracking for a remote branch
	4. `<remote branch>` shortcut for `--track` shortcut. If a) such local branch doesn't exit & b) matches **only** one remote - sets up tracking for remote branch
21. `git branch` lists all branches. Optionals:
	1. `-d <branch>` deletes branch
	2. `-v` lists all branches & last commit into them
	3. `--merged` / `--no-merged` + (optional) `<branch>` shows branches that have or have not been merged into working branch (if not specified, else `<branch>`)
	4. `--move <old branch name> <new branch name>` renames a branch ! Danger Zone !
	5. `--all` lists local & remote branches
	6. `-vv` list which remote each local branch tracks
22. `git rebase <branch>` rebases branch you're on to the `<branch>`. Optionalities:
	1. `git rebase --onto <intended branch> [<branch closest to intended> ... <other branches> ... <final interesting branch>]` applies changes from `<final interesting branch>` to `<intended branch>`, skipping all other branches 
## .gitignore files
### Writing Rules:
```bash
1. Blank line | lines starting with '#' will be ignored
   # glob patterns are the "go-to"
2. Starting with / means "avoid recursivity" (i.e. in this dir, not any below)
3. Ending in / means "the whole directory"
4. ! Negates a pattern
5. * - 0 or more chars
6. [abc] means "any chars from `[]`"; [0-9] - 0 through 9
7. ? - single char
```
### Examples:
 ```bash
 # ignore all .a files
*.a
# but do track lib.a, even though you're ignoring .a files above
!lib.a
# only ignore the TODO file in the current directory, not subdir/TODO
/TODO
# ignore all files in any directory named build
build/
# ignore doc/notes.txt, but not doc/server/arch.txt
doc/*.txt
# ignore all .pdf files in the doc/ directory and any of its subdirectories
doc/**/*.pdf
```

## ~ Specials
1. Aliases (get all with `git config --get-regexp ^alias` & create with `git config --global alias.<name> '<command>'`):
	1.  `do`  / `write`  == `commit -a -m`
	2. `last` == `log -1 HEAD` (outputs last commit)`
	3. `switch` == `checkout -b`
	4. `oneline` == `log --pretty=oneline`
2. *blob* - jargon for a version of a file in git
3. Checksums are created via SHA-1
4. HEAD is a pointer to current branch
## Questions:
1. difference between reset and restore
2. mv and rm command working principles
3. rebase
4. resetting
5. --set-upstream
6. git remote show remote

Tags: #cs/ #git #version_control #notes