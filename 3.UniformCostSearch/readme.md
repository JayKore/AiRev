# Uniform Cost Search (UCS)

## Introduction

This program implements **Uniform Cost Search (UCS)**, an uninformed search algorithm used in Artificial Intelligence to find the **least-cost path** from a start node to a goal node.

Unlike BFS, UCS considers the **cost of each path**, making it suitable for weighted graphs.

---

## Concept Used

### What is Uniform Cost Search?

Uniform Cost Search expands the node with the **lowest cumulative cost** first.

It is similar to Dijkstra’s algorithm and guarantees the optimal solution when all costs are positive.

---

### Key Characteristics

* Uses **Priority Queue**
* Expands node with **minimum path cost**
* Guarantees **optimal solution**
* Works for **weighted graphs**

---

## Algorithm (Steps)

1. Initialize priority queue with start node
2. Assign cost = 0
3. While queue is not empty:

   * Remove node with lowest cost
   * If goal is reached → stop
   * Expand neighbors
   * Add them with updated cost
4. Repeat

---

## Example

### Input

```text id="ucsin1"
Graph:
A → B (cost 1), C (cost 4)
B → D (cost 2)
C → D (cost 1)

Start: A
Goal: D
```

---

### Output

```text id="ucsout1"
Path: A → B → D
Cost: 3
```

---

## Explanation

* Path A → C → D has cost 5
* Path A → B → D has cost 3
* UCS selects the **minimum cost path**

---

## Code Explanation

* Priority queue stores nodes with costs
* Nodes are expanded in increasing cost order
* Visited set prevents redundant processing

---

## Frequently Asked Questions

### Q1. How is UCS different from BFS?

**Answer:** BFS uses levels, UCS uses path cost.

---

### Q2. Is UCS optimal?

**Answer:** Yes, if all edge costs are positive.

---

### Q3. What data structure is used?

**Answer:** Priority Queue.

---

### Q4. Where is UCS used?

**Answer:** Route planning, shortest path problems.

---

## Conclusion

Uniform Cost Search is essential for solving problems where cost matters. It ensures the cheapest solution is always found.

If the algorithm insists on taking the “longer-looking” route but still ends up cheaper, it is doing exactly what UCS is meant to do.
