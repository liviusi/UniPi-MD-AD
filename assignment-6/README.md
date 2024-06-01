# Assignment 6

Picture mentioned below can be found in the ./images/ folder.

**Graph diameter**

## Exercise 1
Show how to use matrix computation to compute the diameter D exactly (time is O(n^ω log D)), where n^ω is the cost of binary matrix multiplication, where ω is unknown and currently is only known that 2 ≤ ω ≤ 2.3728596).

## Exercise 2
Prove that any BFS gives a 2-approximation, that is, the computed value is ≥ D/2, where D is the graph diameter. 

## Exercise 3
Consider the 2-sweep algorithm in an unweighted graph: 
```
r = random node in the graph;
a = farthest node from r;  
b = farthest node from a; 
return d(a,b). // their distance
```

Prove that this algorithm, which performs quite well in practice, gives an arbitrary lower value with respect to the diameter D of the following graph (you should fill the missing details in the picture below).