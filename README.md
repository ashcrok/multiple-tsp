# MinMax Single-Depot Multiple Traveling Salesman Problem (multiple-TSP)

This variant of multiple-TSP (called MinMax multiple-TSP) aims to equally distribute the workload among salesmen by requiring the longest tour of all the salesmen to be as short as possible, i.e. minimizing the maximum tour length of each salesman. The problem is to find the tours of each salesman such that the previous restrictions are satisfied and the overall cost of visiting all nodes is minimized, whilst obtaining at the same time balanced tours. Such restrictions appear in real-life applications where the purpose is to have a good balance of workloads for the salesmen.

In other words, we look to optimize a multi-objective problem, where the 2 objectives are:
 - minimize the cummulative cost of all the traveling salesmans
 - minimize the longest traveling salesman route
