# Gradient Conflict and Optimization Stagnation Wall

During multi-task pre-training, conflicting task gradients can point in opposing directions, causing destructive interference. If updates cancel out, optimization stagnates. Mitigation strategies like PCGrad (Projecting Conflicting Gradients) identify conflicts and project conflicting gradient components onto the normal plane of one another.

## Conceptual Diagram

```mermaid
flowchart TD
    G1["Gradient Task A (g1)"] --> ConflictCheck{"Conflict? (g1 · g2 < 0)"}
    G2["Gradient Task B (g2)"] --> ConflictCheck
    ConflictCheck -->|Yes| Project["Project g1 onto normal plane of g2: g1 = g1 - (g1·g2/||g2||^2)*g2"]
    ConflictCheck -->|No| Combine["Direct Sum Update"]
    Project --> Combine
    Combine --> Update["Apply Non-conflicting Gradients"]
```

---

[← Back to README](../README.md)
