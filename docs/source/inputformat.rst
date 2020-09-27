.. _inputformat:

============
Input format
============

Mystery file
============
We expect the mystery file to be a text file which columns are delimited by spaces, tabs or commas. Each row contains D + 1 floats, and describes a data point. The first D floats are the values describing the independent variables in the data point, and the last float describes the dependent variable for the data point. If you're using numpy, `numpy.savetxt` should output a valid file format. Here's a small example that creates a mystery file for y = a + b + c::

    import numpy as np
    X = np.random.rand(100, 3)
    y = np.sum(X, axis=1)
    data = np.concatenate((X,y[:, np.newaxis]), axis=1)
    np.savetxt('mystery.txt', data)

Operations file
===============

The ops file contains a single line with the basic functions that the brute force search tries

.. code-block:: text
 
    Binary:
    +: add
    *: multiply
    -: subtract
    D: divide        (Put "D" instead of "/" in ops file, since f77 can't load it)

    Unary:
    >: increment    (x -> x+1) 
    <: decrement    (x -> x-1)
    ~: negate       (x-> -x)
    I: invert       (x->1/x) (Put "I" instead of "\" in file, since f77 can't load it)
    L: logaritm:    (x-> ln(x)
    E: exponentiate (x->exp(x))
    S: sin:         (x->sin(x))       
    C: cos:         (x->cos(x))       
    A: abs:         (x->abs(x))
    N: arcsin:      (x->arcsin(x))
    T: arctan:      (x->arctan(x))
    R: sqrt         (x->sqrt(x))
    O: double       (x->2*x); note that this is the letter "O", not zero
    J: double+1     (x->2*x+1)
    M: dilogarithm  (x -> Li_2(x); a k a Spence functions)

    nonary: 
    0
    1
    P = pi
    a, b, c, ...: input variables for function (auto-defined and should not be listed in ops file)

For example, 7ops.txt contains the string " +*D>~R0" which means that brute force tries combinations of addition, multiplication, division, incrementation, negation, square root and zero.
