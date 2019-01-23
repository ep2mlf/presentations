#  Machine learning determination of dynamical parameters: The Ising model case

## Introduction

Here are the slides accompanied by a short example notebook which together detail our statistical mechanics approach to Machine Learning. The overarching aim of our work is to better understand the fundamentals behind machine learning, using our knowledge of statistical mechanics.

## Installation

### Conda

Running the notebook should (hopefully) be quite easy. We recommend using conda to get up and running with the least amount of effort. Conda is a package manager which comes with an installation of Anaconda or Miniconda. The two are almost identical however Anaconda's base environment comes with lots of preinstalled packages so takes up more space off the bat. If you just want to use conda to manage your packages/environments without being burdened with all of these packages then Miniconda might be a better option. Installation instructions can be found here:

- (Miniconda) https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html
- (Anaconda) https://docs.continuum.io/anaconda/install/

If you are using `conda` then you can create an environment to use this notebook by entering the following commands:

```
# Create new environment with some of the required packages
conda create -n rbmtalk python=3 matplotlib tqdm jupyter
# Install Pytorch
conda install pytorch torchvision -c pytorch
```

### Compiling the metropolis code

Compiling the metropolis code (which we will use to generate data) should be as easy as typing

```
rbm_talk$ make
```

## Running Code

Once you have compiled the metropolis code and have a python environment with the necessary packages installed. You need to generate the training data. This is achieved simply by running

```
rbm_talk$ ./metro
```

The metropolis algorithm is a well documented algorithm which can be used in the case of the Ising model to generate ensembles of states which are distributed according to the probability distribution defined in the slides (slide 9). The states are represented by vectors of zeros and ones where each number is the state of an individual spin, either spin up (one) or spin down (zero). If you want to know more about the Ising model then the Wikipedia page is quite easy to follow: https://en.wikipedia.org/wiki/Ising_model

Once you have your states you're ready to run the notebook, whilst in this directory just run
```
rbm_talk$ jupyter notebook rbm.ipynb
```

and have a play! Hopefully you can see roughly what we have done with the slides alongside the notebook but if you have any questions please don't hesitate to email either

Tommaso Giani: s1792848@staffmail.ed.ac.uk
Michael Wilson: michael.wilson@ed.ac.uk