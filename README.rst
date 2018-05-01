Snakemake workflows for SBpipe
==============================

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
