# Shamir's Secret Sharing - Constant Term Solver

This project implements a simplified version of **Shamir's Secret Sharing** to find the constant term of a polynomial given some of its roots.

## Problem Statement

Given an unknown polynomial of degree `m`:

f(x) = a_m x^m + a_{m-1} x^{m-1} + ... + a_1 x + c

- Coefficients `a_m, ..., a_1, c` are **positive integers**.  
- `a_m ≠ 0` ensures the polynomial is degree `m`.  
- We need at least `k = m+1` roots to solve for coefficients.  

The task is to **compute the constant term `c`**. The roots are provided in a **JSON format** with different number bases.

---

## Input Format

Example JSON:

```json
{
  "keys": { "n": 4, "k": 3 },
  "1": { "base": "10", "value": "4" },
  "2": { "base": "2", "value": "111" },
  "3": { "base": "10", "value": "12" },
  "6": { "base": "4", "value": "213" }
}

