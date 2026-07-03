# Multi-Task Gradient-Based Era

The Gradient-Based Era integrated multi-objective optimization directly into backpropagation. Using algorithms like MGDA (Multiple Gradient Descent Algorithm), shared parameters are optimized by finding the exact intersection vector of conflicting task gradients. This ensures all tasks improve without any single task dominant-updating and erasing others.

## Conceptual Diagram

```mermaid
flowchart TD
    Task1["Task 1 Gradient (g1)"] --> MGDA["MGDA Solver"]
    Task2["Task 2 Gradient (g2)"] --> MGDA
    MGDA --> CommonGrad["Common Gradient Direction (g_shared)"]
    CommonGrad --> Update["Update Shared Parameters"]
```

---

[← Back to README](../README.md)
