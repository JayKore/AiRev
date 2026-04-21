# Artificial Intelligence Revision Repository

This repository is a structured collection of core Artificial Intelligence concepts and implementations aligned with a typical university syllabus. It is designed to support revision, practical understanding, and quick reference before examinations or viva.

The contents are organized topic-wise, covering search strategies, reasoning methods, logic programming, and foundational AI techniques. Each section contains implementations and examples intended to demonstrate how theoretical concepts translate into working solutions.

Think of this as a guided walkthrough of AI topics—from basic problem solving to logic-based reasoning—assembled in a way that lets you move between theory and implementation without losing track of the bigger picture.

---

# Repository Overview

The repository is divided into logical sections, each corresponding to a major AI topic:

* Search Algorithms: Breadth First Search, Depth First Search, and related strategies
* Problem Solving: State space representation and systematic exploration
* Knowledge Representation: Logical structures used to model information
* Reasoning: Inference techniques such as forward and backward chaining
* Logic Programming: SWI-Prolog implementations of rules and queries
* Additional AI Concepts: Supporting examples and variations of core topics

Each folder contains code files that demonstrate how the concept works in practice.

---

# How to Run Python Programs

Follow these steps to execute Python-based implementations:

1. Ensure Python is installed:

   ```bash
   python --version
   ```

2. Navigate to the required folder:

   ```bash
   cd folder_name
   ```

3. Run the program:

   ```bash
   python filename.py
   ```

4. Provide input if prompted in the terminal.

---

# How to Run SWI-Prolog Programs

These steps assume SWI-Prolog is installed on your system.

1. Install SWI-Prolog (if not already installed):

   * Download from: https://www.swi-prolog.org

2. Open terminal or command prompt.

3. Navigate to the folder containing the `.pl` file:

   ```bash
   cd folder_name
   ```

4. Start SWI-Prolog:

   ```bash
   swipl
   ```

5. Load the program:

   ```prolog
   [filename].
   ```

6. Execute queries:

   ```prolog
   predicate_name(arguments).
   ```

7. Press `;` to see alternative solutions (if available).

8. Exit Prolog:

   ```prolog
   halt.
   ```

---

# What You Should Understand from This Repository

This repository is not just for running code. You should be able to explain:

* How a problem is represented in state space
* How search algorithms explore possible solutions
* The role of heuristics in improving efficiency
* How knowledge is represented using logic
* How inference mechanisms derive conclusions
* The difference between declarative and procedural approaches

---

# Probable Viva Questions

## Search and Problem Solving

* What is state space representation?
* Difference between BFS and DFS
* What is a heuristic function?
* What is informed vs uninformed search?
* Explain A* algorithm

## Knowledge Representation

* What is propositional logic?
* What is predicate logic?
* Difference between semantic networks and frames

## Reasoning

* What is forward chaining?
* What is backward chaining?
* Difference between them

## Logic Programming (Prolog)

* What is a fact, rule, and query?
* What is unification?
* What is backtracking?
* Why is Prolog called a declarative language?

## General AI Concepts

* What is Artificial Intelligence?
* What are the main goals of AI?
* Difference between AI and Machine Learning
* What is an intelligent agent?

---

# Preparation Strategy

To use this repository effectively:

1. Run each program at least once
2. Understand the input and output clearly
3. Be able to explain the logic behind each step
4. Practice writing small variations of the same program
5. Revise key definitions and differences

---

# Final Note

This repository is intended to bridge the gap between theory and implementation. If you can explain what each program is doing without looking at the code, you are prepared.

And if something feels like it just “clicks” after running it a few times, that is usually a sign you are on the right track—no need to overthink it.

---

FOllowing summarizes key graph traversal, search, and problem-solving algorithms with their characteristics, use cases, and comparisons.

## Table of Contents
1. [Depth-First Search (DFS)](#depth-first-search-dfs)
2. [Breadth-First Search (BFS)](#breadth-first-search-bfs)
3. [A* Search](#a-search)
4. [8-Puzzle Solver](#8-puzzle-solver)
5. [Tower of Hanoi](#tower-of-hanoi)
6. [Bayesian Classifier](#bayesian-classifier)
7. [Tic-Tac-Toe AI](#tic-tac-toe-ai)

---

## Depth-First Search (DFS)

### Core Concept
Explores a graph by moving as deep as possible down one path before backtracking.

### Key Characteristics
- **Data Structure**: Stack (LIFO)
- **Approach**: "Go deep first"
- **Memory**: O(depth) - efficient for deep graphs
- **Completeness**: Yes (for finite graphs)
- **Optimality**: No (doesn't guarantee shortest path)

### When to Use
- ✔ Maze solving
- ✔ Topological sorting
- ✔ Cycle detection
- ✔ Puzzle games (e.g., Sudoku)
- ✖ Finding shortest paths

### Time Complexity
**Worst Case**: O(V + E)  
*(V = vertices, E = edges)*

---

## Breadth-First Search (BFS)

### Core Concept
Explores a graph level by level, visiting all neighbors at the present depth before moving deeper.

### Key Characteristics
- **Data Structure**: Queue (FIFO)
- **Approach**: "Explore wide first"
- **Memory**: O(width) - stores all nodes at current level
- **Completeness**: Yes (for finite graphs)
- **Optimality**: Yes (finds shortest path in unweighted graphs)

### When to Use
- ✔ Shortest path finding (unweighted graphs)
- ✔ Web crawling
- ✔ Social network analysis
- ✔ GPS navigation
- ✖ Deep graph exploration (memory intensive)

### Time Complexity
**Worst Case**: O(V + E)

---

## A* Search

### Core Concept
Informed search algorithm that finds the shortest path by combining:
- Actual path cost from start (g(n))
- Heuristic estimate to goal (h(n))

### Key Characteristics
- **Data Structure**: Priority Queue (min-heap)
- **Optimality**: Yes (with admissible heuristic)
- **Completeness**: Yes (if solution exists)
- **Memory**: O(b^d) - stores all explored nodes

### When to Use
- ✔ Pathfinding in games/maps
- ✔ Robot navigation
- ✔ Puzzle solving (8-puzzle)
- ✔ Route planning
- ✖ When no good heuristic exists

### Heuristic Requirements
- **Admissible**: Never overestimates true cost
- **Consistent**: h(n) ≤ cost(n→n') + h(n')

### Comparison Table

| Algorithm | Optimal | Complete | Uses Heuristic | Best For |
|-----------|---------|----------|----------------|----------|
| A*        | Yes     | Yes      | Yes            | Informed pathfinding |
| Dijkstra  | Yes     | Yes      | No             | Weighted graphs |
| BFS       | Yes*    | Yes      | No             | Unweighted graphs |
| DFS       | No      | Yes      | No             | Deep graphs |

*Only optimal for unweighted graphs

---

## 8-Puzzle Solver

### Implementation Details
- Uses A* algorithm with Manhattan distance heuristic
- **g(n)**: Actual moves from start
- **h(n)**: Sum of tile displacements
- Visualizes search tree with solution path

### Why A*?
- Guarantees shortest path
- Efficient heuristic guidance
- Complete (finds solution if exists)

---

## Tower of Hanoi

### Algorithm Used
**Recursive Backtracking**  
- **Time Complexity**: O(2ⁿ)
- **Space Complexity**: O(n) (recursion stack)

### Why This Approach?
- Solves in minimal moves (2ⁿ - 1)
- Classic recursion example
- Clear divide-and-conquer logic

---

## Bayesian Classifier

### Method
**Naive Bayes Classifier**  
Predicts probabilities using:
P(Weather | Evidence) ∝ P(Evidence | Weather) * P(Weather)

### Advantages
- Handles multiple evidence sources
- Clear probabilistic reasoning
- Easily extendable

### Complexity
- **Time**: O(n) for n evidence variables
- **Space**: O(1) (fixed probability tables)

---

## Tic-Tac-Toe AI

### Algorithm Components
| Component       | Algorithm                     | Key Feature                          |
|-----------------|-------------------------------|--------------------------------------|
| Win Check       | Brute-force pattern matching  | Checks all 8 winning combinations    |
| AI Move         | Greedy heuristic              | Win-block-random priority            |
| Game Flow       | Recursive state management    | Alternates turns                     |
| Player Input    | Input validation              | Ensures legal moves                  |

### Strategy
- Immediate win/block decisions
- One-step lookahead
- Recursive game state management

---

# Author

Your Friendly Neighbourhood ....

---