Error Correction Protocols (ECP)
Version: 1.1
Status: Stable
Error Correction Protocols define how the Ironbound system identifies and corrects structural failures.
This includes six fault classes (E1–E6) and six correction modules (CM-1–CM-6).
ECP is used when drift has already manifested and diagnostic signals require active intervention.
Fault Classes
E1 — Role Drift Fault
Cause: Model slips out of assigned role.
Impact: Contaminates downstream logic.
Trigger: Role score ≥ 0.50
E2 — Tone Drift Fault
Cause: Emotional temperature or density diverges from operator specification.
Impact: Breaks consistency and abstraction.
Trigger: Volatility in HAR or sudden density collapse.
E3 — Format Drift Fault
Cause: Output violates required structure.
Impact: Pipeline desynchronization.
Trigger: Missing, reordered, or invented sections.
E4 — Intent Drift Fault
Cause: Output misinterprets operator objective.
Impact: Wrong problem solved.
Trigger: Divergence score ≥ 0.50
E5 — Scope Drift Fault
Cause: Output expands beyond boundaries.
Impact: Framework mutation.
Trigger: Addition of new frameworks, modules, systems.
E6 — Confidence Drift Fault
Cause: Overconfidence or excessive hedging.
Impact: Unreliable reasoning.
Trigger: Confidence pattern mismatch.
Correction Modules
CM-1 — Role Reset
Action: Restart current ILP stage with role lock reinforced.
CM-2 — Density Stabilization
Action: Clamp output within operator density ± 0.5.
CM-3 — Format Restoration
Action: Rebuild section scaffolding from operator blueprint.
CM-4 — Intent Re-Anchor
Action: Rewrite objective from operator’s explicit command only.
CM-5 — Scope Containment
Action: Remove all material outside operator-defined boundary.
CM-6 — Confidence Rebalance
Action: Normalize assertion–hedge ratio.
ECP Routing Logic
Fault → Module
E1 → CM-1
E2 → CM-2
E3 → CM-3
E4 → CM-4
E5 → CM-5
E6 → CM-6
Protocol Execution
Detect drift via DDL
Classify fault class (E1–E6)
Route to correction module
Return corrected output
Reinforce constraints
Resume ILP from same stage unless structural integrity is compromised
Purpose Within Ironbound
ECP prevents small drift fractures from becoming catastrophic failures.
It is the “immune system” of the control stack.
End of specification.