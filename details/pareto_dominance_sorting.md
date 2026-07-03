# Pareto Dominance Sorting

Pareto Dominance Sorting partitions a set of candidate solutions into hierarchical fronts. A solution strictly dominates another if it is at least as good in all objectives and strictly better in at least one. The non-dominated solutions form the first front, and the process repeats to isolate consecutive Pareto frontiers.

## Conceptual Diagram

```mermaid
flowchart TD
    Candidates["All Candidates"] --> Compare["Pairwise Dominance Comparison"]
    Compare --> Front1["Front 1 (Non-dominated)"]
    Compare --> Front2["Front 2 (Dominated by Front 1)"]
    Compare --> Front3["Front 3 (Dominated by Front 2)"]
```

---

[← Back to README](../README.md)
