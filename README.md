# Covering-salesman-problem
This project compares different approaches for solving  covering-salesman problem.

### Covering salesman problem
Covering salesman problem (CSP) is a generalization of traveling salesman problem (TSP). It is stated as follows: to identify the minimum cost tour of a subset of n given cities such that every city not on the tour is within some predetermined covering distance standard, S, of a city that is on the tour. [Reference](https://www.jstor.org/stable/25768381?seq=1)

###  Local Search Method: LS 2
+ __Main Idea:__
    LS2 mainly consists of two iterative procedures: the Improvement Procedure and the Perturbation Procedure. In the Improvement Procedure, the algorithm considers extraction of nodes from the current tour in a round-robin fashion. 
    If by removing a node on the
    tour the solution remains feasible, the tour cost has improved and the node is deleted from the tour.
    On the other hand, extracting a node from the tour may cause some other nodes to no longer be
    fully covered and the solution becomes infeasible. 
    [Paper](https://terpconnect.umd.edu/~raghavan/preprints/GCSPrevv3.pdf)

+ __Advantage:__
    1. Faster than Hopfield network
    2. Can get rid of local minima


### Greedy Randomized Adaptive Search Procedure
+ __Main idea:__
    GRASP may be viewed as a repetitive sampling technique. Each iteration produces a sample solution from an unknown distribution, whose mean and variance are functions of the restrictive nature of the RCL.
    If the RCL is restricted to a single element, then the same solution will be produced at all iterations. The variance of the distribution will be zero and the mean will be equal to the value
    of the greedy solution.

    [Paper](http://www.optimization-online.org/DB_FILE/2001/09/371.pdf)

### Hopfield Network on Covering salesman problem
+ __Main idea:__
    Covering salesman problem can be decompsed as set covering problem and traveling salesman problem (TSP). Then we first solve the set covering problem using greedy algorithm to find the minimum set of cities. Then we sovle the TSP based on this set and get CSP solution.
+ __Set covering problem:__
    Given a set of elements {{1,2,...,n}} (called the universe) and a collection S of m sets whose union equals the universe, the set cover problem is to identify the smallest sub-collection of  S whose union equals the universe. [Reference](https://en.wikipedia.org/wiki/Set_cover_problem)

+ __Traveling salesman problem (TSP)__
    "Given a list of cities and the distances between each pair of cities, what is the shortest possible route that visits each city and returns to the origin city?" [Reference](https://en.wikipedia.org/wiki/Travelling_salesman_problem)

+ __Disadvantage:__
    1. The neurons amount in Hopfield Network is equal to the square power of the amount of cities. The number of weights is equal to the fourth power of the amount of cities.
    2. The solution is very easy to trap into local minima


### Source code
Read the Jupyter Notebook [source code](./Summary.ipynb) in this project


