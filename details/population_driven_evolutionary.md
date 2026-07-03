# Population-Driven Evolutionary Era

The Evolutionary Era ported Pareto tracking into genetic algorithms. Popular frameworks like NSGA-II (Non-dominated Sorting Genetic Algorithm II) and SPEA2 maintained a diverse population of candidate solutions. Individuals are ranked based on non-domination layers, and crowding distance metrics are employed to ensure a uniform distribution of candidates along the Pareto Frontier.

## Conceptual Diagram

```mermaid
flowchart TD
    InitPop["Initial Population"] --> Evaluate["Evaluate Objectives"]
    Evaluate --> NonDomSort["Non-dominated Sorting"]
    NonDomSort --> CrowdingDist["Calculate Crowding Distance"]
    CrowdingDist --> Select["Select Parents (Elitist Selection)"]
    Select --> Crossover["Crossover & Mutation"]
    Crossover --> NewPop["New Population"]
    NewPop --> Evaluate
```

---

[← Back to README](../README.md)
