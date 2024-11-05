# Bempp acoustics exercises

This repository contains tutorials and exercises designed to show you how to use Bempp to solve problems in acoustics. It has been prepared for the [ASSA Autumn School Series in Acoustics 2024](https://assaeindhoven.org/), which included a Computational Acoustics stream with a day on Boundary Element Method taught by [Dr Jonathan A. Hargreaves](https://salford-repository.worktribe.com/person/1159647/jonathan-hargreaves). It is a subset of (with some slight adaptions) the materials in [this reposity](https://github.com/mscroggs/bempp-acoustic-tutorials), which was prepared with [Matthew Scroggs](https://orcid.org/0000-0002-4658-2443) for the [EAA / UKAN Computational Acoustics Summer School](https://acoustics.ac.uk/events/4468/) in 2021. They have all been created in [Jupyter Notebooks](https://jupyter.org/), which allow you to see code, explanation and results all alongside.

You can view these tutorials and exercises [on nbviewer](https://nbviewer.jupyter.org/github/jahargreaves/bempp-acoustic-tutorials-assa/blob/main/README.ipynb) without needing to install Bempp. But if you wish to make any edits yourself, as is required to undertake the exercises, then you'll need to [install Bempp](tutorials/0_install.ipynb) and either clone the repository or download the code (achieved via the green <i>Code</i> button above right).

## Contents
- [Instructions for installing Bempp](tutorials/0_install.ipynb)
- Using the null field approach (an indirect BEM formulation that follows Jonathan Hargreaves' explanation in the lectures)
  - [Tutorial 1: Scattering from a rigid sphere using a null field approach](tutorials/1_sphere_scatterer_null_field.ipynb)
  - [Exercise 1: Uniqueness](exercises/1_uniqueness.ipynb)
- Alternative Direct formulation by Matthew Scroggs
  - [Tutorial 2: Scattering from a rigid sphere using a direct formulation](tutorials/2_sphere_scatterer_direct.ipynb)
  - Checking performance
  - [Tutorial 3: Convergence rates](tutorials/3_convergence.ipynb)
  - [Exercise 3: Iteration counts](exercises/3_iterations.ipynb)
- Impedence boundary conditions
  - [Tutorial 4: Scattering from a impedence sphere](tutorials/4_impedence_scattering.ipynb)
- Radiation Problems
  - [Tutorial 5: Loudspeaker radiation](tutorials/5_loudspeaker.ipynb)
- [Further information](tutorials/7_more.ipynb)


## Notation differences between these tutorials and the Bempp documentation
The bempp website includes a [handbook](https://bempp.com/handbook/index.html), which gives an introduction to how the library operates, and [automatically generated full Python documentation](https://bempp-cl.readthedocs.io/en/latest/), which is useful for looking up specific details once you already understand the main principles for using Bempp. But that documentation uses a different operator notation to what is used in these tutorials, which follow the Jonathan Hargreaves's slides from the summer school.

Here is a summary of the differences:

Operator | Notation used herein | Notation used in Bempp documentation
-------- | -------------------- | ------------------------------------
Identity | I                    | Id
Single layer | S                | V
Double layer | D                | K
Adjoint double layer | A        | K'
Hypersingular | H               | W
