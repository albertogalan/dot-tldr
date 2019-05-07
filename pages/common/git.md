# git

> Distributed version control system.

- Check the Git version:

`git --version`

- Call general help:

`git --help`

- Call help on a command:

`git help {{command}}`

- Execute Git command:

`git {{command}}`

- List files tracked in a branch 

`git ls-tree -r {{branch}} --name-only`


- Rewrite commit history
`https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History`
`git rebase -i HEAD~3`


- Change last commit

`git commit --amend`


- Rever uncommitd changes only to particular file or directory

`git checkout {file}`


- Revert all uncommited changes

`git reset --hard HEAD`


- Mirroring a repository

`git clone --bare https://github.com/albertogalan/dot-git`
`cd dot-git`
`git clone --mirror https://github.com/albertogalan/newrepo`



- Add remote to an existing git repository

`git remote add origin git@github.com:albertogalan/dotgitnew.git`


- Squash commits and change the subject

`git rebase -i HEAD~3`


- Working with submodules

`git submodule add http://github.com/albertogalan/repository`
`git submodule init`
`git submodule update`


- Add credentials and store

`git config credential.helper store`
`git help credential`


- Create a Feature Branch and worktree

git worktree
`cd ~/Demo/myproject`
`git checkout master`
`git branch feature-24601`
`git worktree add ../myproject-24601 feature-24601`
`cd ../myproject-24601`
`git status`

- Cleaning up repository

`rm -rf ../myproject-24601`
`git worktree prune`


- Git aliases

`git config --global alias.add-commit !git add -A && git commit`


