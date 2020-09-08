========
Usage
========

Quick start
===========
You may run::

    python examples/example.py

Internally, 'examples/example.py' looks like this::
  
  from feynman import run_aifeynman

  run_aifeynman("../example_data/", "example1.txt", 30,
                "14ops.txt", polyfit_deg=3, NN_epochs=500)

Where 'example1.txt' contains tab separated data that the regression is performed over, and '14ops.txt' contains the operations the regression is permitted to use.


Examples
========
ai_feynman_example.py contains an example of running the code on some examples (found in the example_data directory). The examples correspond to the equations I.8.14, I.10.7 and I.50.26 in Table 4 in `this paper <https://advances.sciencemag.org/content/6/16/eaay2631/tab-pdf>`_. More data files on which the code can be tested on can be found in the `Feynman symbolic regression dataset <https://space.mit.edu/home/tegmark/aifeynman.html>`_. 

Documentation
=============
.. autofunction:: feynman.run_aifeynman


The data file to be analyzed should be a text file with each column containing the numerical values of each (dependent and independent) variable. The solution file will be saved in the directory called "results" under the name solution_{filename}. The solution file will contain several rows (corresponding to each point on the Pareto frontier), each row showing: 

* the mean logarithm in based 2 of the error of the discovered equation applied to the input data (this can be though of as the average error in bits)
* the cummulative logarithm in based 2 of the error of the discovered equation applied to the input data (this can be though of as the cummulative error in bits)
* the complexity of the discovered equation (in bits)
* the error of the discovered equation applied to the input data
* the symbolic expression of the discovered equation

If test_percentage is different than zero, one more number is added in the beginning of each row, showing the error of the discovered equation on the test set.

For more information on input and output formats, see :doc:`inputformat` and :doc:`outputformat`
