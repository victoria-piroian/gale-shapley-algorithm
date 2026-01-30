# Gale Shapley Algorithm - Stable Matching Program (Student–School Matching)
----------------------------------

## Overview

This project implements a **Stable Matching Problem (SMP) solver** using a variation of the **Gale–Shapley algorithm**. The system models a many-to-one matching scenario between **students** and **schools**, where:

- Students rank schools by preference  
- Schools rank students based on a weighted combination of GPA and extracurricular score  
- Schools may accept multiple students (capacity > 1)  
- The algorithm produces a matching that is **stable** (no blocking pairs)

The program also computes:

- Average suitor regret  
- Average receiver regret  
- Average total regret  
- Stability of the matching  
- Computation time  

---

## Features

- Gale–Shapley stable matching algorithm  
- Many-to-one matching support  
- Two participant types:
  - `Student` (suitor)  
  - `School` (receiver)  
- Regret calculations  
- Stability verification  
- Interactive user input  
- Clean formatted output  

---

## How to Compile and Run

```bash
javac *.java
java Pro5_piroianv
```
---
## Input

### Students:
- Name
- GPA (0.0 – 4.0)
- Extracurricular score (0 – 5)
- Maximum number of matches
- Ranking of schools

### Schools:
- Name
- Alpha (GPA weight, 0.0 – 1.0)
- Maximum number of matches

### School rankings are automatically computed as:

(alpha × GPA) + (1 − alpha) × ES

---

## Output
- Stable or not stable
- Average suitor regret
- Average receiver regret
- Average total regret
- Final matches

### Regret Definition:
- Lower regret indicates a better outcome
- regret = (rank of assigned partner) - 1

### Stability Definition:

A matching is stable if there exists no blocking pair: A student and a school who both prefer each other over their current matches.

---

## Author
Victoria Piroian

University of Toronto

Faculty of Applied Science & Engineering, 2022
