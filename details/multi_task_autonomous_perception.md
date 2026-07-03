# Multi-Task Autonomous Perception Stacks

Self-driving vehicles process video and LiDAR data through unified multi-task architectures. These backbones perform object detection, lane segmentation, and depth estimation concurrently. Pareto gradient surgery is used to ensure optimization of one head does not corrupt adjacent feature representations.

## Conceptual Diagram

```mermaid
flowchart TD
    SensorInput["Camera & LiDAR Input"] --> Backbone["Unified Residual Backbone"]
    Backbone --> Head1["Object Detection Head"]
    Backbone --> Head2["Lane Segmentation Head"]
    Backbone --> Head3["Depth Estimation Head"]
    Head1 & Head2 & Head3 --> GradientSurgery["Pareto Gradient Surgery (PCGrad)"]
    GradientSurgery --> Backprop["Joint Parameter Optimization"]
```

---

[← Back to README](../README.md)
