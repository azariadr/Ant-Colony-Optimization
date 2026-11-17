# Ant Colony Optimization for Solving the Traveling Salesperson Problem

## Description

This project implements the Ant Colony Optimization (ACO) algorithm to solve the Traveling Salesperson Problem (TSP). The TSP is a classic optimization problem where the goal is to find the shortest possible route that visits a given set of cities and returns to the starting city. ACO is a metaheuristic inspired by the foraging behavior of ants, where ants deposit pheromones on the paths they travel, and subsequent ants are more likely to follow paths with higher pheromone concentrations.

## Problem Statement
We solve the TSP using a symmetric cost (distance) matrix representing the travel costs between 5 cities:

$$
\text{Distance Matrix } (d) = \begin{pmatrix}
0 & 10 & 12 & 11 & 14 \\
10 & 0 & 13 & 15 & 8 \\
12 & 13 & 0 & 9 & 14 \\
11 & 15 & 9 & 0 & 16 \\
14 & 8 & 14 & 16 & 0
\end{pmatrix}
$$

## Implementation

ACO is inspired by the foraging behavior of real ants. It uses artificial pheromone trails and heuristic information (visibility, which is the inverse of distance) to probabilistically build paths.
- **Parameters used in this project:**
  - Iterations: `100`
  - Number of Ants ($m$): `5`
  - Evaporation Rate ($\rho$): `0.1`
  - Pheromone Weight ($\alpha$): `1`
  - Heuristic Weight ($\beta$): `2`

## Results

The project demonstrates the effectiveness of the ACO algorithm in finding near-optimal solutions for the TSP. The results show the best route found, the total distance traveled, and the convergence behavior of the algorithm over time. 

- **Optimal Tour (1-based index):** `1 -> 2 -> 5 -> 3 -> 4 -> 1` (or its equivalent reverse)
- **Minimum Cost:** `52`

You can modify the parameters of the algorithm, such as the number of ants, the evaporation rate, and the pheromone influence, to explore their impact on the solution quality.
