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


- Merge actual branch into master (git fetch + git fetch) , with preferences of our branch

`git pull -s recursive -X ours origin master`

- Merge 
`git merge master`
`vim file;git diff file;git add file`
`git push`
- Remove folder from git history

`git filter-branch -f --index-filter "git rm -rf --cached --ignore-unmatch FOLDERNAME" -- --all`


- List biggest files on git history

`git ls-files | xargs du -hs --threshold=1M`


- undo local file changes but NOT REMOVE last commit

`git reset --hard`

- undo local file changes and remove last commit
`git reset --hard HEAD^`
- KEEP local file changes and remove only last commit
`git reset --soft HEAD^`


- best practice

`https://codeinthehole.com/tips/pull-requests-and-other-good-practices-for-teams-using-github/
git chekcout -b feature/branch
git push -u origin feature/branch

git pull origin dev
git rebase dev

git push

merging
git checkout master
git merge feature/branch
git branch -D feature/branch


`

- Diff of all files in HEAD, after adding files ready to commit

`git diff HEAD`


- show commmit only files

`git log --name-status`


- Prune all files not related from .git history

`git gc --prune=now --aggressive`


- remove file from commit

`git filter-branch --tree-filter rm -rf path/to/your/file HEAD`


- Adding git identity to host

`git eval SSH_AUTH_SOCK=/tmp/ssh-Y1rrO3kU7KW0/agent.24425; export SSH_AUTH_SOCK; SSH_AGENT_PID=24426; export SSH_AGENT_PID; echo Agent pid 24426;`


