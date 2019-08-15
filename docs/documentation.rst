Documentation
=============

We are going to use ReadTheDocs.io for online documentation.

Using the Docs:
---------------



Building Docs:
--------------

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
There is a defalt RTD template.  Make it default by editing conf.py (see https://hive.f5.com/docs/DOC-44051)
Build the HTML files with this command::

    # make html 

look in docs/_build/html/index.html to see the local version of your docs.

vi index.rst
Change Main header (above ======)

For sub-pages, put these into the toctree, start them under the : from maxdepth.

Connecting to ReadThe Docs:

Go to https://readthedocs.org.  Create an account.
