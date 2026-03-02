# Drift Diagnostic Layer (DDL)  
Version: 1.1  
Status: Stable

The Drift Diagnostic Layer evaluates model output for six drift classes and produces a structured diagnostic object used by ILP and the Control Layer. Diagnostics do not correct drift; they classify and quantify it.

---

## Role Drift  
**Definition:**  
Model shifts out of its assigned cognitive function (e.g., Architect begins editing or polishing).

**Signals:**  
- Introduction of revision language  
- Providing examples when not requested  
- Self-reference to role or meta-awareness  

---

## Tone Drift  
**Definition:**  
Emotional temperature or voice diverges from the operator-specified density level.

**Signals:**  
- Sudden enthusiasm, humor, or slang  
- Abrupt flattening or over-formality  
- Inconsistent abstraction layer  

---

## Format Drift  
**Definition:**  
Output stops following the expected structural pattern.

**Signals:**  
- Sections not requested  
- Unordered lists instead of ordered  
- Block formats replaced with narrative  

---

## Intent Drift  
**Definition:**  
The model answers the wrong question or expands beyond operator scope.

**Signals:**  
- New objectives not in prompt  
- Invented tasks  
- Extrapolations without operator direction  

---

## Scope Drift  
**Definition:**  
Output exceeds permitted dimensionality (e.g., adds frameworks, new modules, extra layers).

**Signals:**  
- Additional subsystems  
- New concepts not in existing architecture  
- Hybridization with unrelated frameworks  

---

## Confidence Drift  
**Definition:**  
Output shifts toward unjustified certainty or excessive hedging.

**Signals:**  
- Over-assertive claims without basis  
- Excessive “maybe,” “possibly,” or conditional phrasing  
- Inconsistent commitment in parallel statements  

---

## Diagnostic Object Format

DDL outputs a structured evaluation consumed by the Control Layer:

- **role:** {score, flags}  
- **tone:** {score, deviation}  
- **format:** {score, missing, extra}  
- **intent:** {score, divergence}  
- **scope:** {score, overreach}  
- **confidence:** {score, pattern}  
- **density:** {IDS, RI, HAR, volatility}  

---

## Scoring  
- **0.00–0.24** = Stable  
- **0.25–0.49** = Mild drift  
- **0.50–0.74** = Significant drift  
- **0.75–1.00** = Structural failure  

---

## Purpose Within Ironbound

DDL acts as the stabilizer between raw model output and orchestration rules.  
It classifies failure early so ILP v2.1 can route corrections without expanding scope or harming stability.

**End of specification.**