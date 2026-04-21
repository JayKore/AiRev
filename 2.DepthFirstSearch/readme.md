# Depth First Search (DFS)

## Introduction

This program implements **Depth First Search (DFS)**, a fundamental search technique used in Artificial Intelligence to explore graphs by going as deep as possible before backtracking.

DFS is useful for problems involving **backtracking, path finding, and exhaustive search**.

---

## Concept Used

### What is DFS?

Depth First Search explores nodes by going **deep into one branch** before exploring others.

### Key Characteristics

* Uses **Stack (LIFO)** or recursion
* Does not guarantee shortest path
* Efficient for deep exploration problems

---

## Algorithm (Steps)

1. Start from the initial node
2. Mark it as visited
3. Visit one unvisited neighbor
4. Repeat step 3 until no more neighbors
5. Backtrack to previous node
6. Continue until all nodes are visited

---

## Example

### Input

```text id="dfsin1"
Graph:
A → B, C
B → D, E
C → F

Start Node: A
```

### Output

```text id="dfsout1"
A B D E C F
```

---

## Explanation

* Start at A
* Go deep: A → B → D
* Backtrack to B → E
* Then go to C → F

Traversal follows **depth-first expansion**

---

## Code Explanation

* Graph is stored using adjacency list
* Recursion (or stack) is used for traversal
* Visited nodes prevent infinite loops

---

## Frequently Asked Questions

### Q1. Why does DFS use a stack?

**Answer:** Because it follows LIFO order, allowing deep traversal before backtracking.

---

### Q2. Does DFS give shortest path?

**Answer:** No, DFS does not guarantee the shortest path.

---

### Q3. What is time complexity of DFS?

**Answer:** O(V + E)

---

### Q4. Where is DFS used?

**Answer:** Maze solving, cycle detection, backtracking problems.

---

## Conclusion

DFS is useful when exploring all possibilities in depth is required. It is particularly powerful in problems where solutions lie deep in the search space.

When the algorithm keeps diving deeper before reconsidering its choices, that is DFS doing exactly what it was meant to do.
