Snakemake workflows for SBpipe
==============================

|Build Status| |MIT License| |SBpipe| |sbpiper| |Snakemake|

This repository contains the `Snakemake`_ workflows for the `SBpipe`_ project.
The workflows are for model parameter estimation (pe), simulation (sim), 
single parameter scan (ps1), and double parameter scan (ps2).

:: 

    # clone workflow into working directory
    git clone https://github.com/pdp10/sbpipe_snake.git path/to/workdir
    cd path/to/workdir

    # edit config_[sim|ps1|ps2|pe].yaml as needed
    # vim config.yaml

    # execute workflow, deploy software dependencies via conda
    # e.g. parameter estimation workflow
    snakemake -s sbpipe_pe.snake --configfile config_pe.yaml


In order to run these workflows, `SBpipe`_ must be installed.

Conda users can automatically install the worflow dependencies using the provided `environment.yaml` file:

::
    
    # install dependencies into isolated environment
    conda env create -n myworkflow --file environment.yaml

    # activate environment
    source activate myworkflow


.. _Snakemake: https://snakemake.readthedocs.io
.. _SBpipe: https://github.com/pdp10/sbpipe

.. |Build Status| image:: https://travis-ci.org/pdp10/sbpipe.svg?branch=master
   :target: https://travis-ci.org/pdp10/sbpipe
.. |MIT License| image:: http://img.shields.io/badge/license-MIT-blue.svg
   :target: https://opensource.org/licenses/MIT
.. |SBpipe| image:: https://img.shields.io/badge/sbpipe-≥4.18.0-brightgreen.svg?style=flat-square
   :target: https://sbpipe.bitbucket.io
.. |sbpiper| image:: https://img.shields.io/badge/sbpiper-≥1.8.0-brightgreen.svg?style=flat-square
   :target: https://cran.r-project.org/package=sbpiper
.. |Snakemake| image:: https://img.shields.io/badge/snakemake-≥4.8.1-brightgreen.svg?style=flat-square
   :target: https://snakemake.bitbucket.io
