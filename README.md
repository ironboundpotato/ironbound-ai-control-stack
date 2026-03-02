Ironbound AI Control Stack

Version: 2.1
Status: Stable

A control stack for structured LLM workflows integrating density measurement, drift diagnostics, and adaptive orchestration.

1. Overview

The Ironbound AI Control Stack defines a layered governance system for multi-stage LLM reasoning. It integrates:

Density Measurement Spec (DMS) — detects compression instability and verbosity drift

Twelve Demon Ontology v2.1 — classifies drift modes with severity levels

ILP v2.1 — adaptive, severity-routed orchestration protocol

This stack provides deterministic routing, bounded correction cycles, and controlled recovery behavior. It does not modify model weights or guarantee correctness.

2. Components
Density Measurement Spec (DMS)

Defines IDS, Redundancy Index, Hedge-Assertion Ratio, and volatility thresholds to detect semantic compression instability.

Twelve Demon Ontology v2.1

A hardened diagnostic taxonomy with L1–L4 severity tiers and operational routing guidance.

ILP v2.1 (Ironbound Lockstep Protocol)

An adaptive, demon-aware orchestration system with:

Deterministic stage routing

Loop guards

Snapshot restoration rules

Safety-triggered isolation

Explicit escalation paths

3. Documentation

All system specifications are located in /docs:

/docs/control-stack-overview.md

/docs/density-spec.md

/docs/demon-ontology-v2.1.md

/docs/ilp-v2.1.md

Operator identity and execution context configuration:

/operator/profile.json

Validation and examples:

/validation/examples.md

4. Purpose

Ironbound AI enables:

More stable multi-pass LLM workflows

Explicit drift detection and routing

Transparent orchestration logic

Reproducible correction cycles

It serves as a practical methodology for operators working with complex, multi-step reasoning systems.

5. Status

All v2.1 components are stable.
Future updates require version increments and explicit specification changes.

6. License

This project uses the Gilbert Attribution License v1.1, located in /LICENSE.
