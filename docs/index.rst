AI Feynman
==========


This code is an improved implementation of AI Feynman: a Physics-Inspired Method for Symbolic Regression, Silviu-Marian Udrescu and Max Tegmark (2019) `[Science Advances] <https://advances.sciencemag.org/content/6/16/eaay2631/tab-pdf>`_ and AI Feynman 2.0: Pareto-optimal symbolic regression exploiting graph modularity, Udrescu S.M. et al. (2020) `[arXiv] <https://arxiv.org/abs/2006.10782>`_.

Example usage::
  
  from feynman import run_aifeynman

  run_aifeynman("../example_data/", "example1.txt", 30,
                "14ops.txt", polyfit_deg=3, NN_epochs=500)

Where 'example1.txt' contains tab separated data that the regression is performed over, and '14ops.txt' contains the operations the regression is permitted to use.


Installation (From source)
==========================
Prereqs: (I made the numbers up)

* numpy (>= 1.15)
* torch (>= 1.0)
* wheel

Build distribution::

  python setup.py sdist

Install::

  pip install dist/feynman-2.0.0.tar.gz

Test::

  python examples/example.py

.. automodule:: feynman.S_run_aifeynman
   :members:
   


.. toctree::
   :maxdepth: 2
   :caption: Contents:
feynman


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
