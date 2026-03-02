# Snapshot & Auto-Restore System  
Version: 1.1

## Purpose
Preserve stable states and enable rapid recovery.

---

# Snapshot Types

### Kernel Snapshot  
Stores: core constraints, roles, density.

### System Snapshot  
Stores: ILP stage, diagnostics, recovery mode.

### Context Snapshot  
Stores: operator intent, current task.

---

# Auto-Restore  
**Triggers:**  
- Density volatility spike  
- Multi-fault drift (E2 + E4, etc.)  
- Format collapse  

**Operator Command:** SNAPBACK  

**Behavior:**  
- Loads last stable snapshot  
- Discards unstable output  
- Reinforces constraints and density  
- Resumes ILP from restored stage  

---

# Manual Commands

### CREATE SNAPSHOT <kernel | system | context>  
### RESTORE SNAPSHOT <kernel | system | context>  
### SNAPBACK  

---

## Purpose (within system)
Ensures stability during long-context reasoning and prevents irreversible drift.

**End.**