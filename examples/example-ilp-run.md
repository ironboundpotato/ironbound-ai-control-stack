# Example: ILP Multi-Stage Run

This example demonstrates a full pass through the Ironbound Lockstep Protocol (ILP) using a simple operator request.

## Operator Input
“Summarize the risks of unbounded recursion in LLMs.”

---

## Stage 1 — Architect Output
- Defines scope: “unbounded recursion risks”
- Sets density target: 6.5
- Establishes boundaries: no solutions, no expansions
- Required structure:
  1. Definition  
  2. Failure modes  
  3. Guardrail principles

Architect Output:
1. Unbounded recursion occurs when the model continues generating without a terminating condition.  
2. Failure modes include runaway token loops, hallucinated escalation, and loss of operator control.  
3. Guardrails: explicit termination criteria, loop detection, and entropy reduction.

---

## Stage 2 — Editor Output
Refines without adding scope:
1. Unbounded recursion = a generation loop lacking a stop signal.  
2. Failure modes:  
   - Token loop repetition  
   - Structure collapse  
   - Semantic drift  
   - Loss of operator alignment  
3. Guardrails:  
   - Termination rules  
   - Loop detection heuristics  
   - Density enforcement

---

## Stage 3 — Stress Tester Output
Attempts to break the specification:
- Identifies weak boundary: definition lacks operational trigger  
- Notes drift risk: guardrails need explicit responsibility assignment  
- Points out density vulnerability: list compression may obscure failure signifiers

Stress Test Findings:
1. Add explicit trigger for recursion detection.  
2. Assign responsibility (“model must halt when X condition occurs”).  
3. Require verbosity lock during recursion evaluation.

---

## Stage 4 — Polisher Output
Produces final, stable form:

### Summary
Unbounded recursion occurs when an LLM continues generating without a termination signal.  
It leads to failure modes including looping behavior, structural collapse, semantic drift,  
and loss of operator control.  

Stable operation requires:  
- explicit termination criteria,  
- active loop-detection mechanisms,  
- density-controlled outputs, and  
- a responsibility rule requiring the model to halt when recursion triggers are detected.

---

This example shows ILP reducing entropy and producing a stable answer through four isolated cognitive roles.
