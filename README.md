# MinMax Single-Depot Multiple Traveling Salesman Problem (multiple-TSP)

This variant of multiple-TSP (called MinMax multiple-TSP) aims to equally distribute the workload among salesmen by requiring the longest tour of all the salesmen to be as short as possible, i.e. minimizing the maximum tour length of each salesman. The problem is to find the tours of each salesman such that the previous restrictions are satisfied and the overall cost of visiting all nodes is minimized, whilst obtaining at the same time balanced tours. Such restrictions appear in real-life applications where the purpose is to have a good balance of workloads for the salesmen.

In other words, we look to optimize a multi-objective problem, where the 2 objectives are:
 - minimize the cummulative cost of all the traveling salesmans
 - minimize the longest traveling salesman route
 
## Proposed approaches

### Genetic algorithm

The first approach we propose is a simple genetic algorithm, which incapsulates both objectives in one, with the same ratio (the fitness function is represented as the cummulative values of the overall cost and the minmax score). We introduced 2 different mutation operators, one that optimizes locally a single traveling salesman and one that optimizes the overall chromosome by playing with the length of the salesmans. The crossover is a form of PMX crossover on individual salesmans between chromosomes, but without a cut point, due to the lack of consistancy between same traveling salesmans from different chromosomes. We use a standard tournament based as the selection operator with elitism included.

## Test problems

The problems used in this repository can be found <a href="https://profs.info.uaic.ro/~mtsplib/MinMaxMTSP/index.html">here</a>, with also the best results found.

Credits to the authors of the <a href="https://link.springer.com/chapter/10.1007/978-3-319-19644-2_22">article</a> that proposed this problem and published their results.
