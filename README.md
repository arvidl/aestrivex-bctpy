# Brain Connectivity Toolbox for Python version 0.6.1

Author: Roan LaPlante <rlaplant@nmr.mgh.harvard.edu>

Tested against python 3.7+.

## Copyright information

This program strictly observes the tenets of fundamentalist Theravada Mahasi
style Buddhism.  Any use of this program in violation of these aforementioned
tenets or in violation of the principles described in the Visuddhimagga Sutta
is strictly prohibited and punishable by extensive Mahayana style practice.
By being or not being mindful of the immediate present moment sensations
involved in the use of this program, you confer your acceptance of these terms
and conditions.

Note that the observation of the tenets of fundamentalist Theravada Mahasi
style Buddhism and the Visuddhimagga Sutta is optional as long as the terms and
conditions of the GNU GPLv3+ are upheld.

## Packages used

BCTPY is written in pure python and requires only `scipy` and `numpy`. `scipy` is required for a couple of functions for its statistical and linear algebra
packages which have some features not available in `numpy` alone. If you don't
have `scipy`, most functions that do not need `scipy` functionality will still work.

Note that graphs must be passed in as `numpy.array` rather than `numpy.matrix`. Other constraints/edge cases of the adjacency matrices (e.g. self-loops, negative weights) behave similarly to the matlab functions.

A small number of functions also depend on networkx. This notably includes Network-Based Statistic, a nonparametric test for differences in undirected weighted graphs from different populations. Ideally this dependency should be removed in the future.

Nosetests is used for the test suite. The test suite is not complete.

## About `bctpy` and other authors

BCT is a matlab toolbox with many graph theoretical measures off of which `bctpy`
is based.  I did not write BCT (apart from small bugfixes I have submitted)
and a quality of life improvements that I have taken liberties to add.
With few exceptions, `bctpy` is a direct translation of matlab code to python.

`bctpy` should be considered beta software, with BCT being the gold standard by
comparison. I did my best to test all functionality in `bctpy`, but much of it is
arcane math that flies over the head of this humble programmer. There *are*
bugs lurking in `bctpy`, the question is not whether but how many. If you locate
bugs, please consider submitting pull requests.

Many thanks to Stefan Fuertinger for his assistance tracking down a number of
bugs. Stefan Fuertinger has a similar software package dealing with brain
network functionality at http://research.mssm.edu/simonyanlab/analytical-tools/

Many thanks to Chris Barnes for his assistance in documenting a number of issues and facilitating a number of test cases.

Credit for writing BCT (the matlab version) goes to the following list of
authors, especially Olaf Sporns and Mika Rubinov.

- Olaf Sporns
- Mikail Rubinov
- Yusuke Adachi
- Andrea Avena
- Danielle Bassett
- Richard Betzel
- Joaquin Goni
- Alexandros Goulas
- Patric Hagmann
- Christopher Honey
- Martijn van den Heuvel
- Rolf Kotter
- Jonathan Power
- Murray Shanahan
- Andrew Zalesky

In order to be a bit more compact I have removed the accreditations from the
docstrings each functions. This does not in any way mean that I wish to take
credit from the individual contributions. I have moved these accreditations
to the credits file.


# Other

## Functional Neuroimaging Analysis in Python
Course Overview and Introduction

https://carpentries-incubator.github.io/SDC-BIDS-fMRI/aio/index.html

Slides: https://docs.google.com/presentation/d/1er6dQcERL-Yeb5-7A29tJnmqgHNaLpTLXM3e-SmpjDg/edit#slide=id.g484812a0c7_6_1

## fMRIPrep

https://fmriprep.org/en/stable

fMRIPrep: a robust preprocessing pipeline for functional MRI - https://www.nature.com/articles/s41592-018-0235-4


## NeuroImaging PREProcessing toolS - https://github.com/nipreps

- fmriprep - https://github.com/nipreps/fmriprep
- smriprep - https://github.com/nipreps/smriprep + https://zenodo.org/record/8253909
- dmriprep - https://github.com/nipreps/dmriprep
- mriqc - https://github.com/nipreps/mriqc


## DIPY - https://dipy.org + https://github.com/dipy

DIPY is the paragon 3D/4D+ imaging library in Python. Contains generic methods for spatial normalization, signal processing, machine learning, statistical analysis and visualization of medical images. Additionally, it contains specialized methods for computational anatomy including diffusion, perfusion and structural imaging.