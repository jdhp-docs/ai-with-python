.. warning:: Please note that at this time, this document is a work in progress that is not intended to be read by anyone other than its authors.

Machine Learning frameworks
===========================

Tensorflow
----------

- Google
- https://www.tensorflow.org/

Scikit-learn
------------

- Machine learning
- http://scikit-learn.org/

SciPy
-----

- https://www.scipy.org/
- My snippets: https://github.com/jeremiedecock/snippets/tree/master/python/scipy

Theano
------

- http://deeplearning.net/software/theano/
 
Pylearn2
--------

- Deeplearning
- Development status: stopped (almost no commit in 2016)
- Web site: http://deeplearning.net/software/pylearn2/
- Source code: https://github.com/lisa-lab/pylearn2

Quick and dirty bootstrap
'''''''''''''''''''''''''

Install dependencies::

    conda install theano
    conda install nose-parameterized
    mkdir ~/pylearn2_data

Set PYLEARN2_DATA_PATH in ~/.bash_profile (MacOS)::

    export PYLEARN2_DATA_PATH="/Users/jdecock/pylearn2_data"
    export PYLEARN2_VIEWER_COMMAND="open -Wn"

Then run::

    source ~/.bash_profile

Install pylearn2 (see http://deeplearning.net/software/pylearn2/index.html#download-and-installation)::

    mkdir -p ~/bin/
    cd ~/bin/
    git clone git://github.com/lisa-lab/pylearn2.git
    cd pylearn2
    python setup.py develop --user

Run the first tutorial (see ~/bin/pylearn2/pylearn2/scripts/tutorials/grbm_smd/README):

..code:: bash

    # Download the CIFAR10 dataset
    cd ~/bin/pylearn2/pylearn2/scripts/datasets
    ./download_cifar10.sh
    
    # Make the dataset
    cd ~/bin/pylearn2/pylearn2/scripts/tutorials/grbm_smd
    python make_dataset.py
    
    # Train the model
    ~/bin/pylearn2/pylearn2/scripts/train.py cifar_grbm_smd.yaml
    
    # Show results
    ~/bin/pylearn2/pylearn2/scripts/show_weights.py cifar_grbm_smd.pkl
    ~/bin/pylearn2/pylearn2/scripts/plot_monitor.py cifar_grbm_smd.pkl

Blocks
------

- http://blocks.readthedocs.io/en/latest/

Keras
-----

- https://keras.io/

Lasagne
-------

- http://lasagne.readthedocs.io/en/latest/

MILK
----

- Utilisé par pylearn2 pour K-means
- https://pythonhosted.org/milk/
- Source code: https://github.com/luispedro/milk/
- Development status: stopped ? (no commit in 2016)

Features:

- LASSO
- Random forests
- Self organising maps
- SVMs (using the libsvm solver with a pythonesque wrapper around it)
- Stepwise Discriminant Analysis for feature selection
- Non-negative matrix factorisation
- K-means using as little memory as possible
- Affinity propagation

See also
--------

- http://deeplearning.net/software_links/


Machine Learning Benchmarks and Datasets
========================================

Reference datasets:

- MNIST
- CIFAR-10
- CIFAR-100
- SVHN

