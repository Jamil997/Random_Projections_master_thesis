# Random Projection for Linear Programming

## Overview  
This project studies random‐projection methods to reduce constraint dimensions in large LPs and evaluates two recovery algorithms on both feasible and infeasible instance sets.

## Features  
- **Feasible Instances**  
  - Generator: `generate_feasible_problems(m, n, num_problems, density)`  
  - Projection: Gaussian random matrices of size \(k \times m\)  
  - Recovery:  
    1. Dual‐based (exact-solve)  
    2. Primal-based (pseudoinverse)  
  - Metrics: original vs. projected CPU time, feasibility error, objective error, negativity

- **Infeasible Instances**  
  - Generator: `generate_infeasible_problems(m, n, num_problems, density)`  
  - Projectors:  
    - Sparse \(\{\pm1,0\}\) random matrix  
    - Orthogonal via QR  
  - Metrics: original vs. projected CPU time, projection/multiplication/solve breakdown, misclassification rate (acc)

## Requirements  
```bash
pip install numpy scipy cvxpy pandas
