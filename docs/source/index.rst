AI Feynman
==========


This code is an improved implementation of AI Feynman: a Physics-Inspired Method for Symbolic Regression, Silviu-Marian Udrescu and Max Tegmark (2019) `[Science Advances] <https://advances.sciencemag.org/content/6/16/eaay2631/tab-pdf>`_ and AI Feynman 2.0: Pareto-optimal symbolic regression exploiting graph modularity, Udrescu S.M. et al. (2020) `[arXiv] <https://arxiv.org/abs/2006.10782>`_.


Please check `this Medium article <https://towardsdatascience.com/ai-feynman-2-0-learning-regression-equations-from-data-3232151bd929>`_ for a more detailed explanation of how to get the code running.


Example usage::
  
  from feynman import run_aifeynman

  run_aifeynman("../example_data/", "example1.txt", 30,
                "14ops.txt", polyfit_deg=3, NN_epochs=500)

Where 'example1.txt' contains tab separated data that the regression is performed over, and '14ops.txt' contains the operations the regression is permitted to use.


Install::

   pip install aifeynman

Run::

  python examples/example.py


.. toctree::
   :hidden:
   :maxdepth: 1

   installation
   usage
   inputformat
   outputformat
   faq

