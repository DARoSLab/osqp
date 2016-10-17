# Operator Splitting QP Solver

Python implementation of the operator splitting QP solver for problems in the form
```
minimize        x'Qx + c'x
subject to      Aeq x = beq
                Aineq x <= bineq
                l <= x <= u
```

## TODO

- [x] Stopping criterion
- [ ] Do preconditioning/equilibration
- [ ] JIT Compilation (Numba ?) to speedup results: numba does not work well
- [x] Timer and compare to other QP solvers
- [ ] Presolver
- [ ] Infeasibility detection:
    - Generalize [result](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=7040300) to non strongly convex problems
- [ ] Unboundedness detection
- [ ] Stepsize selection: maybe choose
- [x] Warm starting
- [ ] Polishing:
    - It works but not very robust yet
    - See [this article](https://arxiv.org/pdf/1609.07478.pdf)
- [ ] Add testing script

## Problems
- [ ] Maros and Meszaros Test set: CVXQP1_S.mat --> Need 50k iterations to converge!

## Test Problems

- QPLIB2014 http://www.lamsade.dauphine.fr/QPlib2014/doku.php
- Maros and Meszaros Convex Quadratic Programming Test Problem Set: https://github.com/YimingYAN/QP-Test-Problems