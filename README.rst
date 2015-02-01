====================================
 Github Pages Website for Docutils_
====================================

Build Instructions
==================

.. code-block::
    
    $ git clone https://github.com/docutils/docutils.git
    $ cd docutils

    # branch with changes for https://github.com/docutils/docutils/pull/9
    $ git remote add tony https://github.com/tony/docutils.git
    $ git fetch tony github-docs
    $ git checkout github-docs
    
    # clone the site repository
    $ cd ../
    $ git clone https://github.com/docutils/docutils.github.io.git
    $ cd docutils.github.io
    
    # build our docs
    $ python ../docutils/tools/buildhtml.py --destination ./ ../docutils/docs
    
    # push, wait a few seconds and refresh http://docutils.github.io
    $ git add .
    $ git commit -m "Update"
    $ git push

.. _Docutils: http://docutils.github.io/
