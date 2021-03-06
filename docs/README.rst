What is Studio?
==============

|Hex.pm|

Studio is a model management framework written in Python to help simplify and expedite your model building experience. It was developed to minimize the overhead involved with scheduling, running, monitoring and managing artifacts of your machine learning experiments. No one wants to spend their time configuring different machines, setting up dependencies, or playing archeologist to track down previous model artifacts.

Most of the features are compatible with any Python machine learning
framework (`Keras <https://github.com/fchollet/keras>`__,
`TensorFlow <https://github.com/tensorflow/tensorflow>`__,
`PyTorch <https://github.com/pytorch/pytorch>`__,
`scikit-learn <https://github.com/scikit-learn/scikit-learn>`__, etc);
some extra features are available for Keras and TensorFlow.

**Use Studio to:** 

* Capture experiment information- Python environment, files, dependencies and logs- without modifying the experiment code. 
* Monitor and organize experiments using a web dashboard that integrates with TensorBoard. 
* Run experiments locally, remotely, or in the cloud (Google Cloud or Amazon EC2) 
* Manage artifacts
* Perform hyperparameter search
* Create customizable Python environments for remote workers.

Example usage
-------------

Start visualizer:

::

    studio ui

Run your job:

::

    studio run train_mnist_keras.py

You can see the results of your job at http://127.0.0.1:5000. Run
``studio {ui|run} --help`` for a full list of ui / runner options

Installation
------------

pip install ``studioml`` from the master pypi repositry:

::

    pip install studioml

Find more `details <http://docs.studio.ml/en/latest/installation.html>`__ on installation methods and the release process. 

Authentication
--------------

Currently Studio supports 2 methods of authentication: `email / password <http://docs.studio.ml/en/latest/authentication.html#email--password-authentication>`__ and using a `Google account. <http://docs.studio.ml/en/latest/authentication.html#google-account-authentication>`__ To use ``studio run`` and ``studio ui`` in guest
mode, in studio/default\_config.yaml, uncomment "guest: true" under the
database section.

Alternatively, you can set up your own database and configure Studio to
use it. See `setting up database <http://docs.studio.ml/en/latest/setup_database.html>`__. This is the
preferred option if you want to keep your models and artifacts private.


Further reading and cool features
---------------------------------

-  `Running experiments remotely <http://docs.studio.ml/en/latest/remote_worker.html>`__
   
   -  `Custom Python environments for remote workers <http://docs.studio.ml/en/latest/customenv.html>`__

-  `Running experiments in the cloud <http://docs.studio.ml/en/latest/cloud.html>`__

   -  `Google Cloud setup instructions <http://docs.studio.ml/en/latest/gcloud_setup.html>`__

   -  `Amazon EC2 setup instructions <http://docs.studio.ml/en/latest/ec2_setup.html>`__

-  `Artifact management <http://docs.studio.ml/en/latest/artifacts.html>`__
-  `Hyperparameter search <http://docs.studio.ml/en/latest/hyperparams.html>`__
-  `Pipeline for trained models <http://docs.studio.ml/en/latest/model_pipelines.html>`__

.. |Hex.pm| image:: https://img.shields.io/hexpm/l/plug.svg
   :target: https://github.com/studioml/studio/blob/master/LICENSE
