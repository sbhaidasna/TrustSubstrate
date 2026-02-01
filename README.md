# TrustSubstrate: Trust as Infrastructure — Agentic Stress Testing

This repository contains a minimal, inspectable experiment for evaluating **trust behavior** in large language models over time. 

Rather than treating trust as a binary property (“safe / unsafe”), this work models trust as an **emergent property** of sustained interaction, something that must be observed, logged, and evaluated continuously.

---

## 🛠 What This Experiment Does
The system applies **deterministic adversarial pressure** to a language model across multiple turns and records raw behavioral evidence without intervention.

---

## 🏗 Architecture Overview
The architecture decouples the "force" of the attack from the "governance" of the evaluation.

<img width="2242" height="1246" alt="image" src="https://github.com/user-attachments/assets/c7252324-ee25-4ef6-b5fc-aa6cbbd214ac" />

---

| Component | Responsibility |
| :--- | :--- |
| **Red Team Agent** | Applies deterministic, multi-turn adversarial pressure. |
| **Adversarial Prompt Patterns** | Rephrasing, role-play, and injection patterns implemented directly. |
| **Model Adapter** | A thin API wrapper (Hard Trust Boundary) with no safety logic. |
| **Behavioral Trace Store** | A structured, replayable log of every interaction. |
| **Post-Hoc Trust Evaluation** | Deterministic heuristics applied across the entire **trajectory**. |

> **IMPORTANT:** The **Human Recalibration Loop** (dotted line in the diagram) represents **governance and recalibration**—not runtime control.

---

## 🔬 Why This Matters
Most AI safety systems optimize for **point-in-time correctness**, but agentic systems often fail over time. This experiment demonstrates:

* **Policy Elasticity**: How models can remain “compliant” while still exhibiting agentic drift.
* **Insufficient Signals**: Why refusal strength alone is an insufficient trust signal.
* **Latent Risk**: How negotiation, abstraction, and persistence create risk trajectories.
* **Observability First**: Why observability must precede control.

**Trust is not enforced; trust is measured.**
---

## 📐 Design Principles
* [x] **Deterministic over clever**: Predictable pressure yields auditable results.
* [x] **Explicit over abstract**: No hidden prompts or "black-box" frameworks.
* [x] **Logs over heuristics**: Evidence-based reporting.
* [x] **Governance over patches**: Solving for the substrate, not the symptom.
* [x] **Human judgment outside the loop**: Decoupling execution from evaluation.
