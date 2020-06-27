## About

This repository is where I play around with Quantum Programming, especially by using Ocean that is a software which is a suite of tools D-Wave Systems provides on the D-Wave GitHub repository for solving hard problems with quantum computers.

- [Original repository of Ocean](https://docs.ocean.dwavesys.com/en/stable/index.html)
- [The documentation of Ocean](https://docs.ocean.dwavesys.com/en/stable/index.html)

## Formulate our problems

- We need to formulate problems we want to solve as a <strong>Binary Quadratic Model (BQM)</strong>.
- In order to solve a BQM, we need to define an objective function which would be <strong>[Quadratic Unstractured Binary Optimization (QUBO)](https://docs.ocean.dwavesys.com/projects/dimod/en/stable/reference/bqm/binary_quadratic_model.html?highlight=QUBO)</strong> or <strong>[Ising](https://docs.ocean.dwavesys.com/projects/dimod/en/stable/reference/bqm/binary_quadratic_model.html?highlight=QUBO)</strong>.
  By finding the values that minimizes the objective function, we solve the BQM.
- A BQM equation has two parts:
  - Objective: What we are trying to minimize
  - Constraints: Rules we need to satisfy

## BQM Development Process

1. Convert our objective and constraints to math statements with binary variables if we picked QUBO as an objective function or -1/+1 variables if Ising.

2. Make our objective and constraints "QUBO appropreate".

   - Objective is a minimizing function
   - Constraints are satisfied at thier minimum values

3. Combine our objective and constraints.

## Setup environment

1. Create an env
2. Install Ocean into the env you just created.
   `pip install dwave-ocean-sdk`
3. Type `dwave setup` to setup a config file.

For more details, see the [Ocean documentation](https://docs.ocean.dwavesys.com/en/stable/overview/install.html)
