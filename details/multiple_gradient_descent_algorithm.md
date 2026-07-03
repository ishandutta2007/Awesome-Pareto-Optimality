# Multiple Gradient Descent Algorithm (MGDA)

MGDA formulates multi-task learning as a multi-objective optimization problem. It solves for a convex combination of gradients that minimizes the common descent direction norm. If the minimum-norm direction is zero, the optimizer has reached a Pareto critical point where no further multi-objective improvement is possible.

## Conceptual Diagram

```mermaid
flowchart TD
    Gradients["Task Gradients: g1, g2, ..., gT"] --> ConvexSolver["Solve: min ||sum alpha_i * g_i||^2 s.t. sum alpha = 1"]
    ConvexSolver --> MinNormGrad["Minimum-Norm Gradient (g_descent)"]
    MinNormGrad --> Update["Apply Descent Update"]
```

---

[← Back to README](../README.md)
