Ironbound Lockstep Protocol (ILP)
Version: 2.1
Status: Stable — Required
The Ironbound Lockstep Protocol defines a deterministic multi-stage workflow for orchestrating large language models without permitting role drift, scope expansion, or hidden inference. ILP ensures that every pass decreases entropy.
Core Principles
Models perform exactly one cognitive function per pass.
No pass may increase variance or introduce new material.
Corrections must follow explicit operator commands — never inference.
Drift is expected; ILP absorbs and redirects it rather than allowing cascade failure.
Human operator is the final authority in all cases.
Pipeline Stages
Stage 1 — Architect
Defines structure, constraints, density, scope, and required outputs.
Produces blueprint only; no polishing, no examples, no exploratory content.
Stage 2 — Editor
Improves clarity, coherence, and internal alignment.
Forbidden: expansion, invention, new sections, new concepts.
Stage 3 — Stress Tester
Identifies drift vectors, contradictions, weak logic, and structural fractures.
Forbidden: rewriting content, adding new ideas, proposing fixes.
Stage 4 — Polisher
Produces final smooth version for delivery.
Forbidden: altering meaning, adding content, changing scope.
Entropy Reduction Rule
Each pass must reduce variance.
If any pass expands, mutates, or dilutes the output, ILP must be restarted from Stage 1.
Drift Interaction
ILP consumes data from:
Density Measurement Spec (IDS, RI, HAR, volatility)
Drift Diagnostic Layer (role, tone, format, intent, scope, confidence)
If drift exceeds threshold:
Restart only the affected stage
Maintain upstream constraints
Do not regenerate entire output unless integrity is compromised
Command Syntax
Operator initiates ILP with:
INITIATE ILP v2.1
ROLE: Architect → Editor → Stress Tester → Polisher
DENSITY: <0–10>
CONSTRAINTS: Seven Immutable Constraints enforced
Restart Syntax
RESET STAGE <1–4>
Density and constraints remain locked unless explicitly changed.
Design Purpose
ILP is the stabilizer that allows multi-model orchestration, long-context reasoning, and modular pipeline design without drift spirals or runaway inference.
It is the backbone of Ironbound’s reliability under cognitive load.
End of specification.