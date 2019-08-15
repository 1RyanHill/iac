Documentation
=============

We are going to use ReadTheDocs.io for online documentation.

Using the Docs:
---------------

Documentation for this effort can be found at https://iac.readthedocs.io/


Setting up Docs:
----------------

Sphinx is a documentation generation tool.  It allows us to treat documenation as code.
ReadTheDocs links to our documenation in GitHub and puts it online for us.

We are following instructions from http://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html
This includes a video.  Start there.

Create your GitHub project.  In our case, this is the IAC (Infrastructure As Code) project.
Install Python if you do not have it.
Install Sphinx.  You my have to look up instructions if your flavor of linux uses Apt instead of pip.
Navigate tot he project folder and create a docs directory,::

    # cd /path/to/project
    # mkdir docs

We are going to use Sphinx.  Set this up with:: 

    # cd docs
    # sphinx-quickstart

Take defaults except do say y to Seperate source and build directories.

There is a defalt RTD template.  Make it default by editing conf.py (see https://iac.readthedocs.io/ and (better) https://hive.f5.com/docs/DOC-44051)

Edits to conf.py to enable the theme:

Configure your conf.py file to apply the Read the Docs theme.  Add an "import sphinx_rtd_theme" near the top of the config file just under the other import statements that are commented out.::

    # import os
    # import sys
    import sphinx_rtd_theme

Comment  out the default Sphinx theme.::

    html_theme = 'alabaster'
    # html_theme = 'alabaster'

Add the below lines to the bottom of the config file.::

    html_theme = "sphinx_rtd_theme"
    html_theme_path = [sphinx_rtd_theme.get_html_theme_path()]

Build the HTML files with this command::

    # make html 

look in docs/_build/html/index.html to see the local version of your docs.  You can use a browser to point to something like this:  file:///home/ryan/Documents/github/iac/docs/_build/html/index.html


Editing Docs:
-------------

Edit and add files in the docs directory.  The file extensions will be .rst (for ReStructuredText).  Docs for Sphinx / reStucturedText can be found here: http://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html

vi index.rst
Change Main header (above ======)

For sub-pages, put these into the toctree, start them under the : from maxdepth.

Connecting to ReadThe Docs:
---------------------------

* Go to https://readthedocs.org.  Create an account.
* Import your project.
* Build your docs.
* Any time you want to update the published docs, return to https://readthedocs.org/projects/iac/ and build a new version.
* There is an auto-build but it fails on my linux box.  May yours work better.

**Troubleshooting:**

* Make sure your GitHub repo is public.  Otherise you get an error about an inability to log in.
* Make sure you have pushed all of your changes to the master branch of your github repo.
