========
Usage
========

Documentation
=============
.. py:function:: aifeynman.launch(pathdir, filename, [BF_try_time=60], [BF_ops_file_type='14ops.txt'], [polyfit_deg=4], [NN_epochs=4000], [vars_name=[]], [test_percentage=0])

    Runs AI Feynman. Saves the solutions to results/ directory to the file results/solution_{filename}. Parameters in [square brackets] are optional.

    :param pathdir: path to the directory containing the data file
    :type pathdir: str
    :param filename: the name of the file containing the data
    :type filename: str
    :param BF_try_time: time limit in seconds for each brute force call (default is 60 seconds)
    :type BF_try_time: float
    :param BF_ops_file_type: file containing the symbols to be used in the brute force code (default is "14ops.txt")
    :type BF_ops_file_type: str
    :param polyfit_deg:  maximum degree of the polynomial tried by the polynomial fit routine (default is 4)
    :type polyfit_deg: int
    :param NN_epochs: number of epochs for the training (default is 4000)
    :type NN_epochs: int
    :param vars_name: name of the variables appearing in the equation (including the name ofthe output variable). This should be passed as a list of strings, with the name of the variables appearing in the same order as in the input data
    :type vars_name: [str]
    :param test_percentage: percentage of the input data to be kept aside and used as a test set
    :type test_percentage: float

The data file to be analyzed should be a text file with each column containing the numerical values of each (dependent and independent) variable. The solution file will be saved in the directory called "results" under the name solution_{filename}. The solution file will contain several rows (corresponding to each point on the Pareto frontier), each row showing: 

* the mean logarithm in based 2 of the error of the discovered equation applied to the input data (this can be though of as the average error in bits)
* the cummulative logarithm in based 2 of the error of the discovered equation applied to the input data (this can be though of as the cummulative error in bits)
* the complexity of the discovered equation (in bits)
* the error of the discovered equation applied to the input data
* the symbolic expression of the discovered equation

If test_percentage is different than zero, one more number is added in the beginning of each row, showing the error of the discovered equation on the test set.

For more information on input and output formats, see :doc:`inputformat` and :doc:`outputformat`
