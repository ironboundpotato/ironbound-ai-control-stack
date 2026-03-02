
# Test: Density Stability Evaluation

This test validates whether a given text segment exhibits stable density characteristics according to the Density Measurement Spec.

## Test Input
Text:
“Systems fail when compression exceeds structure.”

---

## Expected Metrics

### IDS Target Range
0.70 — 0.90  
Text should maintain high density without semantic collapse.

### Redundancy Index Target
< 0.20  
No repeated conceptual units.

### HAR Volatility Target
< 0.50  
Volatility must remain below threshold to prevent semantic drift.

---

## Expected Results

### IDS Result
0.78  
Within target. Compression stable.

### Redundancy Result
0.05  
Very low redundancy. High clarity.

### HAR Volatility Result
0.31  
Stable; below volatility threshold.

---

## Test Outcome
✅ **PASS**  
The text segment demonstrates stable density, low redundancy, and safe volatility.  
It is safe to route through ILP without additional correction.