# Assignment 5

**Count-min sketch: range queries**

## Exercise 1

Consider the counters F[i] for 1 ≤ i ≤ n, where n is the number of items in the stream of any length. At any time, we know that ||F|| is the total number of items (with repetitions) seen so far, where each F[i] contains how many times item i has been so far.  We saw that CM-sketches provide a FPTAS F'[i] such that F[i] ≤ F'[i] ≤ F[i] + ε ||F||, where the latter inequality holds with probability at least 1 - δ.

Consider now a range query (a,b), where we want Fab = sum_{a ≤ i ≤ b} F[i]. Show how to adapt CM-sketch so that a FPTAS F'ab is provided:

- Baseline is sum_{a ≤ i ≤ b} F'[i], but this has drawbacks as both time and error grows with b-a+1.
- Consider how to maintain counters for just the sums when b-a+1 is any power of 2 (less or equal to n):
- - Can we now answer quickly also when b-a+1 is not a power of two?
- - Can we reduce the number of these power-of-2 intervals from n log n to 2n?
- - Can we bound the error with a certain probability?

	Suggestion: it does not suffices to say that it is at most δ the probability of error of each individual counter; while each counter is still the actual wanted value plus the residual as before, it is better to consider the sum V of these wanted values and the sum X of these residuals, and apply Markov’s inequality to V and X rather than on the individual counters.


## Exercise 2

Show (and prove correctness) that there is a deterministic streaming algorithm that works in O(1) space and finds the most frequent item if the latter appears strictly more than half of the times in the stream