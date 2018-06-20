Lie Groups
==========

[![nbviewer](https://cdn.rawgit.com/jupyter/design/master/logos/Badges/nbviewer_badge.svg)](http://nbviewer.jupyter.org/github/byu-magicc/lie_groups/) [![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/byu-magicc/lie_groups/master)

This repo houses an implementation-focused introduction to Lie Groups for roboticists. All material is written in Python and presented in Jupyter Notebook format.

For the best experience, start reading online with `nbviewer` or interacting with the code using `binder` by clicking the appropriate badge above. Alternatively, follow the *Getting Started* instructions below to run the notebook on your local machine.

## Overview ##

The purpose of this repo is to present theory, tools, and examples of Lie groups and algebras for the practitioner working with the control, estimation, and optimization of rigid bodies.

To facilitate this, each chapter will present a section on using the group element to illustrate kinematics, solving differential equations, control, and estimation. We take the approach of starting with the unit circle (`S^1`) and working through more complicated spaces: `SE(2)`, `SO(3)`, `SE(3)`, and `SL(3)`.

## Motivation ##

Many interesting problems in control and estimation exist which can be solved by using "hacks" like wrapping Euler angles, normalizing quaternions at every step, etc. Alternatively, Lie theory can be applied to implement algorithms that do their work on the manifold (i.e., the surface of all 3D rotation matrices, `SO(3)`).

In particular, vision-based control and estimation is an active research area that employs the use of Lie groups and Lie algebras to leverage computationally efficient representations of rigid body transformations. Many state of the art algorithms in visual-inertial odometry, SLAM, and robust control use these concepts.

## Getting Started ##

To get started improving and learning with these notebooks, make sure you have Jupyter installed:

```bash
$ pip install jupyter --user
```

After cloning this repo and navigating into its directory on your machine, kick off the Jupyter notebook server with:

```bash
$ jupyter notebook
```

The server will start and a new browser tab will open.

For more information on Python/pip, see [here](https://magiccvs.byu.edu/wiki/#!sw_guides/python.md).

You will also need `ffmpeg` installed to render matplotlib animations as inline videos. On Ubuntu, this is accomplished with

```bash
sudo apt install ffmpeg
```

For other operating systems, refer to the documentation [here](https://www.ffmpeg.org/) or [here](https://github.com/adaptlearning/adapt_authoring/wiki/Installing-FFmpeg).

## Handling Merge Conflicts: `nbdime` ##

Because Jupyter notebook are difficult to parse as raw text, the [`nbdime`](https://nbdime.readthedocs.io/en/stable/installing.html) tool was created to help graphically manage merge conflicts. Install using `pip` with

```bash
$ pip install -U nbdime
```

and make sure to integrate with `git` using `nbdime config-git --enable --global`. This will allow `git diff` to use `nbdime`'s command-line diff interface for any `*.ipynb` files. Alternatively, you can use `nbdiff-web` to compare Jupyter notebooks graphically.

See the `nbdime` [docs ](https://nbdime.readthedocs.io/en/stable/vcs.html) to read more about `git` integration and using `nbdime` as the merge tool.
