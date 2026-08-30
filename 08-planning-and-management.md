## 08 — Software Project Planning and Management
 
Software Project Management covers planning, estimating, scheduling, staffing, and risk/configuration control activities needed to deliver a software project successfully.
 
### Core Concepts
- **Software Project Planning**: establishing scope, estimating size/effort/cost/schedule, and defining risk and resource plans before/along development.
- **Software Size Estimation** underlies all other estimates (effort, cost, schedule).
### Size & Effort Estimation Techniques
| Technique | Description |
|---|---|
| **LOC (Lines of Code)** | Estimate size by counting/predicting source lines; simple but language-dependent, hard to estimate early |
| **Function Point Analysis (FPA)** | Measures size from functional user requirements (inputs, outputs, inquiries, files, interfaces) weighted by complexity — language-independent |
| **COCOMO** (Constructive Cost Model) | Empirical model estimating effort/cost/schedule from estimated size (KLOC) |
 
### COCOMO
| Project Type | Characteristics | Effort Formula (Basic COCOMO: Effort = a×(KLOC)^b) |
|---|---|---|
| **Organic** | Small team, familiar/in-house, flexible requirements | a=2.4, b=1.05 |
| **Semi-detached** | Medium size/complexity, mixed experience team | a=3.0, b=1.12 |
| **Embedded** | Tight constraints (hardware, regulations), complex | a=3.6, b=1.20 |
 
- **COCOMO Cost Drivers** (Intermediate COCOMO): attributes that adjust nominal effort — grouped as Product attributes (reliability, complexity), Hardware attributes (execution time/storage constraints), Personnel attributes (analyst/programmer capability, experience), Project attributes (tools, schedule constraints).
- **Effort Estimation**: derived from size + cost drivers (person-months).
- **Schedule Estimation**: development time formula, e.g. Basic COCOMO `Tdev = c×(Effort)^d` — schedule is not linearly reducible by adding people (see Brooks' Law).
### Staffing & Scheduling
- **Rayleigh-Norden Model**: models staffing level over a project's life cycle as a curve that rises, peaks, then tapers off — effort is not uniformly distributed across the schedule.
- **Brooks' Law**: *"Adding manpower to a late software project makes it later"* — due to added communication overhead and ramp-up time for new members.
- **Project Scheduling**: breaking work into tasks/milestones with dependencies and timelines (e.g., via Work Breakdown Structure, Gantt/PERT charts).
### Risk Management
| Step | Description |
|---|---|
| **Risk Identification** | Identify potential risks (technical, schedule, cost, personnel, requirements) |
| **Risk Assessment** | Estimate probability and impact of each identified risk; prioritize |
| **Risk Mitigation** | Plan actions to reduce probability/impact (avoidance, transfer, reduction) |
| **Risk Monitoring** | Continuously track risks and mitigation effectiveness through the project |
 
### Configuration Management
- **Software Configuration Management (SCM)**: process of systematically controlling changes to software artifacts (code, docs, requirements) throughout the life cycle — includes identification of configuration items, version control, change control, status accounting, and audits.
### Practical Takeaway
- FPA is preferred over LOC for early, technology-independent size estimation; COCOMO effort estimates depend heavily on correct project-type classification.
- Brooks' Law is a direct caution against "throwing people at" schedule slippage.
- Risk management should run continuously, not as a one-time upfront exercise — reassess as the project progresses.
- SCM (via Git or similar) is the backbone of reproducible, auditable software delivery.
### Quick Reference
| Term | Meaning |
|---|---|
| LOC | Size estimate by lines of code |
| FPA | Size estimate from functional requirements |
| COCOMO | Empirical effort/cost/schedule estimation model |
| Brooks' Law | Adding people to a late project delays it further |
| Rayleigh-Norden | Staffing follows a rise-peak-taper curve over time |
| SCM | Controlled management of artifact versions/changes |
 