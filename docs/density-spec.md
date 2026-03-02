Density Measurement Spec (DMS)
Version: 1.1
Status: Stable
The Density Measurement Spec defines heuristic metrics used to detect compression stability, verbosity drift, and semantic volatility during multi-stage LLM workflows. These signals are consumed by the Diagnostic Layer and the Control Layer.
Information Density Score (IDS)
IDS estimates semantic compression by dividing distinct propositional claims by total text length.
Definition of propositional claim: any clause with a subject–predicate structure that asserts a state, relationship, or causal link.
Examples:
“Drift increases under load.” → 1 claim
“Drift increases because constraints weaken.” → 2 claims
“Drift increases under load and weak constraints amplify it.” → 2 claims
IDS formula (normalized):
IDS = claims / characters
Redundancy Index (RI)
Measures repetition of semantic units. Higher values indicate verbosity drift or unstable compression.
RI is computed by comparing repeated phrases and structural duplication within the output.
Hedge–Assertion Ratio (HAR)
Measures balance between hedging terms and assertive claims.
Target range: 0.20–0.35
Rationale: below 0.20 suggests overconfidence drift; above 0.35 suggests diluted commitment.
Volatility
Measures change in IDS across pipeline stages.
Volatility = |IDS at stage N – IDS at stage N-1|
Default threshold: 0.005
Values above threshold indicate instability or loss of compression control.
Limitations of DMS
Metrics are heuristic and approximate.
IDS may inflate under hallucination-heavy outputs.
HAR does not distinguish justified uncertainty from evasive hedging.
Volatility may increase naturally during long-context degradation.
Use Within Ironbound
Density metrics feed into the Demon Detection Layer (DDL) and influence routing decisions in ILP v2.1.
Density does not enforce correctness; it indicates structural stability.
End of specification.