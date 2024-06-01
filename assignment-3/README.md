# Assignment 3

## Exercise 1

Design a space-efficient data structure D for prefix sums over a binary vector (bitvector) B of n bits. D replaces B, and should use O(n) bits; moreover, it must support the following constant-time operation (see attached pdf): 
- rank(i) = sum(B[0..i]) = sum_{0 ≤ j ≤i} B[j] (hint: sample B to build D + use lookup table)

## Exercise 2
Consider an implementation of D that takes near-optimal space log_2(n choose k) + o(n) bits, where k is the number of 1s in B. Design an alternative to Bloom filter with failure probability f as an approximate dictionary. A useful approximation is log_2(n choose k) ~ k log_2 (n/k) to get nearly-optimal space log_2 (1/f)  n + o(n) bits and constant time query (see attached pdf). Hint: use D to reconstruct the value of B[i] and a universal hash function h : U -> [n/f].