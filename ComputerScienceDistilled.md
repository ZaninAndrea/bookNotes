# Computer Science Distilled, Wladston Ferreira Filho

## Basics
### Ideas
- flowcharts are a powerful tool
- you could also write pseudocode
- if you model you problem mathmatically you can leverage the work done by others in the past

### Logic
- the fundaments of formal logic are booleans, the conditional --> operator, the negation ! operator, the AND and OR operators
- remember that from A-->B doesn't follow B-->A
- AND and OR follow associativty and distributivity
- DeMorgan's Law: 
!(A AND B) = !A OR !B
!A AND !B = !(A OR B)
- we can use truth tables to represent logic statements
- logic gates perform logic operations on electric current

### Counting
- a bunch of combinatorial stuff

### Probability
- bunch of high school probability
- gambler's fallacy: thinking that past events affect the likelihood of a future independent even, e.g. that rolling 10 times 1 in a row makes a 1 less likely as 11th roll

## Complexity
- always consider the best, the worst and the average case scenario, but the most important is the worst case
- time complexity is a function that maps input size to number of operations
- if we ignore everything but the dominant term and remove constants we get Big O notation
- exponential growth algorithms as practically not runnable
- remember to also consider the space complexity

## Strategy
### Iteration
- iteration is a loop
- Given a collection of objects S, the power set of S is the set containing all subsets of S
- to compute the power set:
```
function power_set(flowers)
    fragrances ← Set.new
    fragrances.add(Set.new)
    for each flower in flowers
        new_fragrances ← copy(fragrances)
        for each fragrance in new_fragrances
            fragrance.add(flower)
        fragrances ← fragrances + new_fragrances
    return fragrances
```

### Recursion
- We say there’s recursion when a function delegates work to clones of itself
- Recursive algorithms are generally simpler and shorter than iterative ones, but require more memory

### Brute force
- simply try every option

### Backtracking
- example: the 8 queens problem. To solve it you start placing queens at random, when you can't place any more queens you undo the last move and retry until you find the solution, or have no more possible moves, then you undo another move and retry
- the mantra is *fail early, fail often*

### Heuristics
- heuristics provide good enough solutions
- an example are greedy algorithms: always make the best choice and never question it later, in the knapsack problem it's always put in the item with the highest value
- for some problems heuristics like greedy algorithms always provide te best choice, e.g. fractional knapsack

### Divide and Conquer
- continue splitting the problem until a base case, then join the solutions. E.g. merge sort
- the knapsack can be solved through divide and conquer: base case: 0 elements to fit. To merge solution take the one that maxs the revenue.

### Dynamic programming
Sometimes identical computations are performed multiple times when solving a problem. Dynamic programming is identifying repeated subproblems in order to compute them only once

### Branch and bound
Find the upper and lower bounds, then discard every option that doesn't fit before doing any calculation.

## Data
### Abstract data types
An Abstract Data Type (ADT) is the specification of a group of operations that make sense for a given data type.

It allows us to separate the interface from the implementation of the various operations.

### Common abstractions
Among the common abstractions:
- stack
- queue
- priority queue (elements have a priority)
- list
- sorted list
- map (aka Dictionary)
- set (unordered group)

### Structure
Data structures define how data is organized in the computer memory.
Among those:
- array
- linked list
- double linked list
- tree
- binary search tree
- self balancing trees
- binary heap: like binary trees but the parent node has to be smaller (or greater) than both children. Useful to implement priority queues
- graph
- hash tables: search is O(1), but it requires a lot of memory. They have the issue of hash collisions: 2 items having the same hash, to solve this use a linked list as element of the has table. Too many collisions lower the performance

## Algorithms
### Sorting
Quicksort and mergesort are good for not sorted at all datasets
Insertion sort is good for almost sorted datasets

### Search

