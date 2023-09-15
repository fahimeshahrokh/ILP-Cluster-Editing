# ILP-Cluster-Editing

## Overview

This code implements a graph clustering algorithm using integer linear programming (ILP). Given an undirected graph, it finds the minimum edit distance to make the graph a cluster graph, i.e. a graph where each connected component forms a clique.  

The input is a text file containing the graph in the DIMACS format. The output is the optimized cluster graph after editing edges.

The algorithm has the following steps:

1. Read graph from text file and create a NetworkX graph object
2. Compute the complement graph 
3. Formulate an ILP problem to minimize edge edits
   - Binary variables for adding/removing edges
   - Constraints to maintain cycle consistency
4. Solve ILP using PuLP  
5. Extract solution and create clustered graph
6. Plot original graph, complement graph, and solution graph

## Requirements

- Python 3
- NumPy
- Pandas 
- NetworkX
- Matplotlib
- PuLP

## Usage

The input file name and parameters can be modified in the code directly.

## References

The ILP formulation is based on:

- Böcker, Sebastian, and Jan Baumbach. "Cluster editing." Proceedings of the 9th conference on Computational Methods in Systems Biology. 2011.

## Author

Fahime Shahrokh, 2020
