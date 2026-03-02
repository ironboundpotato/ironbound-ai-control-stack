# Example: Density Evaluation and Stability Check

This example demonstrates how the Density Measurement Spec is applied to evaluate compression quality and detect instability before it becomes drift.

## Input Text
“Time is a forward-only structure correcting itself through pressure and meaning.  
People malfunction when internal load exceeds available structure.”

---

## Step 1 — Generate Raw Metrics

### IDS (Information Density Score)
Measures how much conceptual content exists per token.

Result: **0.82**  
Interpretation: High density; compression is efficient without losing clarity.

### Redundancy Index
Detects repeated semantic units.

Result: **0.12**  
Interpretation: Very low redundancy; message is tightly packed.

### HAR Volatility (High-Activation Region Variance)
Checks for unstable conceptual jumps.

Result: **0.41**  
Interpretation: Moderate volatility; this is expected in abstract conceptual writing.

---

## Step 2 — Stability Assessment

### Compression Stability
High density + low redundancy = **stable compression**.

### Semantic Continuity
Volatility < 0.50 → **structure remains coherent**.

### Drift Susceptibility
No indicators of scope widening, hallucination, or intent mutation.  
Susceptibility rating: **Low**

---

## Step 3 — Recommended Routing
Because the text is stable:

- No recompression required.  
- No boundary reinforcement needed.  
- Safe to pass through ILP without triggering Stress Tester corrections.

---

## Step 4 — Reformulated Output (Optional)
If lower volatility is desired, apply density smoothing:

“Time moves in one direction, correcting itself through pressure.  
People falter when their internal load exceeds their structure.”

Volatility reduced to **0.28**.

---

This example demonstrates how density metrics guide routing, correction, and stability decisions across the control stack.