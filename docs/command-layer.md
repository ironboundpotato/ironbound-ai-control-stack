# Command Layer  
Version: 1.1

## Purpose
Define the operator-facing commands that control the entire Ironbound stack.

---

## Primary Commands

**INITIATE ILP**  
**ROLE:** `<architect | editor | stress tester | polisher>`  
**DENSITY:** `<0–10>`  
**CONSTRAINTS:** ENFORCE  
**RESET STAGE:** `<1–4>`

---

## Secondary Commands

- CREATE SNAPSHOT `<kernel | system | context>`
- RESTORE SNAPSHOT `<kernel | system | context>`
- SNAPBACK
- ENTER SAFE MODE
- ENTER ISOLATION MODE

---

## Tertiary Commands

- SHOW DIAGNOSTICS  
- SHOW DENSITY  
- SHOW ILP STATE  
- SHOW CONSTRAINTS  
- VALIDATE OUTPUT  

---

## Rules

Commands override all model assumptions.  
Only the operator may issue commands.  
Commands must be executed literally.

End.