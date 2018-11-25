# Environment Configuration

**Presented by:** 
 x Nehal Soni
 x Vishal Rangras

For *Image Processing and Computer Vision* track, python will be used as programming language along with various libraries and frameworks useful. The dependency management in Python can be best handled using Anaconda and it comes with many powerful features, Jupyter Notebook being one of those. We will extensively use Anaconda so instructions to setup the same are provided below:

As per the Anaconda [docs](http://conda.pydata.org/docs):

> Conda is an open source package management system and environment management system 
for installing multiple versions of software packages and their dependencies and 
switching easily between them. It works on Linux, OS X and Windows, and was created 
for Python programs but can package and distribute any software.

## Overview
We need to follow 3 simple steps to get our environment up and running:

1. Install [`Anaconda`](https://www.continuum.io/downloads) on your computer from direct [link](https://www.continuum.io/downloads) or from "\\\\192.168.102.226\\Software\\AI Community\\Software" location if you are in the Cignex's network.
2. Follow the environment setup instructions below to create a new `conda` [environment](http://conda.pydata.org/docs/using/envs.html)
3. Each time you wish to work, activate your `conda` environment. Easy peasy!

## Installation

**Download** the version of `Anaconda` that matches your system from https://www.continuum.io/downloads

## Create Environment

**Pre-requisite:** You must have git installed in your system and added to the Path variable.

**Setup:** Start Anaconda prompt. Execute the following commands to create a new `conda` environment, in which, we will add required dependencies.

```sh
conda update conda
conda create -n cv_env python=3.6.6 anaconda
conda env list   # To list all the available environments. Ensure that your environment cv_env is listed here.
activate cv_env  # Command for Windows
source activate cv_env  # Command for Linux
pip install --upgrade opencv-python # To install opencv
pip install -q -U opencv-python # Try this if the above one doesn't work
pip install imutils  # This is a helper library for image processing
conda list  # To list all the available packages in your environment. See if this list returns opencv and imutils or not, it should.
```

## Anaconda Commands

| Sr. No. | Command  | Usage |
|---|---|---|
| 1 |conda update conda|To update Anaconda|
| 2 |conda create -n <<env_name>> python=<<x.x>> anaconda|To create new environment with a given name and python version|
| 3 |activate <<env_name>> or source activate <<env_name>>|To activate your environment|
| 4 |deactivate or source deactivate|To deactivate an environment|
| 5 |conda install -n <<env_name>> [package_name]|To install a package in given environment.|
| 6 |conda install -c <<channel_name>> -n <<env_name>> [package_name]|To install binaries from a given channel|
| 7 |conda env list|To list all the available environments in your system|
| 8 |conda list|To see packages installed in your environment|
| 9 |conda remove -n <<env_name>> - all|To remove an environment|
| 10 |conda clean -tp|To clean up tarball files after environment setup is completed|
| 11 |jupyter notebook <<notebookname.ipynb>>|To run a jupyter notebook|