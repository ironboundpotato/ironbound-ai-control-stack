# Ironbound AI Control Stack Architecture Overview  
Version: 2.1  
Status: Stable

This document provides a top-level architectural map for the Ironbound AI Control Stack.  
It defines how the major components of the system relate to each other and where detailed specifications can be found.

---

# Layer Overview

The Ironbound stack is composed of **three integrated layers**:

---

## 1. Measurement Layer  
Provides density metrics such as:  
- Information Density Score  
- Redundancy Index  
- Hedge–Assertion Ratio  
- Volatility  

These metrics detect compression instability and semantic drift.  
**Full details:** `/docs/density-spec.md`

---

## 2. Diagnostic Layer  
Implements the Twelve Demon Ontology v2.1.  
This layer classifies output deviations into twelve drift types with assigned severity levels (L1–L4).

**Full details:** `/docs/demon-ontology-v2.1.md`

---

## 3. Control Layer  
Implements the Ironbound Lockstep Protocol (ILP v2.1).

This adaptive orchestration system:  
- Routes stages according to demon severity  
- Enforces bounded correction cycles  
- Manages snapshots  
- Applies safety-triggered isolation  

**Full details:** `/docs/ilp-v2.1.md`

---

# Control Flow Summary