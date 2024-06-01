# Assignment 4

## Exercise 1
Consider the randomized min-cut algorithm discussed in class. We have seen that its probability of success is at least 2/n, where n is the number of its vertices.

- Describe how to implement the algorithm when the graph is represented by adjacency lists, and analyze its running time. In particular, a contraction step can be done in O(n) time.
- A weighted graph has a weight w(e) on each edge e, which is a positive real number. The min-cut in this case is meant to be min-weighted cut, where the sum of the weights in the cut edges is minimum. Describe how to extend the algorithm to weighted graphs, and show that the probability of success is still ≥ 2/n. [hint: define the weighted degree of a node]
- Show that running the algorithm N times independently at random, and taking the minimum among the min-cuts thus produced, the probability of success can be made at least 1 − 1/n^c for a constant c > 0 (hence, with high probability).