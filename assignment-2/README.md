# Assignment 2

## Exercise 1
Consider the Karp-Rabin string matching in its Las Vegas version, where the fingerprint f(x) = x % p for a random prime p in [2...tau] is replaced by h(x) = (a x + b % p) % q, where now p  > q are given primes, and a ≠ 0 and b are random integers from [0... p-1]. 
- Discuss whether h(x) can be still computed as a rolling hash, and which are the benefits of replacing f(x) with h(x). 
- Does the expected running time changes significantly?

## Exercise 2
Your company has a database S ⊆ U of keys. For this database, it uses a hash function h uniformly chosen at random from a universal family H (as seen in class). It also keeps a bit vector B of m entries, initialized to zeroes, which are then set B[h(k)] = 1 for every k ∈ S (note that collisions may happen). Unfortunately, the database S has been lost, thus only B and h survived, and the rest is no more accessible.
- Under the hypothesis that m ≥ c |S| for some c > 1, can we use the expected number of 1s in B to estimate |S| under a uniform choice at random of h ∈ H? 
- Based alone on B and h, how can you establish if any key given k ∈ U was also in S or not, and what is the probability of error? [Note: you are not choosing k and S randomly as the they are both given... randomization here is in the choice of h ∈ H]  