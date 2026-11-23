# yoSalsa — motion-based dance practice
**Independent product design and development · MediaPipe Pose · React/TypeScript · Capacitor · 2026**

[Luke's portfolio](https://lukedooley.design)

## The problem
Dance-practice feedback needs to be timely and understandable. A pose-tracking prototype also needs to distinguish tracking quality from the quality of someone's movement: a weak camera signal should not become misleading feedback.

## My contribution
I designed and developed the mobile practice application across interaction design, movement scoring, performance feedback, real-device testing and TestFlight beta distribution.

## What I built and investigated
- A phone-camera pose-analysis loop using MediaPipe.
- Practice attempts and feedback around movement scoring.
- A React + Vite + Capacitor host for physical-iPhone benchmarking.
- Deterministic scorer-validation tooling and controlled model comparisons.

## A measured technical decision
A recorded physical-iPhone benchmark on **11 September 2026** ran five consecutive 12-second attempts using MediaPipe Pose Landmarker full.

| Observation | Recorded result |
| --- | --- |
| Analysis rate | 29.8–29.9 frames/second |
| p95 inference time | 18–21 ms |
| Dropped frames | 0–0.3% |

Those results supported choosing the full model as the V1 default, with MoveNet retained as a fallback/debug adapter. These are results from one recorded device session, not a performance promise for every device or proof of scoring accuracy.

## What remains important
Tracking speed and valid dance feedback are different questions. Scoring validation, movement definitions and testing with practitioners remain part of the product's development.

## Status
TestFlight beta / development. This is **not** a fully launched App Store product. The private repository includes a benchmark/scoring implementation and is not a complete public product distribution.

This showcase summarises recorded engineering evidence and my product contribution; it does not publish private source or test data.
