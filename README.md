Lie Groups
==========

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/byu-magicc/lie_groups/master)

This repo houses an implementation-focused introduction to Lie Groups for roboticists. All material is written in Python and presented in Jupyter Notebook format. Start reading and interacting with the code online by clicking the binder badge above.

## Overview ##

The purpose of this repo is to present theory, tools, and examples of Lie groups and algebras for the practitioner working with the control, estimation, and optimization of rigid bodies.

To facilitate this, each chapter will present a section on using the group element to illustrate kinematics, solving differential equations, control, and estimation. We take the approach of starting with the unit circle (`S^1`) and working through more complicated spaces: `SE(2)`, `SO(3)`, `SE(3)`, and `SL(3)`.

## Motivation ##

Many interesting problems in control and estimation exist which can be solved by using "hacks" like wrapping Euler angles, normalizing quaternions at every step, etc. Alternatively, Lie theory can be applied to implement algorithms that do their work on the manifold (i.e., the surface of all 3D rotation matrices, `SO(3)`).

In particular, vision-based control and estimation is an active research area that employs the use of Lie groups and Lie algebras to leverage computationally efficient representations of rigid body transformations. Many state of the art algorithms in visual-inertial odometry, SLAM, and robust control use these concepts.
