# The 'Alignment Tax' Frontier

The Alignment Tax represents the performance degradation on general capabilities when aligning models to safety constraints. Pushing safety alignment to prevent harmful responses can lead to over-refusal of benign requests. Navigating the Helpful-Harmless Pareto Frontier is critical to balancing usefulness and safety.

## Conceptual Diagram

```mermaid
flowchart TD
    Alignment["Safety Fine-Tuning (DPO/RLHF)"] --> Safe["High Harmlessness"]
    Alignment --> Tax["Refusal Underfitting (Lower Helpfulness)"]
    Tax & Safe --> Tradeoff["Pareto-Optimal Boundary Control"]
```

---

[← Back to README](../README.md)
