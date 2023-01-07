# Git CheatSheet

# Hi All! <br>
> In this repo I'll keep on uploading useful git commands.

## Convert working directory to git repository
- `git init`

## Set global config parameter
- `git config --global user.name "user_name"`
- `git config --global user.email "email_address"`

## check status of git repo
- `git status`

## add files to staging
- `git add <filename>` # add single file to staging
- `git add <file1> <file2>` # add multiple files to staging
- `git add .` or `git add --a` # add all files to staging

## remove files from staging
- `git rm --cached <filename>` or `git restore --staged <filename>` # unstage single file
- `git rm --cached <file1> <file2>` or `git restore --staged <file1> <file2>` # unstage multiple files

## commit files
- `git commit -m '<message for commit>'` # commit staged files
- `git commit -a -m '<message for commit>'` # directly commit all tracked files, however donot commit untracked files

## merge current commit with last commit
- `git commit --amend` 

## check commit history
- `git log` # display commit history without showing changes
- `git log -p` # display commit history along with changes
- `git log -p -<n>` # display last n commit where n can be 1,2,3
- `git log --stat` # display commit statistics
- `git log --pretty=oneline` # display single commit in single line
- `git log --pretty=short` # display short summary of commit
- `git log --pretty=full` # display full summary of commit
- `git log --since=2.days` # display last 2 days commit, instead of `days` we can use `weeks`, `months`, `years`, `Hours`
- `git log --pretty=format:"%h -- %an"` # format commit history, refer <a href="https://git-scm.com/docs/pretty-formats">this</a> link for more details

## change git repo to working directory / delete git repo
- `rm -rf .git` # delete .git file so that we can change git repository to simple directory

## clone remote git repository
- `git clone <repo_url> [repo_name]` # download remote repo to your local system

## some useful linux command
- `touch <filename>` # create a new file
- `ls` # show files in directory
- `vim <filename>` # open file in vim editor

## compare staging area and commit
- `git diff` # compare staging area and working directory
- `git diff --staged` # compare staging area with previous commit

## rename and delete file using git
- `git rm <filename>` # delete file from directory as well as staged 
- `git mv <old_name> <new_name>` # rename file and stage as well

## restore unstaged files to last commit
- `git checkout -- <filename>` # note: it does not work with staged files
- `git checkout -f` # restore all modification (staged or unstaged) to previous commit

## working with branches
- `git checkout -b <branch_name>` # create and switch to new branch
- `git checkout <branch_name>` # switch to another branch
- `git branch -v` # display last commit of all branch
- `git branch --merged` # display merged branches
- `git branch --no-merge` # display unmerged branches
- `git branch -d <branch_name>` # delete if branch is merged else error
- `git branch -D <branch_name>` # delete branch irrespective of merged or not
- `git branch -m <new_branch_name>` # rename current branch to new name
- `git branch -M <new_branch_name>` # rename current branch to new name
- `git branch -m <old_name> <new_name>` # rename branch from any other branch

## creating alias
- `git config --global alias.alias_name command_name` 
> Example: <br>
> `git config --global alias.st status` <br> 
> here instead of `status` we can use `st` <br> 
> Now if we type ----> `git st` ----> this is equivalent to ---> `git status` <br>

## working with remote repository
- `git clone <repo_url>` # creating clone of remote repository in locat system
- `git push -u origin <branch_name>` # push local branch to remote branch
- `git push origin <lacal_branch_name>:<remote_branch_name>` # push local branch to remote branch with new name
- `git remote -v` # show the URLs that  are used during the reading and write operation
- `git push origin -d <branch_name>` # delete branch in remote
