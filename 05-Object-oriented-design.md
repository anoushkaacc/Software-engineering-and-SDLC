## 05 — Object-Oriented Analysis and Design (OOAD)
 
OOAD models a system as a collection of interacting **objects** (instances of **classes**) that encapsulate both data and behavior, in contrast to the function-centric view of structured design.
 
### Core Concepts
- **Class**: template/blueprint defining attributes and operations (behavior).
- **Object**: a runtime instance of a class with its own state.
- **Abstraction**: modeling only relevant attributes/behavior for a given context, hiding irrelevant detail.
- **Encapsulation**: bundling data and operations together, restricting direct external access (information hiding).
- **Inheritance**: a class (subclass) derives attributes/operations from another (superclass), enabling reuse and specialization.
- **Polymorphism**: same operation/interface behaves differently depending on the object's actual class (overriding/overloading).
### Object-Oriented Analysis (OOA)
- Focuses on *what* the system must do, modeled through real-world objects/domain concepts.
- **Domain Analysis**: studying the problem domain to identify relevant classes, objects, and relationships independent of implementation.
- **Identifying Classes and Objects**: derived from nouns in requirement statements, domain entities, or responsibilities.
- **Actors**: external entities (users/systems) that interact with the system.
- **Use Cases**: descriptions of system functionality from an actor's perspective — a sequence of interactions achieving a goal.
### Object-Oriented Design (OOD)
- Refines the analysis model into implementable classes, adding design-level detail: interfaces, data structures, algorithms, and relationships suited for coding.
### Relationships Between Classes
| Relationship | Description | Strength | Example |
|---|---|---|---|
| **Association** | General structural link between classes | Weak | `Student` — `Course` |
| **Aggregation** | "Has-a" relationship; whole-part but parts can exist independently | Medium | `Department` has `Professors` |
| **Composition** | Strong "has-a"; parts cannot exist without the whole (lifecycle bound) | Strong | `Car` has `Engine` |
| **Generalization / Inheritance** | "Is-a" relationship; subclass specializes superclass | Structural (hierarchy) | `Car` is a `Vehicle` |
| **Dependency** | One class relies on another temporarily (e.g., as a method parameter) | Weakest | `OrderProcessor` depends on `Logger` |
 
### Design Patterns
- Reusable, proven solutions to recurring design problems in OOD (e.g., Singleton, Factory, Observer, Strategy) — captured as templates of interacting classes/objects rather than finished code.
### Practical Takeaway
- OOAD maps naturally to real-world domain modeling — improves communication with non-technical stakeholders via use cases and class diagrams.
- Composition over inheritance is generally preferred in modern design to reduce tight coupling from deep class hierarchies.
- Correctly distinguishing aggregation vs composition affects object lifecycle management (e.g., cascade deletes in persistence layers).
### Quick Reference
| Term | Meaning |
|---|---|
| Encapsulation | Data + behavior bundled, access restricted |
| Inheritance | Reuse/specialization via "is-a" |
| Polymorphism | Same interface, different behavior |
| Aggregation | "Has-a", parts independent |
| Composition | "Has-a", parts lifecycle-bound |
| Use Case | Functional interaction between actor and system |