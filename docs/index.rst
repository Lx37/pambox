pambox
======

`pambox <https://github.com/achabotl/pambox>`_ is a Python toolbox to
facilitate the development of auditory models, with a focus on speech
intelligibility prediction models.

The Grand Idea is for `pambox` to be a repository of published auditory models,
as well as a simple and powerful tool for developing auditory models.
Components should be reusable and easy to modify.
`pambox` uses a standard interface for all speech intelligibility prediction
models in the toolbox, which should simplify comparisons across models.

In case Python is not your thing and you prefer Matlab, the `Auditory Modeling
Toolbox <http://amtoolbox.sourceforge.net>`_ is an excellent alternative.

Installing
----------

Right now, `pambox` is only available through Github. It should be available
via `pip` soon. To install `pambox` from source::

    git clone https://github.com/achabotl/pambox.git
    cd pambox
    python setup.py install

You'll also need all the requirements in `requirements.txt <https://github
.com/achabotl/pambox/blob/develop/requirements.txt>`_. If you use `conda
<https://store.continuum.io/cshop/anaconda/>`_, you can simply run the
following to install all the dependencies::

    conda install --file requirements.txt


Structure of the toolbox
------------------------

The structure of the toolbox is inspired by the auditory system. The classes
and functions are split between "peripheral" and "central" parts. The
"peripheral" part is directly accessible through an :mod:`~pambox.inner`,
a :mod:`~pambox.middle`, and an :mod:`~pambox.outer` module.
The :mod:`~pambox.central` part is more general and contains the
modules and functions for central processes, without much extra separation
for now.

The :mod:`~pambox.speech` module contains speech intelligibility models and
various functions and classes to facilitate speech intelligibility prediction
experiments.

The :mod:`~pambox.utils` module contains functions for manipulating
signals, such as setting levels, or padding signals, that are not directly
auditory processes.

The :mod:`~pambox.distort` module contains distortions and processes that
can be applied to signals. Most of them are used in speech intelligibility
experiments.

The :mod:`~pambox.audio` module is a thin wrapper around `pyaudio
<http://people.csail.mit.edu/hubert/pyaudio/>`_ that simplifies the playback of
numpy arrays, which is often useful for debugging.

Contents
--------

.. toctree::
  :maxdepth: 2

  audio/index
  inner/index
  middle/index
  outer/index
  central/index
  speech/index
  distort/index
  utils/index


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

