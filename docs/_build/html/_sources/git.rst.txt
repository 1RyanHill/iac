git Commands
============

OK, there is some setup with ssh keys to avoid having to use passwords all the time.

::

# git init     (create new repo)
# git clone username@host:/pat/to/repo     (Create a local copy of a remote repo)
# git config --global user.email "you@mail.com"
# git config --global user.name "username"
# git config --list
#
# git add .
# git commit -m "commit comment"
#
# git branch
# git push -u git@github.com:<username>/<project name> master  (sets the remote repo)
# git push
#
# git checkout <branch>
# git checkout -b <new branch>   (Create new branch and go to it)
# git branch -d <branchName>   (delete a branch you are done with)
#
# git pull   (updates local repo to latest commit; tis is a fetch and merge)
