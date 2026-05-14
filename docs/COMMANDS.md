# CeCell Command Reference  
### Full List of Commands • Usage • Voice Equivalents • Developer Notes

CeCell provides a powerful suite of commands designed to support accessibility‑first, autonomous, and intelligent development workflows.  
This document lists every command, what it does, how to use it, and how developers can extend or integrate it.

---

# 🧭 Command Categories

CeCell commands are grouped into the following categories:

- **Core Activation & Voice**
- **Workspace Intelligence**
- **Patch Generation & Repair**
- **Merge Simulation & Repo Comparison**
- **Memory System**
- **Panels & Views**
- **Developer Utilities**
- **Ascendia Cloud Integration (Future)**

---

# 🎤 1. Core Activation & Voice Commands

## **CeCell: Start**
**Description:**  
Initializes CeCell, loads subsystems, and prepares panels.

**Voice Equivalent:**  
“CeCell start”  
“Start CeCell”

**Developer Notes:**  
Triggers extension activation events.

---

## **CeCell: Voice Command**
**Description:**  
Enables voice‑driven interaction with CeCell.

**Voice Equivalent:**  
“CeCell listen”  
“CeCell command mode”

**Developer Notes:**  
Routes microphone input to the command router.

---

# 🧠 2. Workspace Intelligence Commands

## **CeCell: Analyze Workspace**
**Description:**  
Scans the entire workspace and generates a structured intelligence report.

**Detects:**  
- Framework indicators  
- Dependency mismatches  
- Missing files  
- Build issues  
- Repo health  
- Structure problems  
- Code smells  

**Voice Equivalent:**  
“Analyze workspace”  
“Scan my project”

**Developer Notes:**  
Outputs data to the Workspace Intelligence Panel.

---

## **CeCell: Analyze Active File**
**Description:**  
Runs a focused analysis on the currently open file.

**Voice Equivalent:**  
“Analyze this file”  
“What’s wrong with this file”

---

## **CeCell: Show Workspace Indicators**
**Description:**  
Displays all detected indicators in the Workspace Panel.

**Voice Equivalent:**  
“Show indicators”  
“Workspace health”

---

# 🩹 3. Patch Generation & Repair Commands

## **CeCell: Generate Patch (Active File)**
**Description:**  
Creates a patch for the currently open file.

**Voice Equivalent:**  
“Generate patch for this file”  
“Fix this file”

**Developer Notes:**  
Outputs `.patch` content and diff preview.

---

## **CeCell: Generate Patch (Workspace)**
**Description:**  
Creates a patch covering the entire workspace.

**Voice Equivalent:**  
“Generate workspace patch”  
“Fix the whole project”

---

## **CeCell: Apply Patch**
**Description:**  
Applies a previously generated patch.

**Voice Equivalent:**  
“Apply patch”  
“Apply the fix”

---

## **CeCell: Rollback Patch**
**Description:**  
Reverts the last applied patch.

**Voice Equivalent:**  
“Undo patch”  
“Rollback fix”

---

## **CeCell: Show Patch Diff**
**Description:**  
Displays a diff view of the generated patch.

**Voice Equivalent:**  
“Show patch diff”  
“Show changes”

---

# 🔍 4. Merge Simulation & Repo Comparison

## **CeCell: Predict Merge Failures**
**Description:**  
Simulates a merge and predicts conflicts before they occur.

**Voice Equivalent:**  
“Predict merge issues”  
“Check merge safety”

---

## **CeCell: Simulate Merge**
**Description:**  
Runs a full merge simulation and generates a merge plan.

**Voice Equivalent:**  
“Simulate merge”  
“Show merge plan”

---

## **CeCell: Compare Local vs Remote Repo**
**Description:**  
Compares the local repository with its remote counterpart.

**Voice Equivalent:**  
“Compare with remote”  
“Repo comparison”

---

## **CeCell: Compare Repos**
**Description:**  
Compares two repositories or two branches.

**Voice Equivalent:**  
“Compare repos”  
“Compare branches”

---

# 🧩 5. Memory System Commands

## **CeCell: Write Memory Entry**
**Description:**  
Adds a new memory entry to CeCell’s memory subsystem.

**Voice Equivalent:**  
“Save memory entry”  
“Remember this”

---

## **CeCell: Search Memory**
**Description:**  
Searches memory entries by keyword.

**Voice Equivalent:**  
“Search memory for X”  
“What do you remember about Y”

---

## **CeCell: Open Memory Panel**
**Description:**  
Opens the Memory Panel.

**Voice Equivalent:**  
“Open memory panel”  
“Show memory”

---

# 🖥️ 6. Panel Commands

## **CeCell: Open Autonomous Panel**
**Description:**  
Displays the Autonomous Panel.

**Voice Equivalent:**  
“Open autonomous panel”  
“Show autonomous tasks”

---

## **CeCell: Open Workspace Intelligence Panel**
**Description:**  
Displays workspace indicators, structure, and health.

**Voice Equivalent:**  
“Open workspace panel”  
“Show workspace intelligence”

---

# 🛠️ 7. Developer Utility Commands

## **CeCell: Reload Extension**
**Description:**  
Reloads CeCell without restarting VS Code.

**Voice Equivalent:**  
“Reload CeCell”

---

## **CeCell: Show Logs**
**Description:**  
Opens CeCell’s internal logs.

**Voice Equivalent:**  
“Show CeCell logs”

---

## **CeCell: Debug Mode**
**Description:**  
Enables verbose logging and developer diagnostics.

**Voice Equivalent:**  
“Enable debug mode”

---

# 🌐 8. Ascendia Cloud Integration (Future)

These commands will activate once Ascendia Cloud integration is enabled:

- **CeCell: Sync Memory to Cloud**  
- **CeCell: Load Cloud Memory**  
- **CeCell: Cloud Workspace Analysis**  
- **CeCell: Autonomous Cloud Refactor**  
- **CeCell: Multi‑Repo Cloud Intelligence**

---

# 🧱 Adding New Commands (Developer Guide)

To add a new command:

### 1. Register it in `package.json`
```json
"contributes": {
  "commands": [
    {
      "command": "cecell.myNewCommand",
      "title": "CeCell: My New Command"
    }
  ]
}
