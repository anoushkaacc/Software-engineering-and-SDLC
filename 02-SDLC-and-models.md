## 02 — SDLC & Process Models
 
The **Software Development Life Cycle (SDLC)** is a structured sequence of phases (feasibility, requirements, design, coding, testing, deployment, maintenance) used to develop software systematically. A **process model** is a specific way of organizing these phases.
 
### Core Concepts
- SDLC phases (generic): Feasibility Study → Requirements Analysis → Design → Coding → Testing → Maintenance.
- Process models differ mainly in **ordering, overlap, and iteration** of these phases, and in how they handle risk and changing requirements.
### Types / Classification
 
| Model | Structure | Best Fit | Key Weakness |
|---|---|---|---|
| **Classical Waterfall** | Strict sequential phases, no feedback | Well-understood, stable requirements | No backtracking; unrealistic for real projects |
| **Iterative Waterfall** | Sequential + feedback loops to earlier phases | Most real-world "waterfall" projects | Still document-heavy, slow to adapt |
| **V-Model** | Waterfall bent into a V; each dev phase paired with a test phase | Safety-critical/regulated systems | Rigid, late defect discovery possible |
| **Prototyping** | Build throwaway/quick prototype to clarify requirements, then develop | Unclear/evolving requirements | Prototype may be mistaken for final product |
| **Incremental Development** | Build & deliver in functional increments | Requirements known but delivery needs to be phased | Needs good architecture upfront to avoid rework |
| **Evolutionary Development** | System evolves through repeated refinement (exploratory or throwaway) | Requirements not fully known upfront | Hard to manage/scope; poor visibility of progress |
| **Spiral Model** | Repeated cycles of planning → risk analysis → engineering → evaluation | Large, high-risk projects | Complex, needs risk-assessment expertise |
| **Agile (general)** | Short iterations ("sprints"), continuous customer feedback, working software over documentation | Changing requirements, need for fast delivery | Needs disciplined, collocated/communicative teams |
| **Extreme Programming (XP)** | Agile method emphasizing pair programming, TDD, continuous integration, simple design, refactoring | Small teams, rapidly changing requirements | Demands high developer discipline |
| **Scrum** | Agile framework: Sprints, Product Backlog, Sprint Backlog, Daily Scrum, Sprint Review/Retrospective, roles (Product Owner, Scrum Master, Team) | Iterative delivery with prioritized backlog | Not prescriptive on engineering practices |
 
### Process / Workflow (Spiral Model example)
```
        Plan → Risk Analysis → Engineering → Customer Evaluation
          ↑___________________________________________|
        (repeat spiral, radius = cumulative cost, each loop = one phase)
```
 
### Comparison
 
| Aspect | Predictive (Waterfall/V-Model) | Evolutionary (Agile/Prototyping) |
|---|---|---|
| Requirements | Fixed upfront | Emerge/change over time |
| Planning | Detailed, upfront | Adaptive, iteration-by-iteration |
| Documentation | Heavy | Minimal, working software prioritized |
| Customer involvement | Mainly at start/end | Continuous |
| Risk handling | Assumed low/managed via planning | Managed via short feedback loops |
| Change tolerance | Low | High |
 
| Aspect | Waterfall | Agile |
|---|---|---|
| Delivery | Single delivery at end | Frequent incremental delivery |
| Flexibility | Low | High |
| Feedback | Late | Continuous |
| Best for | Stable, well-understood domains | Volatile, exploratory domains |
 
### Choosing a Process Model
- Well-understood, stable, contractually fixed requirements → **Waterfall / V-Model**.
- Requirements unclear or UI-driven → **Prototyping**.
- Large, high-risk, high-cost project → **Spiral**.
- Need early partial delivery of a large system → **Incremental**.
- Requirements expected to evolve, need speed and customer feedback → **Agile (Scrum/XP)**.
### Practical Takeaway
- Model choice should follow project risk, requirement stability, and delivery constraints — not fashion.
- V-Model's value is early test-case planning (test phase defined alongside each dev phase), useful in regulated domains (avionics, medical).
- Scrum gives process/management structure; XP gives engineering discipline — many teams combine both.
### Quick Reference
| Model | One-line Identity |
|---|---|
| Waterfall | Sequential, document-driven |
| V-Model | Waterfall + parallel verification/validation |
| Prototyping | Clarify requirements via throwaway build |
| Incremental | Deliver in functional chunks |
| Evolutionary | Refine system iteratively as understanding grows |
| Spiral | Risk-driven repeated cycles |
| Scrum | Sprint-based agile management framework |
| XP | Agile engineering practices (TDD, pairing, CI) |
 