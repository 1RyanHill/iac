git Commands
============

Key access for GitHub
=====================




**On your (Linux, right?) workstation**::

# cd ~/.ssh
# ssh-keygen -t rsa -b 2048
# chmod 0600 id_rsa
# vi config

Enter::

  Host gitlab.com
    HostName gitlab.com
    IdentityFile ~/.ssh/id_rsa

If you take all the defaults on the SSH Keygen, you get two files.  The .pub file is your public key.  the one without an extension is your private key.  Do not loose this.

You can use the public key to authenticate to GitHub (and other places).  Add your public key to your GitHub account and test key auth using::

# ssh -T git@github.com

Finally.  Some Git commands.::

# git init     (create new repo)
# git clone username@host:/path/to/repo (Create a local copy of a remote repo; looks like #  git remote add origin https://github.com/1RyanHill/iac.git)
# git config --global user.email "you@mail.com"
# git config --global user.name "username"
# git config --list
#
# git add .
# git commit -m "commit comment"
#
# git branch
# -  Go to gitHub and add the Repo.
# git remote add origin https://github.com/1RyanHill/iac.git)
# git push -u origin master
# - The below might also work?
# git push -u git@github.com:<username>/<project name> master   (sets the remote repo)
# git push
#
# git checkout <branch>
# git checkout -b <new branch>   (Create new branch and go to it)
# git branch -d <branchName>   (delete a branch you are done with)
#
# git pull   (updates local repo to latest commit; tis is a fetch and merge)
