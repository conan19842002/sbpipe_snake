Snakemake workflows for SBpipe
==============================

|Build Status| |MIT License| |SBpipe| |sbpiper| |Snakemake|

This repository contains the `Snakemake`_ workflows for the `SBpipe`_ project.
The workflows are:

- parameter estimation (pe)
- simulation (sim)
- single parameter scan (ps1)
- double parameter scan (ps2)


To run these workflows `SBpipe`_ and `Snakemake`_ must be installed.

- `non-Miniconda users`: see the documentation to install these packages
- `Miniconda users`: see below

Therefore:

::

    # clone workflow into working directory
    git clone https://github.com/pdp10/sbpipe_snake.git project_name
    cd project_name

    ######################
    # Miniconda users ONLY
    # install dependencies into isolated environment
    conda env create -n sbpipe_snake --file environment.yaml

    # activate environment
    conda activate sbpipe_snake
    ######################

    # create a folder Models and populate it with
    # the mathematical models (see `SBpipe`_) to run.
    mkdir Models

    # edit config_[sim|ps1|ps2|pe].yaml as needed for your models
    # e.g. for model simulation
    vim config_sim.yaml

    # execute workflow, deploy software dependencies via conda
    # e.g. parameter estimation workflow
    snakemake -s sbpipe_sim.snake --configfile config_sim.yaml


.. _Snakemake: https://snakemake.readthedocs.io
.. _SBpipe: https://github.com/pdp10/sbpipe

.. |Build Status| image:: https://travis-ci.org/pdp10/sbpipe.svg?branch=master
   :target: https://travis-ci.org/pdp10/sbpipe
.. |MIT License| image:: http://img.shields.io/badge/license-MIT-blue.svg
   :target: https://opensource.org/licenses/MIT
.. |SBpipe| image:: https://img.shields.io/badge/sbpipe-≥4.18.0-brightgreen.svg?style=flat-square
   :target: http://sbpipe.readthedocs.io
.. |sbpiper| image:: https://img.shields.io/badge/sbpiper-≥1.8.0-brightgreen.svg?style=flat-square
   :target: https://cran.r-project.org/package=sbpiper
.. |Snakemake| image:: https://img.shields.io/badge/snakemake-≥4.8.1-brightgreen.svg?style=flat-square
   :target: https://snakemake.bitbucket.io
