## 10 — Software Reliability
 
Software Reliability is the probability that software will perform its required functions, without failure, for a specified period under specified conditions.
 
### Core Concepts
- **Failure**: observable incorrect behavior/output of the system.
- **Fault (defect/bug)**: underlying incorrect code/logic that *causes* a failure when executed under certain conditions.
- **Error**: human mistake that leads to a fault being introduced.
### Reliability vs Availability
| Aspect | Reliability | Availability |
|---|---|---|
| Definition | Probability of failure-free operation over a time interval | Probability system is operational at a given point in time |
| Concerned with | Continuity of correct service | Uptime (including after recovery from failure) |
| Formula (steady-state) | — | `Availability = MTTF / (MTTF + MTTR)` |
 
### Reliability Measurement
- Common metrics: **MTTF** (Mean Time To Failure), **MTTR** (Mean Time To Repair), **MTBF** (Mean Time Between Failures = MTTF + MTTR), failure rate/failure intensity (failures per unit time).
### Reliability Models
- **Software Reliability Models**: mathematical models predicting failure occurrence over time based on observed failure data — used to estimate current reliability and forecast future failures (e.g., growth-based models tracking cumulative failures against test time).
- **Reliability Growth**: as testing/debugging proceeds, faults are removed and failure intensity decreases — modeled to predict when a reliability target will be met and to decide when testing can stop.
### Reliability Engineering
- Practices spanning the life cycle to achieve reliability targets: fault avoidance (careful design/coding), fault detection (testing/reviews), fault tolerance (redundancy, error handling), and reliability prediction/measurement.
### Practical Takeaway
- Reliability is a *statistical/probabilistic* property (over a time interval), unlike correctness which is binary — important distinction for SLAs.
- Reliability growth models help decide a defensible "stop testing" point rather than testing indefinitely.
- Availability matters independently of reliability — a system with frequent but quickly-repaired failures can have high availability yet low reliability.
### Quick Reference
| Term | Meaning |
|---|---|
| Failure | Observable incorrect behavior |
| Fault | Underlying code defect causing failure |
| MTTF | Mean Time To Failure |
| MTTR | Mean Time To Repair |
| MTBF | MTTF + MTTR |
| Reliability Growth | Failure intensity decreases as testing/debugging proceeds |