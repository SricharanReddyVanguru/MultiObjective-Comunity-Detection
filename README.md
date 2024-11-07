# ﻿Multi-Objective Community Detection


## Project Overview:

This project focuses on community detection within complex networks using multi-objective optimization. Community detection is the process of identifying groups (or communities) of nodes that are more densely connected internally than with the rest of the network. This is a crucial task in fields like social network analysis, biology, and recommendation systems, where understanding clusters can provide insights into underlying structures.

The project employs a genetic algorithm-based approach using NSGA-II (Non-dominated Sorting Genetic Algorithm II) to optimize multiple objectives simultaneously, such as:

Modularity (EQ) - Measures the density of links inside communities compared to links between communities.
Normalized Mutual Information (NMI) - Quantifies the similarity between detected community structures and known community labels, often used for validating clustering quality.

## Key Features:

Multi-Objective Optimization: Uses NSGA-II to maximize modularity and similarity, balancing different objectives for optimal community detection.
Scalable Community Detection: Applies to real-world network data and generates community structures effectively.
Performance Evaluation: Includes functions to compute and evaluate key metrics like modularity and NMI, providing a robust performance assessment.

## Methodology:


The community detection process combines genetic algorithms with objective functions to find optimal partitions of the network:

Initialization: A population of candidate solutions (community partitions) is generated.
Objective Computation: Each solution is evaluated based on modularity and NMI.
NSGA-II Algorithm: The algorithm iterates through selection, crossover, and mutation to evolve the solutions:
Selection: Sorts solutions based on dominance (Pareto ranking).
Crossover and Mutation: Introduces variability to explore possible partitions.
Termination and Result Analysis: The algorithm runs until convergence or a set number of generations, producing a set of non-dominated solutions that represent different trade-offs between modularity and similarity.


## Project Structure

Here is a breakdown of the main files and folders:

Main.m: Main script to run the community detection algorithm.
NSGA2.m: Implements the NSGA-II algorithm, handling the genetic operations and population evolution.
Community and Objective Functions:
Calculate_EQ.m: Computes modularity for a given community partition.
Calculate_NMI.m and FuncNMI.m: Calculate NMI to assess clustering quality.
compute_objective.m: Computes the combined objective values for each solution.
Utilities:
Initial_Population.m: Generates an initial set of community structures.
LocalKmeans.m: Uses local clustering algorithms, likely to refine partitions.
PLOTFUNCTION.m: Visualizes results, showing community structure.
Results and Outputs:
result_NMI.txt: Stores the calculated NMI values for evaluation.
results/: Directory for storing results of multiple runs or parameter configurations.

## Usage Instructions

Prerequisites
MATLAB: The project is implemented in MATLAB, so make sure you have it installed.
Running the Project
Clone the Repository:
bash
Copy code
git clone https://github.com/SricharanReddyVanguru/MultiObjective-Comunity-Detection.git
cd MultiObjective-Comunity-Detection/EMOFM-DK
Run the Main Script:

Open Main.m in MATLAB.
Run the script to start the community detection process.

## View Results:

Output metrics like modularity and NMI will be displayed.
Plots or visualizations (if enabled) will show the detected community structures.


## Example Datasets

Place any network datasets you wish to analyze in the RealWorld folder within EMOFM-DK or specify paths directly in Main.m. The algorithm is designed to handle datasets in adjacency matrix format.
