# Breadth First Search (BFS)

## Introduction

This program implements **Breadth First Search (BFS)**, a fundamental search algorithm in Artificial Intelligence used to traverse or explore graphs level by level.

BFS is particularly useful when the goal is to find the **shortest path in an unweighted graph**.

---

## Concept Used

### What is BFS?

Breadth First Search explores nodes **level by level**, starting from the initial node and visiting all its neighbors before moving to the next level.

### Key Characteristics

* Uses a **Queue (FIFO)**
* Guarantees **shortest path** (in unweighted graphs)
* Complete and optimal (for such cases)

---

## Algorithm (Steps)

1. Start from the initial node
2. Mark it as visited
3. Add it to the queue
4. While the queue is not empty:

   * Remove a node from the queue
   * Visit it
   * Add all unvisited neighbors to the queue
5. Repeat until goal is found or all nodes are visited

---

## Example

### Input

```text id="bfsin1"
Graph:
A → B, C
B → D, E
C → F

Start Node: A
```

### Output

```text id="bfsout1"
A B C D E F
```

---

## Explanation

* Start at A
* Visit neighbors: B, C
* Then visit next level: D, E, F

Traversal order follows **level-wise expansion**

---

## Code Explanation

* Graph is stored using an adjacency list
* A queue is used to maintain order of traversal
* A visited list ensures nodes are not revisited

---

## Frequently Asked Questions

### Q1. Why does BFS use a queue?

**Answer:** Because it follows FIFO order, ensuring nodes are explored level by level.

---

### Q2. Does BFS always give the shortest path?

**Answer:** Yes, but only in **unweighted graphs**.

---

### Q3. What is time complexity of BFS?

**Answer:** O(V + E), where V = vertices and E = edges.

---

### Q4. Where is BFS used?

**Answer:** Shortest path problems, network traversal, web crawling.

---

## Conclusion

BFS is a simple yet powerful algorithm for exploring graphs systematically. It ensures that the closest nodes are visited first, making it ideal for shortest path problems.

If everything expands outward neatly like ripples in water, you are probably looking at BFS working exactly as intended.
