==========================
FAQ
==========================

What is AI Feynman?
**************************
AI Feynman is a symbolic regression software that achieves the state of the art on the `Feynman symbolic regression dataset <https://space.mit.edu/home/tegmark/aifeynman.html>`_. It is an improved implementation of AI Feynman: a Physics-Inspired Method for Symbolic Regression, Silviu-Marian Udrescu and Max Tegmark (2019) `[Science Advances] <https://advances.sciencemag.org/content/6/16/eaay2631/tab-pdf>`_ and AI Feynman 2.0: Pareto-optimal symbolic regression exploiting graph modularity, Udrescu S.M. et al. (2020) `[arXiv] <https://arxiv.org/abs/2006.10782>`_.

Where are the results stored?
*********************************
A sub-directory will be created at the current directory called 'results'. Under that directory, you'd find a solution file 'solution_{filename}' where {filename} is the filename provided to the launch function. See :doc:`usage` for more information

I am getting Fortran or C++ compilation issues.
**********************************************************
You might be missing the relevant compiler. On Ubuntu, to install the Fortran compiler you can run:
    apt-get install gfortran

For the C++ compiler you can run:
    apt-get install build-essential


How do I cite AI Feynman?
********************************
If you compare with, build on, or use aspects of the AI Feynman work, please cite the following::

    @article{udrescu2020ai,
        title={AI Feynman: A physics-inspired method for symbolic regression},
        author={Udrescu, Silviu-Marian and Tegmark, Max},
        journal={Science Advances},
        volume={6},
        number={16},
        pages={eaay2631},
        year={2020},
        publisher={American Association for the Advancement of Science}
    }