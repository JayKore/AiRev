# A* Search Algorithm

## Introduction

This program implements the **A* (A-Star) Search Algorithm**, one of the most efficient search techniques in Artificial Intelligence used to find the shortest path using both cost and heuristic information.

A* improves performance by making informed decisions during search.

---

## Concept Used

### What is A*?

A* is an **informed search algorithm** that evaluates nodes using:

```text id="astarfunc"
f(n) = g(n) + h(n)
```

Where:

* g(n) = actual cost from start
* h(n) = estimated cost to goal

---

### Key Characteristics

* Uses **heuristic function**
* Combines cost + estimate
* Guarantees **optimal solution** (if heuristic is admissible)
* More efficient than UCS

---

## Algorithm (Steps)

1. Start from initial node
2. Add it to open list
3. Select node with lowest f(n)
4. Expand neighbors
5. Update cost and heuristic
6. Repeat until goal is reached

---

## Example

### Input

```text id="astarin2"
Graph with costs and heuristic values
Start: A
Goal: G
```

---

### Output

```text id="astarout2"
Optimal Path: A → B → D → G
Minimum Cost Path Found
```

---

## Explanation

* A* considers both:

  * Distance already traveled
  * Estimated distance to goal
* Chooses the most promising path

---

## Code Explanation

* Uses priority queue for node selection
* Maintains:

  * g(n) values
  * h(n) values
* Updates f(n) dynamically

---

## Frequently Asked Questions

### Q1. What makes A* better than UCS?

**Answer:** A* uses heuristic guidance, making it faster.

---

### Q2. What is admissible heuristic?

**Answer:** A heuristic that never overestimates actual cost.

---

### Q3. Is A* always optimal?

**Answer:** Yes, if heuristic is admissible.

---

### Q4. Where is A* used?

**Answer:** Games, navigation systems, robotics.

---

## Conclusion

A* is one of the most powerful search algorithms, combining efficiency and optimality by using both actual and estimated costs.

When the algorithm seems to “know” which path looks promising before fully exploring it, that is A* doing its job properly.
