CLI Commands:
=============

Set up GitHub Project:
----------------------

200~mkdir github
292  cd github
293  mkdir iac
294  cd iac
295  mkdir docs
296  git init
297  touch README
298  git add *
299  git commit -m "initial commit"
302  git status
303  git branch

go to github and add a Repo.

305  git remote add origin https://github.com/1RyanHill/iac.git
306  git push -u origin master

Start docs:
-----------

309  cd docs

https://hive.f5.com/docs/DOC-44051
    $ pip install sphinx  
    $ pip install sphinx-autobuild  
    $ pip install sphinx_rtd_theme

310 sphinx-quickstart

Customize the Sphinx Environment

 

Configure your conf.py file to apply the Read the Docs theme.  Add an "import sphinx_rtd_theme" near the top of the config file just under the other import statements that are commented out.

 

    # import os  
    # import sys  
    import sphinx_rtd_theme  

 

Comment  out the default Sphinx theme.

 

    html_theme = 'alabaster'  
    # html_theme = 'alabaster'  

 

Add the below lines to the bottom of the config file.

 

    html_theme = "sphinx_rtd_theme"  
    html_theme_path = [sphinx_rtd_theme.get_html_theme_path()]  

 

312  make html
