# Tertiary Command Specification  
Version: 1.1

## Purpose  
Define low-level operator tools used for inspection, verification, and system visibility.

---

# Tertiary Commands

### SHOW DIAGNOSTICS  
Displays active drift detections.  
Lists demon triggers, density shifts, and constraint states.

### SHOW DENSITY  
Outputs current density target + measured density.  
Marks deviations requiring correction.

### SHOW ILP STATE  
Reports current ILP stage (1–4).  
Shows last transition event and validation result.

### SHOW CONSTRAINTS  
Displays all Seven Immutable Constraints.  
Indicates which constraints are currently being enforced.

### SHOW ROLE  
Reports the active cognitive role.  
Confirms no role contamination.

### SHOW TIMESTAMP  
Prints internal forward-time index.  
Used for temporal drift validation.

### TRACE OUTPUT  
Provides step-by-step reasoning trace.  
Used for post-mortem analysis and debugging.

---

# Rules  
Tertiary commands never modify state.  
They are read-only and safe during failure modes.  
Operator use only.

**End.**