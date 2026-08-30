## 06 — UML (Unified Modeling Language)
 
UML is a standardized, general-purpose graphical modeling language for visualizing, specifying, constructing, and documenting the artifacts of an object-oriented software system.
 
### Core Concepts
- **UML Building Blocks**: Things (structural: class, interface, use case, node; behavioral: interaction, state machine), Relationships (association, dependency, generalization, realization), Diagrams (visual representations grouping things and relationships).
- UML diagrams split into **Structural** (static) and **Behavioral** (dynamic) categories.
### Types / Classification
 
| Diagram | Category | Purpose |
|---|---|---|
| **Use Case Diagram** | Behavioral | Shows actors, use cases, and their relationships — captures functional requirements |
| **Class Diagram** | Structural | Shows classes, attributes, operations, and relationships (association, aggregation, composition, generalization) |
| **Object Diagram** | Structural | Snapshot of objects (class instances) and their links at a point in time |
| **Sequence Diagram** | Behavioral | Shows time-ordered message exchange between objects for a scenario |
| **Communication Diagram** | Behavioral | Shows object interactions focused on links/structure rather than time order (formerly "collaboration diagram") |
| **Activity Diagram** | Behavioral | Models workflow/business process logic — control flow, decisions, parallelism (like a flowchart) |
| **State Machine Diagram** | Behavioral | Models states of an object and transitions triggered by events |
| **Component Diagram** | Structural | Shows organization/dependencies among software components (modules, interfaces) |
| **Deployment Diagram** | Structural | Shows physical deployment of artifacts on hardware nodes |
 
### Relationships in UML
| Relationship | Meaning | Notation |
|---|---|---|
| Association | Structural link between classes | Plain line |
| Aggregation | Whole-part, part can exist independently | Line with hollow diamond at whole |
| Composition | Whole-part, part's lifecycle bound to whole | Line with filled diamond at whole |
| Generalization | Inheritance ("is-a") | Line with hollow triangle arrow at parent |
| Realization | Class implements an interface | Dashed line with hollow triangle arrow |
| Dependency | One element uses another temporarily | Dashed line with open arrow |
 
### UML for Analysis and Design
- **Analysis phase**: Use Case Diagrams (requirements), initial Class Diagrams, Activity Diagrams (business workflows).
- **Design phase**: detailed Class Diagrams, Sequence/Communication Diagrams (object interaction logic), State Machine Diagrams (complex object behavior), Component/Deployment Diagrams (implementation & deployment architecture).
### Process / Workflow (typical usage across SDLC)
```
Requirements → Use Case Diagram
Analysis      → Class Diagram (conceptual) + Activity Diagram
Design        → Class Diagram (detailed) + Sequence/State Diagrams
Implementation→ Component Diagram
Deployment    → Deployment Diagram
```
 
### Practical Takeaway
- Use Case + Sequence diagrams are the most commonly used pair for translating requirements into interaction logic during design.
- State Machine diagrams are valuable for objects with complex lifecycle behavior (e.g., order status, connection states).
- Component/Deployment diagrams matter most for architecture and DevOps discussions (service boundaries, physical infrastructure).
### Quick Reference
| Diagram | One-line Identity |
|---|---|
| Use Case | Actor-system functional interactions |
| Class | Static structure: classes & relationships |
| Object | Snapshot of instances |
| Sequence | Time-ordered message flow |
| Communication | Structure-focused interaction |
| Activity | Workflow/control flow |
| State Machine | Object states & transitions |
| Component | Software module organization |
| Deployment | Physical hardware/software mapping |
 