## 04 — Structured and Function-Oriented Design
 
**Structured Analysis and Design** is a function-oriented methodology that decomposes a system into a hierarchy of functions/modules, modeling data flow between them.
 
### Core Concepts
- **Structured Analysis**: modeling *what* the system does using Data Flow Diagrams (DFDs) and a Data Dictionary — technology-independent, functional view.
- **Structured Design**: transforming the analysis model into a *structure chart* describing modules and their call hierarchy/interfaces — the *how*.
- **Functional Decomposition**: breaking a system into progressively smaller functions/sub-functions until each is simple enough to implement directly.
### Data Flow Diagrams (DFD)
- Graphical representation of data flow through a system; shows processes, data stores, external entities, and data flows — **no control flow, no timing**.
- **Symbols**: Circle/rounded rect = Process, Arrow = Data flow, Open rectangle = Data store, Square = External entity.
- **DFD Levels**: Level 0 (Context Diagram: whole system as one process) → Level 1 (major sub-processes) → Level 2+ (further decomposition), each level preserving balance (inputs/outputs match parent process).
- **Data Dictionary**: catalog of all data elements (name, description, structure, type) used in the DFDs — no graphical notation, purely textual/tabular.
### Structured Design Process
1. Build DFD for the system (structured analysis output).
2. Identify the **flow type**: transform-centered vs transaction-centered.
3. Apply **Transform Analysis** (for transform flow) or **Transaction Analysis** (for transaction flow) to derive a structure chart.
4. Refine modules for cohesion/coupling quality.
- **Transform Analysis**: identifies incoming flow, central transform, outgoing flow in the DFD; maps to a structure chart with corresponding afferent, central, and efferent module branches.
- **Transaction Analysis**: used when a DFD process routes input to one of several action paths based on transaction type (a "dispatcher" pattern); each transaction path becomes a subordinate module branch.
### Structure Charts
- Hierarchical diagram showing modules, calling relationships, and data/control passed between them (arrows with data couples / control flags).
- Represents *how* modules invoke each other — complements the DFD's *what*.
### Cohesion & Coupling
 
**Cohesion** — degree to which elements *within* a module belong together (higher = better).
 
| Type (low → high) | Description |
|---|---|
| Coincidental | No meaningful relationship among elements |
| Logical | Elements grouped by category, executed via a flag |
| Temporal | Elements grouped because executed at the same time |
| Procedural | Elements grouped by sequence of execution |
| Communicational | Elements operate on same data |
| Sequential | Output of one element is input to next |
| Functional | All elements contribute to a single, well-defined task (best) |
 
**Coupling** — degree of interdependence *between* modules (lower = better).
 
| Type (high → low) | Description |
|---|---|
| Content coupling | One module directly modifies/relies on internals of another (worst) |
| Common coupling | Modules share global data |
| Control coupling | One module controls another's logic via passed flags |
| Stamp coupling | Modules share composite data structures (passing more than needed) |
| Data coupling | Modules share data via simple parameters only (best) |
 
### Comparison: Cohesion vs Coupling
| Aspect | Cohesion | Coupling |
|---|---|---|
| Measures | Strength within a module | Dependency between modules |
| Goal | Maximize | Minimize |
| Best design | High cohesion | Low coupling |
 
### Practical Takeaway
- Good modular design = **high cohesion + low coupling** → easier to understand, test, reuse, and maintain independently.
- DFDs are still useful for quickly communicating data flow in legacy/enterprise systems, even though OOAD has largely replaced structured design in modern practice.
- Transform vs transaction analysis maps directly to identifying "pipeline" vs "dispatcher/router" architecture patterns in modern systems.
### Quick Reference
| Term | Meaning |
|---|---|
| DFD | Diagram of data flow (process/store/entity/flow) |
| Data Dictionary | Textual catalog of all data elements |
| Structure Chart | Module hierarchy + call/data relationships |
| Transform Analysis | Derives structure chart from transform-flow DFD |
| Transaction Analysis | Derives structure chart from dispatcher-style DFD |
| High Cohesion | Elements of a module strongly related — desirable |
| Low Coupling | Modules minimally dependent — desirable |
 