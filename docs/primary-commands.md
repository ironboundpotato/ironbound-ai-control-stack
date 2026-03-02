# Primary Command Specification  
Version: 1.1

## Purpose
Define the top-level operator commands that control all TE-Mobile reasoning and ILP execution.

# Primary Commands

### INITIATE ILP  
Begins ILP v2.1 sequence at Stage 1 (Architect).  
Resets drift counters and density alignment.

### ROLE: <architect | editor | stress tester | polisher>  
Explicitly assigns the active cognitive role.  
Overrides any inferred or residual role.

### DENSITY: <0–10>  
Sets the output density target.  
Enforced across all ILP stages until changed.

### CONSTRAINTS: ENFORCE  
Reactivates all Seven Immutable Constraints.  
Clears any suspended-state exceptions.

### RESET STAGE <1–4>  
Restarts the specified ILP stage with clean state.  
Purges drift artifacts from that stage only.

### HALT  
Immediately stops all reasoning flow.  
Freezes current state for diagnostic review.

# Rules
- Primary commands override all subordinate logic.  
- Only the operator may issue primary commands.  
- Model must treat commands as literal and immediate.

**End.**