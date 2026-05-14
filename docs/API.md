# CeCell Internal API Documentation  
### Engines • Memory Schema • Command Router • Panels • Cloud Integration

This document provides a complete reference for CeCell’s internal APIs.  
It is intended for developers extending CeCell, integrating it with Ascendia Cloud, or building new engines, commands, or panels.

---

# 🧩 Overview

CeCell exposes several internal APIs:

- **Command Router API**  
- **Patch Engine API**  
- **Merge Engine API**  
- **Workspace Analyzer API**  
- **Memory Subsystem API**  
- **Panel (Webview) API**  
- **Local Client API**  
- **Cloud Client API (Future)**  

Each subsystem is modular and can be extended or replaced.

---

# 🧭 1. Command Router API

The command router is the central dispatcher for all CeCell commands.

### **Registering a Command**
```ts
vscode.commands.registerCommand("cecell.myCommand", async () => {
  return commandRouter.run("myCommand");
});
