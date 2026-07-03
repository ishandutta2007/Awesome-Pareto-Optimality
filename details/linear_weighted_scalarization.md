# Linear Weighted Scalarization Era

Linear Weighted Scalarization is the traditional baseline for multi-objective optimization (MOO). It works by assigning static multipliers (weights) to each conflicting goal to combine them into a single global loss function. While simple and computationally efficient, its major limitation is its inability to capture non-convex regions of the true Pareto Frontier, meaning key trade-offs may be skipped entirely.

## Conceptual Diagram

```mermaid
flowchart TD
    Loss1["Loss 1 (e.g., Accuracy)"] -->|* alpha| Weighted1["Weighted Loss 1"]
    Loss2["Loss 2 (e.g., Latency)"] -->|* beta| Weighted2["Weighted Loss 2"]
    Weighted1 & Weighted2 --> Sum["Global Loss (L = alpha*L1 + beta*L2)"]
    Sum --> Optimizer["Single-Objective Optimizer"]
```

---

[← Back to README](../README.md)
