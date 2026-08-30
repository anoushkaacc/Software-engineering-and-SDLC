## 07 — Software Testing
 
Software Testing is the process of executing a program with the intent of finding defects and evaluating whether it meets specified requirements.
 
### Core Concepts
- **Verification vs Validation**:
  - *Verification*: "Are we building the product right?" — checks conformance to specification, done via reviews, inspections, static analysis.
  - *Validation*: "Are we building the right product?" — checks the product satisfies actual user needs, done via dynamic testing/execution.
- **Testing Principles**: Testing shows presence of defects, not their absence; exhaustive testing is impossible; test early (start testing activities as early as possible in SDLC); defect clustering (most defects concentrate in few modules); pesticide paradox (repeating same tests stops finding new bugs — tests must evolve); testing is context-dependent; absence-of-errors is a fallacy (a bug-free but unusable system still fails).
### Testing Levels
| Level | Scope | Performed By |
|---|---|---|
| **Unit Testing** | Individual module/function in isolation | Developer |
| **Integration Testing** | Interfaces/interaction between integrated modules | Developer/Tester |
| **System Testing** | Complete, integrated system against requirements | Test team |
| **Acceptance Testing** | System against user/business needs, in real or simulated environment | Client/User |
| **Regression Testing** | Re-testing after changes to ensure no new defects introduced | Any level, repeated |
 
### Types / Classification
 
| Approach | Basis | Description |
|---|---|---|
| **Black-Box Testing** | Specification-based | Tests functionality without knowledge of internal code structure |
| **White-Box Testing** | Structure-based | Tests internal logic/paths using knowledge of code |
 
**Black-Box Techniques**
| Technique | Description |
|---|---|
| Equivalence Partitioning | Divide input domain into classes expected to be handled the same way; pick one representative per class |
| Boundary Value Analysis | Test at and just around boundaries of input ranges (min, max, min-1, max+1) — defects cluster at boundaries |
| Cause-Effect Graphing | Model logical relationships between input conditions (causes) and outputs (effects) as a graph, convert to a decision table |
| Decision Table Testing | Tabulate combinations of conditions and corresponding actions; ensures all logical combinations are tested |
 
**White-Box Techniques**
| Technique | Description |
|---|---|
| Path Testing | Ensure all/critical independent execution paths through code are exercised |
| Control Flow Graph (CFG) | Graphical representation of a program's control flow: nodes = statements/blocks, edges = control transfer |
| Cyclomatic Complexity | `V(G) = E − N + 2` (E = edges, N = nodes) — gives the number of independent paths; also = number of decision points + 1 |
 
### Test Coverage Criteria
| Criterion | Requirement |
|---|---|
| **Statement Coverage** | Every statement executed at least once (weakest) |
| **Branch Coverage** | Every branch (true/false outcome of decision) executed at least once |
| **Condition Coverage** | Every individual boolean sub-condition evaluated to both true and false |
| **MC/DC** (Modified Condition/Decision Coverage) | Every condition independently affects the decision outcome, in addition to branch coverage — used in safety-critical systems (strongest of these) |
 
### Process / Workflow
```
Unit → Integration → System → Acceptance
   ↘________ Regression testing after every change _______↗
```
 
### Test Case Design & Adequacy
- **Test Case Design**: deriving inputs, execution conditions, and expected outputs to test a specific objective (functional or structural).
- **Test Adequacy**: a criterion to decide "have we tested enough?" — typically defined via coverage criteria.
- **Test Coverage**: quantitative measure of how much of the code/requirements has been exercised by a test suite (e.g., % statement coverage).
### Practical Takeaway
- Black-box techniques (equivalence partitioning, BVA) are efficient for reducing test case count while catching high-probability defect zones.
- Cyclomatic complexity is a practical proxy for both testing effort (minimum independent paths) and code maintainability/risk.
- MC/DC is mandated in avionics/safety-critical standards (e.g., DO-178C) — know it if working in regulated domains.
### Quick Reference
| Term | Meaning |
|---|---|
| Verification | Building product right (spec conformance) |
| Validation | Building right product (user needs) |
| Cyclomatic Complexity | V(G) = E − N + 2 |
| Statement Coverage | Weakest — every line executed |
| MC/DC | Strongest common criterion — used in safety-critical SW |
| Regression Testing | Re-test after change to catch new defects |