Ironbound AI Control Stack Architecture Overview
Version: 2.1
Status: Stable
This document provides a top-level architectural map for the Ironbound AI Control Stack. It defines how the major components of the system relate to each other and where detailed specifications can be found.
The Ironbound stack is composed of three integrated layers:
Measurement Layer
Provides density metrics such as Information Density Score, Redundancy Index, Hedge–Assertion Ratio, and volatility. These metrics detect compression instability and semantic drift. Full details: /docs/density-spec.md
Diagnostic Layer
Implements the Twelve Demon Ontology v2.1. This layer classifies output deviations into twelve drift types with assigned severity levels (L1–L4). Full details: /docs/demon-ontology-v2.1.md
Control Layer
Implements the Ironbound Lockstep Protocol (ILP v2.1). This adaptive orchestration system routes stages according to demon severity, enforces bounded correction cycles, manages snapshots, and applies safety-triggered isolation. Full details: /docs/ilp-v2.1.md
Control Flow Summary:
Input → Architect → DDL Scan → Editor → DDL Scan → Stress Tester → DDL Scan → Polisher → Final DDL → Output or Correction
Signal Relationships:
Density metrics feed into demon classification.
Demon classification determines routing decisions in ILP.
ILP applies correction cycles, rebuilds, snapshots, or isolation as needed.
This file is an entry point only. For complete specifications, see the documentation in /docs.