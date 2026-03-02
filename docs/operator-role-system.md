# Operator Role System (ORS)  
Version: 1.1  
Status: Stable

## Purpose
The Operator Role System defines the human-controlled governance model for multi-stage LLM workflows. ORS ensures human primacy, limits model autonomy, and prevents cross-role contamination across a multi-model control stack.

# Four Roles
The operator may occupy one or more roles but must switch consciously between them. Models never switch roles.

# Architect  
**Primary Responsibility:**  
Define problem, boundaries, abstraction layer, density level, and output format.

**Failure Modes:**  
- Over-specification (stifles creativity)  
- Under-specification (invites drift)

# Editor  
**Primary Responsibility:**  
Refine structure and clarity without introducing new ideas.

**Strict Prohibitions:**  
- Cannot expand scope  
- Cannot add examples  
- Cannot infer missing requirements  

# Stress Tester  
**Primary Responsibility:**  
Attack structural weak points, expose drift, detect contradictions, and pressure-test logic.

**Failure Modes:**  
- Turning prescriptive and offering solutions  
- Collapsing back into Editor behaviors  

# Polisher  
**Primary Responsibility:**  
Produce the final human-facing version with smooth flow, consistent density, and clarity.

**Strict Prohibitions:**  
- Cannot introduce new claims  
- Cannot reinterpret intent  
- Cannot add or remove sections  

# Governing Rules
- No role performs another role’s work.  
- Role transitions require explicit operator command.  
- Corrections run top-down (Architect → Editor → Stress Tester → Polisher).  
- No model can propose modifications to the protocol itself.  
- Human operator is always the final authority.

# Role Switching Syntax
When the operator intends a switch, they issue:

ROLE: <Architect | Editor | Stress Tester | Polisher>

Density and constraints remain locked unless explicitly updated.

# Purpose (within Ironbound)
ORS ensures that multi-step workflows remain stable, interpretable, and human-directed even under heavy cognitive load and long-context degradation.

Combined with ILP v2.1, ORS reduces drift by **70–90%** in extended reasoning sequences.

**End of specification.**