# Bayesian Inference

## Introduction

This program demonstrates **Bayesian Inference**, a probabilistic approach in Artificial Intelligence used to update beliefs based on new evidence.

It is widely used in decision making, prediction, and classification problems.

---

## Concept Used

### What is Bayesian Inference?

Bayesian Inference is based on **Bayes’ Theorem**, which calculates the probability of an event given prior knowledge.

---

### Bayes’ Theorem

```text id="bayes1"
P(A | B) = (P(B | A) * P(A)) / P(B)
```

Where:

* P(A | B) = Posterior probability
* P(B | A) = Likelihood
* P(A) = Prior probability
* P(B) = Evidence

---

### Key Idea

* Start with prior belief
* Update belief when new data arrives
* Result is improved prediction

---

## Algorithm (Steps)

1. Define prior probabilities
2. Observe new evidence
3. Calculate likelihood
4. Apply Bayes’ formula
5. Update probability

---

## Example

### Input

```text id="bayesin1"
Disease Probability = 0.01
Test Accuracy = 0.99
```

---

### Output

```text id="bayesout1"
Updated Probability after test result
```

---

## Explanation

* Initial probability is updated using evidence
* Even accurate tests may produce unexpected probabilities
* Shows importance of prior knowledge

---

## Code Explanation

* Probabilities stored as variables
* Formula applied step by step
* Output shows updated belief

---

## Frequently Asked Questions

### Q1. What is prior probability?

**Answer:** Initial belief before observing evidence.

---

### Q2. What is posterior probability?

**Answer:** Updated belief after considering evidence.

---

### Q3. Where is Bayesian used?

**Answer:** Spam filtering, medical diagnosis, prediction systems.

---

### Q4. Why is Bayesian important?

**Answer:** It helps make decisions under uncertainty.

---

## Conclusion

Bayesian Inference provides a powerful way to update beliefs based on evidence, making it essential for probabilistic reasoning in AI.

When the answer changes because new information arrives, that is not inconsistency—it is Bayesian reasoning working as intended.
