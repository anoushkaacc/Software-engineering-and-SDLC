## 11 — Software Maintenance
 
Software Maintenance is the modification of a software system after delivery to correct faults, improve performance, adapt to a changed environment, or prevent future problems.
 
### Types / Classification
| Type | Purpose | Trigger |
|---|---|---|
| **Corrective Maintenance** | Fix faults/defects found after release | Reported bugs/failures |
| **Adaptive Maintenance** | Adapt software to a changed environment (OS, hardware, regulations) | External environment change |
| **Perfective Maintenance** | Improve performance, add new features, enhance maintainability | Evolving user requirements |
| **Preventive Maintenance** | Improve future maintainability, prevent latent faults from surfacing | Proactive code/documentation improvement |
 
*(Corrective + Adaptive + Perfective + Preventive together account for the bulk of typical maintenance effort, with perfective/adaptive work usually dominating over purely corrective work.)*
 
### Maintenance Process
1. Identify need for change (bug report, request, environment change).
2. Analyze impact and feasibility.
3. Design and implement modification.
4. Regression test to ensure no new defects.
5. Release updated version; update documentation.
### Core Concepts
- **Maintenance Cost**: typically the largest share of total software life-cycle cost; driven by system complexity, documentation quality, and staff turnover/familiarity with the code.
- **Software Evolution**: the continuous change of software over time as it is maintained — governed informally by "laws of software evolution" (systems must continually adapt or become progressively less useful; complexity tends to increase unless actively managed).
- **Legacy Software**: older software, often business-critical, that is difficult/costly to maintain due to outdated technology, lost documentation, or original-developer turnover, yet too risky/expensive to fully replace.
### Software Re-engineering & Reverse Engineering
- **Reverse Engineering**: analyzing existing software (code/binaries) to recover its design or specification — understanding *what* a legacy system does without having original documentation.
- **Software Re-engineering**: restructuring/rewriting existing software into a new form (e.g., improved architecture, new technology stack) while preserving its functionality — often begins with reverse engineering, followed by restructuring and forward engineering into the new system.
### Process / Workflow (Re-engineering)
```
Legacy System → Reverse Engineering (recover design/specs)
             → Restructuring (improve internal structure)
             → Forward Engineering (build new/improved system)
```
 
### Practical Takeaway
- Maintenance, not initial development, usually dominates total software cost — architecting for maintainability upfront pays off.
- Distinguishing maintenance types matters for planning/budgeting: corrective work is often reactive/urgent, while perfective/adaptive work can be planned.
- Legacy modernization projects typically follow reverse-engineer → restructure → forward-engineer, especially when documentation is missing or outdated.
### Quick Reference
| Term | Meaning |
|---|---|
| Corrective | Fix reported defects |
| Adaptive | Adjust to environment changes |
| Perfective | Enhance features/performance |
| Preventive | Improve future maintainability |
| Legacy Software | Old, hard-to-maintain but critical system |
| Reverse Engineering | Recover design from existing code |
| Re-engineering | Rebuild system into improved form |