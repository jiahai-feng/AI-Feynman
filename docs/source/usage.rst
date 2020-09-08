========
Basic Usage
========

You may run::

    python examples/example.py

Internally, 'examples/example.py' looks like this::
  
  from feynman import run_aifeynman

  run_aifeynman("../example_data/", "example1.txt", 30,
                "14ops.txt", polyfit_deg=3, NN_epochs=500)

Where 'example1.txt' contains tab separated data that the regression is performed over, and '14ops.txt' contains the operations the regression is permitted to use.

