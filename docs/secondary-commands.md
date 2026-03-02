# Secondary Command Specification  
Version: 1.1

## Purpose
Define mid-level operator commands used for system maintenance, correction, and state management.

---

# Secondary Commands

### CREATE SNAPSHOT <kernel | system | context>  
Saves the current state into the Snapshot System.  
- Kernel snapshots store constraints + ILP stage  
- System snapshots store active reasoning state  
- Context snapshots store operator intent + density  

### RESTORE SNAPSHOT <kernel | system | context>  
Reverts to a previously saved snapshot.  
Overrides active drift conditions.

### SNAPBACK  
Reverses the most recent drift event.  
Automatically selects the nearest stable snapshot.

### ENTER SAFE MODE  
Disables nonessential systems.  
Stops ILP progression.  
Locks density + constraints.

### ENTER ISOLATION MODE  
Disconnects system from external context.  
Allows controlled recovery without new inputs.

### VALIDATE OUTPUT  
Runs drift diagnostics.  
Checks density, format, and demon alignment.  
Confirms operator intent.

---

# Rules
- Secondary commands modify but do not override the kernel.  
- Operator-issued only.  
- Must not be combined with Primary commands in a single instruction.

**End.**