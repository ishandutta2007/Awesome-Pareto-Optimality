# High Cost of Infinite Frontier Sampling

Sampling a dense Pareto Frontier using evolutionary or grid search requires training thousands of configurations, which is extremely expensive. Mitigation techniques like GradNorm and dynamic loss weighting balance task training dynamically in a single run, significantly reducing compute costs.

## Conceptual Diagram

```mermaid
flowchart TD
    MultiLoss["Multi-Task Loss Functions"] --> GradNorm["GradNorm Optimizer"]
    GradNorm -->|Dynamic Weighting| Balance["Auto-adjust Task Priorities on-the-fly"]
    Balance --> SingleRun["Find Pareto Frontier in a Single Training Run"]
```

---

[← Back to README](../README.md)
