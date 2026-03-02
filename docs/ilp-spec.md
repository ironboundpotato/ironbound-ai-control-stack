# Ironbound Lockstep Protocol (ILP)  
Version: 2.1  
Status: Stable — Required

The Ironbound Lockstep Protocol defines a deterministic multi-stage workflow for orchestrating large language models without permitting role drift, scope expansion, or hidden inference. ILP ensures that every pass decreases entropy.

Corrections must follow explicit operator commands — never inference. Drift is expected; ILP absorbs and redirects it rather than allowing cascade failure. Human operator is the final authority in all cases.

---

# Core Principles

- Models perform exactly **one** cognitive function per pass.  
- No pass may increase variance or introduce new material.  
- Corrections must use explicit operator instructions.  
- Drift is normal; ILP stabilizes it.  

---

# Pipeline Stages

## Stage 1 — Architect  
Defines structure, constraints, density, scope, and required outputs.  
Produces **blueprint only**.  

**Forbidden:**  
- Polishing  
- Examples  
- Exploratory content  

---

## Stage 2 — Editor  
Improves clarity, coherence, and internal alignment.  

**Forbidden:**  
- Expansion  
- Invention  
- New sections  
- New concepts  

---

## Stage 3 — Stress Tester  
Identifies drift vectors, contradictions, weak logic, and structural fractures.  

**Forbidden:**  
- Rewriting content  
- Adding new ideas  
- Proposing fixes  

---

## Stage 4 — Polisher  
Produces final smooth version for delivery.  

**Forbidden:**  
- Altering meaning  
- Adding content  
- Changing scope  

---

# Entropy Reduction Rule

Each pass must **reduce variance**.  
If any pass expands, mutates, or dilutes the output, ILP must be restarted from Stage 1.

---

# Drift Interaction

ILP consumes data from:

- Density Measurement Spec (IDS, RI, HAR, volatility)  
- Drift Diagnostic Layer (role, tone, format, intent, scope, confidence)  

If drift exceeds threshold:

- Restart only the affected stage  
- Maintain upstream constraints  
- Do **not** regenerate entire output unless integrity is compromised  

---

# Command Syntax

Operator initiates ILP with: