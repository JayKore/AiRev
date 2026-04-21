# Artificial Intelligence Viva Crash Sheet

---

## 1. Basics

### What is Artificial Intelligence?

Artificial Intelligence is the branch of computer science that enables machines to perform tasks that normally require human intelligence.

---

### What is an Intelligent Agent?

An intelligent agent perceives its environment and takes actions to maximize the achievement of its goals.

---

### Types of Agents

* Simple Reflex Agent
* Model-Based Agent
* Goal-Based Agent
* Utility-Based Agent

---

## 2. Search Algorithms

### BFS vs DFS

| BFS                      | DFS                              |
| ------------------------ | -------------------------------- |
| Level-wise traversal     | Depth-wise traversal             |
| Uses Queue               | Uses Stack                       |
| Guarantees shortest path | Does not guarantee shortest path |

---

### What is a Heuristic?

A heuristic is a function that estimates the cost from the current state to the goal state.

---

### Hill Climbing

* Greedy local search algorithm
* Moves only to better states
* May get stuck in local maxima

---

### Uniform Cost Search (UCS)

Expands the node with the lowest path cost.

* Uses Priority Queue
* Guarantees optimal solution (if costs are positive)

---

### A* Algorithm

```
f(n) = g(n) + h(n)
```

* g(n): actual cost from start
* h(n): estimated cost to goal

A* is optimal if the heuristic is admissible.

---

### Admissible Heuristic

A heuristic that never overestimates the actual cost.

---

## 3. Problem Solving

### What is State Space?

The set of all possible states of a problem.

---

### What is Goal State?

The desired final state.

---

### Eight Puzzle Key Points

* It is a state space problem
* Uses heuristic functions
* Common heuristic: Manhattan Distance

---

### Manhattan Distance

The sum of distances of tiles from their goal positions.

---

## 4. Probability (Bayesian)

### Bayes Theorem

```
P(A|B) = (P(B|A) * P(A)) / P(B)
```

---

### Terms

* Prior: Initial belief
* Posterior: Updated belief after evidence
* Likelihood: Probability of evidence

---

### Why Bayesian?

To update probabilities when new evidence is available.

---

## 5. Logic and Prolog

### What is Prolog?

A logic programming language based on facts and rules.

---

### Components

* Fact → `parent(a,b)`
* Rule → `grandparent(X,Y)`
* Query → `?- grandparent(a,X)`

---

### Unification

Matching variables with values.

---

### Backtracking

Trying alternative solutions automatically when one fails.

---

### Declarative vs Procedural

| Declarative | Procedural |
| ----------- | ---------- |
| What to do  | How to do  |

---

## 6. Important Differences

### BFS vs UCS

* BFS → Based on levels
* UCS → Based on path cost

---

### UCS vs A*

* UCS → No heuristic
* A* → Uses heuristic

---

### Hill Climbing vs A*

* Hill Climbing → Local search
* A* → Global optimal search

---

## 7. Common Traps

### Hill Climbing Issues

* Local maxima
* Plateau
* Ridge

---

### A* Requirement

Heuristic must be admissible.

---

### BFS Limitation

High memory usage.

---

### DFS Limitation

Can go into infinite depth.

---

## 8. Most Asked Questions

### Which algorithm gives shortest path?

* BFS (unweighted graphs)
* UCS / A* (weighted graphs)

---

### Why are heuristics used?

To reduce search time and improve efficiency.

---

### What is an optimal solution?

A solution with minimum cost.

---

### What is completeness?

The ability of an algorithm to always find a solution if one exists.

---

### What is local maxima?

A state that is better than neighbors but not the best overall.

---

## 9. Quick Answers

* AI is about making machines act intelligently
* Search algorithms explore state space
* Heuristics guide search efficiently
* A* combines cost and estimate for optimal search
* Prolog uses facts, rules, and queries
* Bayesian updates probability using evidence

---

## 10. Final Strategy

Before viva, make sure you can:

* Explain each algorithm in 1–2 lines
* Give one simple example
* State one advantage and one limitation

---

## Golden Line (Use if stuck)

“This is a state space search problem where we try to reach the goal state using an appropriate search strategy.”

---

## Final Note

If you understand how search works, why heuristics are used, and how logic-based reasoning operates, you are well prepared.

If something starts to make sense all at once after revising a few times, that is usually when things have finally clicked.
