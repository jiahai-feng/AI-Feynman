============
Installation
============

Note that for now, AI Feynman is only supported on Linux and Mac environments.

From PyPi
=========

To install from PyPi, you may run::

    pip install aifeynman


From source
===========
First, ensure that your python environment has the following packages:

* numpy (>= 1.15)
* torch (>= 1.0)
* wheel

And that a fortran compiler (such as gfortran) is installed on your computer, and is discoverable in the system path. You may verify this by typing `gfortran --version` in the terminal.

Then, clone the repository. First, build the distribution::

  python setup.py sdist

Then, to install::

  pip install dist/feynman-2.0.0.tar.gz
