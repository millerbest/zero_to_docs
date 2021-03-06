Installing sphinx
=================

First off we must install sphinx and get our project ready to install some
documentation.

Install and upgrade sphinx
--------------------------

First we'll install sphinx and a few related packages that extend the
functionality of sphinx. We'll cover them in more detail later on.::

  pip install sphinx sphinx-gallery numpydoc --upgrade

Cloning the sample repository
-----------------------------

This tutorial is paired with a skeleton repository we've put
together to help guide you through the setup process. You can
find it in this repository in the ``sphinx-template`` folder.

The ``sphinx-template`` repository already has fully-functioning documentation
that you can use as a reference. This guide will show how to build this
documentation from scratch.

To build the documentation from scratch, first change into the ``sphinx-template``
repository folder.::

  cd path/to/zero_to_sphinx/sphinx_template

Then delete the ``docs`` folder of the repo.::

  rm -rf docs/*

Note this deleted the documentation, but not the whole repository. We'll spend
the rest of this tutorial adding some good documentation back in.

Take a look at what's inside the repository we downloaded.::

  ls -l ../sphinx_template

Inside this folder is a sample repository that could use some documentation.
If we look inside it, we can see that the repo has:

* a python package called ``my_package`` with some code
* an examples folder called ``examples``
* configuration files for the repo
* an empty folder ``docs`` where we'll put new documentation

The ``my_package`` folder has the code for the project...

This is a common structure for a package. We've got some code that
gets something done, and a few examples that show off this code.
Since we are hosting this repo on github, we are also deploying it to
gh-pages in order to have our own little website.

In addition, note that the `docs` folder is relatively empty.
Let's change that!

Running Sphinx Quickstart
-------------------------
The easiest way to set up a sphinx repository is to use
``sphinx-quickstart``. This will ask you a few questions about
your project, and then quickly generate a shell structure for
your documentation.

You'll need to run this command from your shell (because it asks you
questions interactively). Do the following things:

* Change directories to the ``docs`` directory.::

    cd ../sphinx-template/docs

* Run the sphinx-quickstart tool.::

    sphinx-quickstart

  This will begin an interactive session that will ask you a few questions
  about your project. Here are some suggested answers:

  * Answer ``no`` when it asks whether you want separate ``source`` and
    ``build`` directories. This will put the built website in a folder called
    ``_build`` that lies in the same folder where your text files exist.
  * Make sure to answer ``yes`` when it asks you to install the following packages
    * githubpages
    * MathJax
    * intersphinx
  * Give whatever you like for the name / version number of the documentation.
    A good suggestion is following structure like ``v0.1``.
  * For the other questions, the default answer is fine. Just hit ``enter``.

Build your documentation
------------------------
After you run ``sphinx-quickstart``, you can already build
your documentation and see how it looks. To do this, just navigate to the
folder in which you ran ``sphinx-quickstart`` and run::

  make html

This will inspect the text files in your documentation folder and render
them into built documentation. Navigate to the ``_build/html`` folder, and
click on ``index.html``. You should see a rendered page show up in your
web browser.

This is quite a bare-bones documentation page. Next we'll need to customize
our docs. First, let's take a look at :ref:`structure`.
