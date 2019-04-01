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


