# 🐍 Python Programming Lab: Conditional Statements & Boolean Logic (Task 01)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/islamyasser424-design/Python-Task--01/blob/main/Python_Task_01.ipynb)
![Python Version](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Topics](https://img.shields.io/badge/Focus-Conditional%20Flow%20%26%20Branching-success?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

A structured Python laboratory assignment focused on Boolean logic evaluation, unary, binary, and multi-way conditional branching (`if`, `if-else`, `if-elif-else`), logical operator chaining (`and`), and arithmetic remainder inspection (`%`).

---

## 📌 Table of Contents
- [📖 Overview](#-overview)
- [🎯 Learning Objectives](#-learning-objectives)
- [🧩 Problem Statements & Solutions](#-problem-statements--solutions)
  - [1. Single-Branch Decision: `if`](#1-single-branch-decision-if)
  - [2. Dual-Branch Decision: `if-else`](#2-dual-branch-decision-if-else)
  - [3. Multi-Way Partitioning: `if-elif-else`](#3-multi-way-partitioning-if-elif-else)
  - [4. Compound Logical Filtering: Sign & Parity Classification](#4-compound-logical-filtering-sign--parity-classification)
- [📊 Decision Matrix & Truth Flow](#-decision-matrix--truth-flow)
- [💻 Getting Started & Execution](#-getting-started--execution)
- [👤 Author & Connect](#-author--connect)

---

## 📖 Overview

Conditional control structures form the bedrock of algorithmic decision making in software engineering and data analytics. This repository implements progressive numeric evaluation problems designed to master:
- **Predicate evaluation** yielding boolean truth values (`True` / `False`).
- **Binary mutual exclusion** using `if-else` blocks.
- **Exhaustive domain discretization** using sequential `if-elif-else` branches.
- **Short-circuit logical evaluation** via operator chaining (`and`).
- **Parity checking** combining arithmetic modulo (`% 2`) with relational equality (`== 0`, `!= 0`).

---

## 🎯 Learning Objectives

* Formulate robust boolean expressions to guard code paths against unexpected input states.
* Master the syntax and indentation rules of Python's control flow statements.
* Eliminate redundant evaluations by using structured `elif` ladders rather than uncoupled `if` blocks.
* Handle boundary values (e.g., zero `0`) cleanly in sign-detection workflows.
* Combine arithmetic operations with boolean logic for multi-attribute categorization (e.g., positive even vs. positive odd).

---

## 🧩 Problem Statements & Solutions

### 1. Single-Branch Decision: `if`
**Objective:** Prompt the user for an integer and execute a conditional statement that prints a confirmation message only when the number is strictly positive.

```python
number = int(input("Enter a number: "))

if number > 0:
    print("The number is positive")
```
* **Mechanism:** Evaluates `number > 0`. If `True`, the indented block executes. If `False` or equal to `0`, execution bypasses the block cleanly with zero side-effects.

---

### 2. Dual-Branch Decision: `if-else`
**Objective:** Implement a binary branching structure to differentiate between positive and negative numbers.

```python
number = int(input("Enter a number: "))

if number > 0:
    print("The number is positive")
else:
    print("The number is negative")
```
* **Mechanism:** Divides the input domain into two mutually exclusive execution paths. If the relational condition fails, the fallback `else` branch automatically triggers.

---

### 3. Multi-Way Partitioning: `if-elif-else`
**Objective:** Correctly partition the entire set of real integers ($\mathbb{Z}$) into three discrete categories: positive, negative, and zero.

```python
number = int(input("Enter a number: "))

if number > 0:
    print("The number is positive")
elif number < 0:
    print("The number is negative")
else:
    print("The number is zero")
```
* **Mechanism:** Implements a short-circuiting condition ladder. When `number > 0` is false, it proceeds to test `number < 0`. If both fail, it definitively infers that `number == 0` without needing an explicit third condition check.

---

### 4. Compound Logical Filtering: Sign & Parity Classification
**Objective:** Classify user inputs into granular categories: negative, positive & even, positive & odd, or zero using compound logical conjunctions.

```python
number = int(input("Enter a number: "))

if number < 0:
    print("The number is negative")
elif number > 0 and number % 2 == 0:
    print("The number is positive and even")
elif number > 0 and number % 2 != 0:
    print("The number is positive and odd")
else:
    print("The number is zero")
```
* **Mechanism:**
  * Uses the modulo operator `number % 2` to determine divisibility by 2.
  * Employs the logical `and` operator to enforce dual criteria (both sign positivity and parity status).
  * Handles boundary condition (`0`) in the default `else` branch.

---

## 📊 Decision Matrix & Truth Flow

| Test Input ($x$) | Relational Tests | Evaluated Branch | Console Output |
| :---: | :---: | :---: | :--- |
| `14` | $x > 0$ (`True`) $\land$ $x \pmod 2 == 0$ (`True`) | Branch 2 (`elif`) | `"The number is positive and even"` |
| `7` | $x > 0$ (`True`) $\land$ $x \pmod 2 \neq 0$ (`True`) | Branch 3 (`elif`) | `"The number is positive and odd"` |
| `-12` | $x < 0$ (`True`) | Branch 1 (`if`) | `"The number is negative"` |
| `0` | $x < 0$ (`False`), $x > 0$ (`False`) | Fallback (`else`) | `"The number is zero"` |

---

## 💻 Getting Started & Execution

### Option 1: Run Online in Google Colab (Zero Setup)
Click the badge below to run and interact with the notebook directly in your browser:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/islamyasser424-design/Python-Task--01/blob/main/Python_Task_01.ipynb)

### Option 2: Run Locally via Git & Jupyter

1. **Clone the repository:**
   ```bash
   git clone https://github.com/islamyasser424-design/Python-Task--01.git
   cd Python-Task--01
   ```

2. **Launch in Jupyter Notebook or VS Code:**
   ```bash
   jupyter notebook Python_Task_01.ipynb
   ```

---

## 👤 Author & Connect

**Islam Yasser**  
*Data Analyst & Business Intelligence Specialist*

* 🌐 **Portfolio Website:** [islamyasser424-design.github.io/portfolio-](https://islamyasser424-design.github.io/portfolio-/)
* 💼 **LinkedIn Profile:** [linkedin.com/in/islam-yasser-55048b378](https://www.linkedin.com/in/islam-yasser-55048b378/)
* 🐙 **GitHub Profile:** [@islamyasser424-design](https://github.com/islamyasser424-design)
* ✉️ **Email:** [islamyasser424@gmail.com](mailto:islamyasser424@gmail.com)

---
<p align="center">
  <sub>Part of the Python Programming & Data Analytics Portfolio series. Built with clean code and rigorous logic standards.</sub>
</p>
