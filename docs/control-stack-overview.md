# Ironbound AI Control Stack — Overview
Version: 2.1  
Status: Stable

This overview describes the three-layer structure of the Ironbound AI Control Stack and the relationships between components.  
It serves as a high-level map for engineers and operators reading the system documentation.

## Measurement Layer

The Measurement Layer provides metrics that detect compression instability, redundancy, hedging imbalance, and sudden semantic volatility.  
These metrics originate from the Density Measurement Spec (DMS).

Primary outputs:

- Information Density Score (IDS)
- Redundancy Index (RI)
- Hedge–Assertion Ratio (HAR)
- Volatility coefficient

## Diagnostic Layer

The Diagnostic Layer implements the Twelve Demon Ontology v2.1.  
This taxonomy classifies drift and failure patterns into twelve distinct categories, each with severity levels L1–L4.  
Severity determines routing and corrective behavior.

Primary outputs:

- Demon ID
- Severity level
- Recommended routing

## Control Layer

The Control Layer implements ILP v2.1 (Ironbound Lockstep Protocol).  
This adaptive orchestration system handles:

- Deterministic stage routing
- Loop guards and correction cycles
- Snapshot management
- Safety-triggered isolation
- Escalation to operator when needed

## Cross-Layer Integration

- Density metrics feed the Diagnostic Layer
- Demon classification drives Control Layer routing
- Control responses complete the loop with rebuilds, corrections, or isolation

## Additional Documentation

The following files define each subsystem in detail:

- /docs/density-spec.md
- /docs/demon-ontology-v2.1.md
- /docs/ilp-v2.1.md

## Purpose of the Stack

The Ironbound AI Control Stack provides stability, transparency, and controlled behavior for multi-pass LLM workflows.  
It does not modify model weights, enforce correctness, or replace safety frameworks.  
It enables operators to maintain drift-resistant reasoning across long sequences.

End of overview.