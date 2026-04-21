# Other Experiments

## Introduction

This folder contains a collection of additional Artificial Intelligence experiments that demonstrate **logic-based problem solving and rule-based reasoning**, primarily using **Prolog (SWI-Prolog)**.

These experiments are designed to strengthen understanding of:

* Declarative programming
* Knowledge representation
* Logical inference
* Problem-solving using rules and facts

Unlike procedural languages, these programs focus on describing *what is true*, rather than *how to compute it*.

---

# Concepts Covered

## 1. Logic Programming

Logic programming is a paradigm where problems are solved using:

* **Facts** → Known truths
* **Rules** → Relationships between facts
* **Queries** → Questions asked to the system

Example:

```prolog id="lp1"
parent(john, mary).
```

---

## 2. Prolog Fundamentals

### Components

* **Fact** → `parent(john, mary).`
* **Rule** → `grandparent(X,Y) :- parent(X,Z), parent(Z,Y).`
* **Query** → `?- grandparent(john, X).`

---

## 3. Backtracking

Prolog automatically:

* Tries all possible solutions
* Returns answers one by one
* Backtracks when needed

---

## 4. Unification

Unification is the process of matching variables with values.

Example:

```prolog id="lp2"
parent(X, mary)
```

---

## 5. State Space Problems

Some experiments may include problems like:

* Water Jug Problem
* Monkey Banana Problem

These involve:

* Initial state
* Goal state
* Valid operations

---

# How to Run SWI-Prolog Programs

Follow these steps carefully:

### Step 1: Install SWI-Prolog

Download from:
https://www.swi-prolog.org

---

### Step 2: Open Terminal

Navigate to the folder:

```bash id="pro1"
cd 9.Other_Experiments
```

---

### Step 3: Start Prolog

```bash id="pro2"
swipl
```

---

### Step 4: Load Program

```prolog id="pro3"
[filename].
```

---

### Step 5: Run Queries

```prolog id="pro4"
predicate_name(arguments).
```

Press `;` to view more solutions.

---

### Step 6: Exit

```prolog id="pro5"
halt.
```

---

# Example

## Input (Prolog File)

```prolog id="ex1"
parent(john, mary).
parent(mary, sam).

grandparent(X,Y) :- parent(X,Z), parent(Z,Y).
```

---

## Query

```prolog id="ex2"
?- grandparent(john, X).
```

---

## Output

```text id="ex3"
X = sam
```

---

## Explanation

* john → mary → sam
* Rule applies twice
* Result derived using inference

---

# Code Explanation

* Facts define relationships
* Rules define logic
* Queries trigger reasoning
* Prolog handles search automatically

---

# Frequently Asked Questions

### Q1. What is Prolog?

**Answer:** A logic programming language used for AI applications based on facts and rules.

---

### Q2. What is backtracking?

**Answer:** The process of trying alternative solutions when one path fails.

---

### Q3. What is unification?

**Answer:** Matching variables with values to satisfy a query.

---

### Q4. Difference between fact and rule?

**Answer:**
Fact = known information
Rule = logical relation

---

### Q5. Why is Prolog used in AI?

**Answer:** Because it supports logical reasoning and symbolic computation.

---

### Q6. What is declarative programming?

**Answer:** Describing *what* the solution is rather than *how* to compute it.

---

# Conclusion

These experiments provide hands-on experience with logic-based AI systems. They demonstrate how complex reasoning can emerge from simple rules and structured knowledge.

If it ever feels like the program is quietly figuring things out on its own after you ask a question, that is not magic—it is just Prolog doing exactly what it was designed to do.
