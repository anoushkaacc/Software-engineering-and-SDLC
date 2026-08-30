## 03 — Requirements Engineering
 
**Requirements Engineering (RE)** is the process of eliciting, analyzing, documenting, validating, and managing the requirements of a software system.
 
### Core Concepts
- **Requirements Engineering Process**: Feasibility Study → Elicitation → Analysis → Specification → Validation → Management (iterative, not strictly linear).
- **User Requirements**: high-level statements, in natural language, of what the system should do for stakeholders/customers.
- **System Requirements**: detailed, precise elaboration of user requirements — the basis for design; may use structured/formal notations.
### Key Points
- **Elicitation techniques**: interviews, questionnaires, observation, use cases, joint application development (JAD), prototyping, brainstorming.
- **Analysis**: detecting conflicts, ambiguities, overlaps, and infeasibility among gathered requirements; classifying and prioritizing them.
- **Requirements Specification**: converting analyzed requirements into a well-structured document.
- **SRS (Software Requirements Specification)**: formal document capturing all functional and non-functional requirements; serves as contract between client and developer.
  - Good SRS qualities: Correct, Unambiguous, Complete, Consistent, Verifiable, Modifiable, Traceable.
- **Requirements Validation**: checking the SRS against real stakeholder needs (reviews, walkthroughs, prototyping) — different from "verification" (checking against spec).
- **Requirements Management**: tracking, controlling changes to, and maintaining traceability of requirements throughout the project.
- **Requirements Change Management**: formal process to evaluate, approve/reject, and incorporate change requests without destabilizing the project (change control board, impact analysis).
### Types / Classification
| Type | Description | Example |
|---|---|---|
| **Functional Requirements (FR)** | What the system *should do* — features, behaviors | "System shall allow user login via email/OTP" |
| **Non-Functional Requirements (NFR)** | Quality attributes / constraints on the system | Performance, security, usability, scalability, reliability |
 
| NFR Subtype | Description |
|---|---|
| Product requirements | Speed, reliability, portability |
| Organizational requirements | Standards, delivery process constraints |
| External requirements | Legal, regulatory, interoperability |
 
### Process / Workflow
```
Feasibility Study → Elicitation → Analysis → Specification (SRS)
        ↑_______________ Validation ____________|
                  ↓
          Requirements Management (change control, traceability)
```
 
### Practical Takeaway
- FR vs NFR distinction drives both design decisions and test strategy (functional tests vs performance/security tests).
- A weak SRS is the single biggest source of late-stage rework — invest early.
- Requirements traceability (linking requirement → design → code → test) is essential for change impact analysis and audits.
### Quick Reference
| Term | Meaning |
|---|---|
| Elicitation | Gathering requirements from stakeholders |
| Analysis | Resolving conflicts/ambiguity, prioritizing |
| SRS | Formal document of all requirements |
| Validation | Confirming SRS matches real stakeholder needs |
| FR | What the system does |
| NFR | How well the system does it (quality attributes) |
 
---