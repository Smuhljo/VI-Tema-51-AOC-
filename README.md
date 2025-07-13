# Ant Colony Optimization (ACO) - Manual Implementation for Solving TSP

Course: Artificial Intelligence
Academic Year: 2024/2025
Students:

Bakir Vreto (ID: 19140)

Faruk Baković (ID: 19186)

Muhamed Selmanović (ID: 19115)

📌 Project Overview
This project presents a manual (from scratch) implementation of the Ant Colony Optimization (ACO) algorithm for solving the Travelling Salesman Problem (TSP). The goal is to gain a deeper understanding of bio-inspired optimization algorithms, pheromone dynamics, and the balance between exploration and exploitation.

🔍 Problem Description
Given a dataset of 30 cities (USA), the aim is to find the shortest possible route that visits all cities once and returns to the starting point. ACO is used as the solution method, mimicking real-world ant behavior to discover near-optimal solutions.

🛠️ Technologies Used
Programming Language: Python 3.10
Environment: Jupyter Notebook (Google Colab)
Libraries: NumPy, Matplotlib


🔄 Algorithm Flow
Initialization
  Load city coordinates and compute distance & heuristic matrices.
Ant Movement
  Each ant builds a path using a probabilistic decision rule based on pheromones and distance.
Pheromone Update
  After each round trip, pheromones are updated based on path quality.
Iterations
  The process repeats for T=1000 iterations or until convergence.
Stopping Conditions
  Time limit, stagnation detection, or number of successful tours.

| Parameter            | Value                |
| -------------------- | -------------------- |
| ant\_count           | 30                   |
| iterations (T)       | 1000                 |
| pheromone\_power (β) | 1.25                 |
| distance\_power (α)  | 2.0                  |
| reward\_power        | 0                    |
| min\_ants            | 5                    |
| ant\_speed           | median\_distance / 5 |

📈 Results & Performance
Best Result (30 cities): ~4.3% error from known optimum
Convergence Time: ~47s
Stability: Low std. deviation (~1%)

Best Settings:
  pheromone_power ≈ 1.25
  distance_power ≈ 2.0
  reward_power = 0

Tested on additional datasets (eil51, pr76) to verify robustness and adaptability.

▶️ Demo & Visualization
Demo Notebook: See the main .ipynb file in this repo
Graphs: Include route convergence over time, pheromone distribution, and path comparisons

Plots:
  Best path length over iterations
  Comparison between heuristic and non-heuristic search
