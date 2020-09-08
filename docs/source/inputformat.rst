.. _inputformat:

============
Input format
============

Mystery file
============
We expect the mystery file to be a space-separated text document. Each row contains D + 1 floats, and describes a data point. The first D floats are the values describing the independent variables in the data point, and the last float describes the dependent variable for the data point. If you're using numpy, `numpy.savetxt` should output a valid file format. Here's a small example that creates a mystery file for y = a + b + c::

    import numpy as np
    X = np.random.rand(100, 3)
    y = np.sum(X, axis=1)
    data = np.concatenate((X,y[:, np.newaxis]), axis=1)
    np.savetxt('mystery.txt', data)

Operations file
===============
