# Eight Puzzle Problem

## Introduction

This program solves the **Eight Puzzle Problem**, a classic problem in Artificial Intelligence used to demonstrate state space search and heuristic-based problem solving.

The puzzle consists of a 3×3 grid with 8 numbered tiles and one blank space. The goal is to reach a target configuration by sliding tiles into the blank space.

---

## Concept Used

### What is the Eight Puzzle Problem?

It is a **state space search problem** where:

* Each configuration is a state
* Moves involve sliding tiles
* The objective is to reach the goal state

---

### Key Concepts

* **State Space**: All possible configurations
* **Initial State**: Starting arrangement
* **Goal State**: Desired arrangement
* **Operators**: Move blank (up, down, left, right)
* **Path Cost**: Number of moves

---

### Heuristics (Important)

Common heuristic functions:

1. **Misplaced Tiles**
2. **Manhattan Distance**

These help improve search efficiency.

---

## Algorithm (General Approach)

1. Start with initial state
2. Check if it is goal state
3. Generate possible moves
4. Evaluate using heuristic
5. Select best state
6. Repeat until goal is reached

---

## Example

### Input

```text id="8pin1"
Initial State:
1 2 3
4 0 6
7 5 8

Goal State:
1 2 3
4 5 6
7 8 0
```

---

### Output

```text id="8pout1"
Moves:
Down → Right → Right

Goal State Reached
```

---

## Explanation

* Blank (0) is moved step by step
* Each move reduces difference from goal
* Heuristic guides optimal path

---

## Code Explanation

* State represented as matrix or list
* Moves generated dynamically
* Search algorithm (often A*) used
* Heuristic used for optimization

---

## Frequently Asked Questions

### Q1. What type of problem is Eight Puzzle?

**Answer:** State space search problem.

---

### Q2. Why use heuristics here?

**Answer:** To reduce number of explored states and improve efficiency.

---

### Q3. What is Manhattan Distance?

**Answer:** Sum of distances of tiles from their goal positions.

---

### Q4. Is the problem always solvable?

**Answer:** No, only certain configurations are solvable.

---

## Conclusion

The Eight Puzzle problem demonstrates how search algorithms and heuristics work together to solve complex problems efficiently.

If the solution feels like it’s carefully rearranging chaos into order one move at a time, that is exactly the point.
