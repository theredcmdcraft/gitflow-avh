This page will contain a few words on the Python rewrite (see the 
[feature/python-rewrite](http://github.com/nvie/gitflow/tree/feature/python-rewrite) branch), the design goals, and
I might even experiment with designing it "out in the open".

Design goals
============

git-flow is the result of a natural evolution, starting from an idea in the
[nvie.com](http://nvie.com/git-model) post
[comment](http://nvie.com/posts/a-successful-git-branching-model/#comment-72478949).
The main pain points of git-flow currently are:

* Testability: git-flow needs unit tests and the biggest mistake has been not
  to write unit tests from the start.  I'm going to fix this one big time!
* Installability: With Python, installing git-flow will be a snap:
  `pip install git-flow`
* Extendibility: The shell scripting framework git-flow consists of now is
  pretty rigid.  To make one change, you need to touch multiple source
  files/functions.  The code needs some proper refactoring.
* Maintainability: See Extendibility.
* Contributability: There simply are more "high-level" volunteers than shell
  scripting volunteers.
* Windows support: The Windows platform is notorious for its lack of a decent
  programmer's toolchain.  Hence, you currently have to install msysgit and/or
  Cygwin to get Git and the basic Unix utility `getopt` to get git-flow to
  run.  Implementing git-flow in Python can change all this, since Python
  ships with "batteries included", requiring no external toolchain again.
* Documentability: Python comes with great documentation tools in the form of
  [Sphinx](http://sphinx.pocoo.org/)


Getting involved
================

The Python rewrite is just getting started (Oct '10) and I invite you to join
the design discussion and invite you to bring on new functionality.  One of the
core design goals is to have the project fully unit tested and ideally, to
cover every line of source code by tests.

If you like to get involved, I advise you to take the following steps.

Testing setup
-------------

* Install virtualenvwrapper:

      `pip install virtualenvwrapper`
  
* Make a gitflow virtual Python environment:

      `mkvirtualenv gitflow`
  
* Install the required testing tools:

      `pip install GitPython nose nose-cover3 coverage`

      And if you are using a pre-2.7 version of Python:

      `pip install unittest2`
  

Hacking
-------

* Check out the Python sources:

``` bash
    git clone git://github.com/nvie/gitflow.git
    cd gitflow
    git checkout -b feature/python-rewrite origin/feature/python-rewrite
```
  
* If you want to switch to the (virtual) gitflow environment at any given time,
  use:

      `workon gitflow`
  
* Run the unit tests and coverage reports:

      `make cover`

