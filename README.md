Cyclus Branching and Global Optimizations
==========================================

This is a public repository for the shared development of a publication on
Cyclus' restart and branching functionality and unique capability enabled by
its implementation.

Not Ready For Reuse
====================

During development, this work is owned solely by the authors until its final 
publication in an archival journal article. Derivatives of this work are not 
permitted until that time, at which point attribution will be necessary, 
accoring to its future license.

Notes
===============

Cyclus' branching feature enables cool things like:

1. Shortcutting simulations that have overlapping history with previously run
   simulations by starting from point in time where the two simulations diverge and making necessary
   perturbations before running only the time steps that differ.

2. Allows perturbation analysis of stochastic simulations. For example, a
   reactor facility might, with some probability shut down unexpectedly at some
   timestep. Branching enables perturbing a single realization of a simulation
   where that reactor went down at a certain time under specific circumstances
   and analyzing the alternative history.  Without restart, it is
   difficult/impossible to do this with internally stochastic simulations.

In addition to more boring things like:

* Pause a long simulation, move it to another computer, and restart it.

* Run a terminated simulation out farther into the future.

The paper will:

* discuss the above listed (and other?) benefits

* explain some of the implementation details necessary for this capability

* demonstrate the optimization performance value of point 1 above.

