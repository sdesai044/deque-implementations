# Deque Implementations

A Java implementation of a double-ended queue (deque) using three distinct 
approaches, each implementing a common `Deque` interface.

## Implementations

- **ArrayListDeque** — reference implementation using ArrayList; O(N) removeFirst
due to element shifting
- **ArrayDeque** — circular array with dynamic resizing; O(1) amortized addFirst,
addLast, removeFirst, removeLast
- **LinkedDeque** — doubly-linked list with sentinel nodes; true O(1) addFirst,
addLast, removeFirst, removeLast with proportional memory usage

## Key Concepts

Data Structures, Algorithms, Circular Arrays, Doubly-Linked Lists, Sentinel Nodes,
Amortized Analysis, Java Generics

## Runtime Comparison

| Implementation | addLast | removeFirst |
|---|---|---|
| ArrayListDeque | O(1) amortized | O(N) |
| ArrayDeque | O(1) amortized | O(1) amortized |
| LinkedDeque | O(1) | O(1) |

Experimental analysis confirmed that ArrayListDeque scales linearly for removeFirst
while ArrayDeque and LinkedDeque maintain constant time regardless of deque size.
