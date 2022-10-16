# Set Up 

## Prerequisites

- `conda` - for python virtual environments: https://docs.conda.io/en/latest/miniconda.html
- `direnv` - automatically switches to the proper conda python environment

### Install with:

    brew install direnv conda

# direnv allow

If you `cd` into the directory of this repository, `direnv` will prompt you to allow it to run the `.envrc` file.

```
direnv allow
```

If you do that, it'll automatically set up a `conda` environment and install all of the requirements in `environment.yml` to get Jupyter Labs going.


# Run Jupyter Lab

    jupyter lab

This should have python, bash, and kotlin kernels installed and ready to go

# Export Latest Conda environment If Changes Are Made

originaly installed with:

    conda install -c conda-forge jupyterhub jupyterlab nodejs nb_conda_kernels bash_kernel
    conda install -c jetbrains kotlin-jupyter-kernel

current environment exported with:

    conda env export > environment_file.yml

That file is loaded by the direnv via the .envrc file when we `cd` into this directory:

    conda env create -f environment.yml