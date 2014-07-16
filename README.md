branchopt-paper
===============

This paper will explain and demonstrate the power of Cyclus' restart+branching
capability.  This capability enables cool things like:

1. Shortcutting simulations that have overlapping history with previously run
   simulations by starting from point in time where the two simulations diverge and making necessary
   perturbations before running only the time steps that differ.

2. Allows perturbation analysis of stochastic simulations. For example, a
   reactor facility might, with some probability shut down unexpectedly at some
   timestep. Branching enables perturbing a single realization of a simulation
   where that reactor went down at a certain time under specific circumstances
   and analyzing the alternative history.  Without restart, it is
   difficult/impossible to do this with internally stochastic simulations.

The paper will:

* discuss the above listed (and other?) benefits

* explain some of the implementation details necessary for this capability

* demonstrate the optimization performance value of point 1 above.

