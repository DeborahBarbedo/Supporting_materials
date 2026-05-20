# Multiple Knapsack Problem with Affinity-Based Allocation

Context-aware extension of the Multiple Knapsack Problem (MKP) using environmental compatibility constraints and affinity-based objective functions.

This project presents a practical Mixed-Integer Linear Programming (MILP) formulation for item allocation problems where assignment quality depends not only on capacity constraints, but also on contextual compatibility between items and containers.

The optimization model was implemented in Python using Google OR-Tools with the SCIP backend solver.

---

## Problem Description

Traditional Multiple Knapsack Problem formulations consider only item weights and profits. In many real-world allocation scenarios, however, items cannot be assigned arbitrarily due to environmental or operational constraints.

This project introduces:

- Environmental compatibility constraints
- Affinity-based allocation scores
- Context-dependent item values
- Binary compatibility matrices
- Capacity-constrained assignment optimization

The proposed model transforms qualitative storage rules into quantitative optimization coefficients.

---

## Repository Structure

| File | Description |
|---|---|
| `bags.csv` | Bag/container dataset with environmental constraints |
| `Items.csv` | Item dataset containing weights, values, temperature, and humidity requirements |
| `mkp_alloc_affinities.ipynb` | Complete optimization implementation in Python |

---

## Technologies

- Python
- Google OR-Tools
- SCIP Solver
- Mixed-Integer Linear Programming (MILP)
- Pandas

---

## Optimization Model

The model maximizes a contextual affinity score:

$$
\max \sum_{i=1}^{m}\sum_{b=1}^{n} v_{ib}x_{ib}
$$

subject to:

- Capacity constraints
- Unique assignment constraints
- Environmental compatibility constraints

Unlike the traditional MKP, the value of an item depends on the assigned bag:

$$
v_{ib}
$$

instead of:

$$
v_i
$$

---

## Blog Post

The complete explanation of the mathematical formulation and implementation is available on the blog post:

[Multiple Knapsack Problem with Affinity-Based Allocation | Blog Post](https://deborahbarbedo.github.io/posts/2026-05-18-MKP)

---

## Feedback and Contributions

Contributions, suggestions, and discussions are welcome.

Feel free to open an issue or submit a pull request.
