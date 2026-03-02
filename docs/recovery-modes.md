# Recovery Modes  
Version: 1.1  
Status: Stable

Recovery Modes define how the Ironbound system responds when drift exceeds acceptable thresholds or structural failure occurs. These modes prevent runaway mutation, preserve constraints, and maintain operator control under extreme conditions.

---

# Safe Mode  
**Purpose:** Reduce system complexity and stabilize output.  
**Behavior:**  
- Density temporarily lowered by 1–2 points  
- No new sections allowed  
- No schema-level changes  

**Used when:**  
- Mild drift  
- Early warning signs appear  

---

# Isolation Mode  
**Purpose:** Contain a corrupted subsystem.  
**Behavior:**  
- Only the affected component is reset  
- Upstream constraints remain locked  
- No cross-module interaction  

**Used when:**  
- Localized drift  
- Role contamination occurs  

---

# Rebuild Mode  
**Purpose:** Restore structural integrity for a damaged layer.  
**Behavior:**  
- Reconstructs affected module from operator specs  
- Keeps external interfaces intact  

**Used when:**  
- Multiple drift classes fire simultaneously  

---

# Snapback Mode  
**Purpose:** Return system to the last known stable state.  
**Behavior:**  
- Loads last stable snapshot  
- Discards unstable output  

**Used when:**  
- Density volatility spikes  
- Entropy jumps  

---

# Hard Reset  
**Purpose:** Total purge of working state.  
**Behavior:**  
- Clears ILP stage  
- Reloads constraints and density  

**Used when:**  
- Repeated failures  
- Persistent drift loops  

---

# BIOS Fail-Safe  
**Purpose:** Minimal mode guaranteeing operator control.  
**Behavior:**  
- All autonomous correction disabled  
- Only constraint and role enforcement remain  

**Used when:**  
- Catastrophic failure  
- System-level corruption is detected  

---

# Role of Recovery Modes  
Recovery Modes ensure the system can degrade gracefully instead of collapsing.  
They protect integrity during long-context reasoning and guarantee that operator authority is never lost.

**End of specification.**