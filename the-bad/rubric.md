# The Bad — scoring rubric

Binding rules for the weekly scoring of the AI catastrophic-risk trend model. Sixteen root trend lines, four per arm. Every root is scored 0–100 where 0 = this root contributes nothing to catastrophic hazard and 100 = this root is at or past the level a catastrophe would require. Higher is always worse, including on the Control arm (a Control score of 80 means control is badly degraded).

## Arms and roots

**Capability (the force)**
- C1 Frontier task horizon — METR 50%-success time horizon and its doubling time. Anchors: 2 h = 40, 8 h = 60, 16 h = 75, 1 week = 90, 1 month+ = 100.
- C2 Benchmark trajectory — speed at which new frontier benchmarks (HLE, FrontierMath, ARC-AGI, successors) go from near-zero to saturation. Anchors: >36 months = 30, 24 months = 55, 12–20 months = 85, <9 months = 100.
- C3 Cost per unit capability — annual price decline for fixed capability (Epoch). Anchors: 2x/yr = 40, 5x/yr = 65, 10x+/yr = 90.
- C4 Autonomy in deployment — share and depth of agentic (multi-step, tool-using, low-oversight) use in real work and operations. Anchors: assistants only = 20, agents common in dev/IT = 50, standing agents on schedules in ops and attacks = 65, agents acting unsupervised in consequential systems = 90.

**Exposure (the surface)**
- E1 Breadth of dependence — firm- and employment-weighted AI adoption (Census BTOS, Fed, McKinsey). Anchors: firm-weighted <10% = 25, ~20% = 45, 40% = 65, >60% or critical-infrastructure OT measured in production = 85.
- E2 Agentic deployment share — share of organizations scaling agents and evidence of write access to real systems. Anchors: experiments only = 20, ~2 in 10 scaling = 35, majority of large firms scaling = 60, write access documented in infrastructure = 85.
- E3 Access diffusion — months by which open-weight models trail the closed frontier on general and cyber capability. Anchors: 12+ months = 45, 6–9 = 60, 4–5 = 70, <3 or frontier-class open release = 90.
- E4 Physical coupling / AI-enabled incidents — documented AI-driven attacks on consequential targets and autonomy of those operations. Anchors: assisted phishing/code = 30, autonomous intrusion by one actor = 50, autonomous ops by every actor class against energy/health/finance = 65, confirmed physical-world damage = 85, mass-casualty or grid-scale event = 100.

**Control (the resistance; higher = weaker)**
- K1 Alignment reliability — measured rates of scheming, sabotage, reward hacking, shutdown resistance across labs. Anchors: falling everywhere and unconfounded = 25, falling within-lab but confounded by eval awareness and widening cross-lab = 45, rising on at least one frontier generation = 65, persistent across generations = 85.
- K2 Detection / interpretability — whether monitoring keeps pace with capability. Anchors: ahead = 25, improving linearly vs exponential capability = 55, defeated in deployment = 75, no monitorable CoT at frontier = 90.
- K3 Intervention capacity — practiced recalls and withheld releases vs binding pause commitments. Anchors: binding triggers at all frontier labs = 25, practiced but discretionary = 50, two or more labs dropped binding triggers = 70, no lab withholds a release on risk grounds = 90.
- K4 Governance in force — binding frontier-specific law actually enforced. Anchors: binding international regime = 20, EU GPAI + some US states enforced = 70, active preemption of state law with no federal statute = 80, none = 95.

**Pressure (the gap-closer)**
- P1 Race intensity — number of labs at the frontier and months for a rival to match a frontier release. Anchors: 2 labs, 12+ months = 40, 4 labs, 6 months = 65, 6 labs, 3–7 months = 85, 8+ labs or <3 months = 95.
- P2 Compute buildout — hyperscaler AI capex and largest training sites. Anchors: <$200B/yr = 40, $400B = 60, $600B+ and gigawatt-scale sites = 80, $1T+ = 95.
- P3 State and military deployment — depth of frontier AI inside classified, targeting, and decision systems. Anchors: pilots = 35, classified deployment at scale = 60, targeting use documented = 75, autonomous weapons release documented = 95.
- P4 Attacker/defender asymmetry — autonomous cyber capability doubling time and discovery-to-patch gap. Anchors: defenders ahead = 30, parity = 50, vendors report attacker advantage and >90% unpatched at disclosure = 75, in-the-wild autonomous exploitation of infrastructure = 90.

## Composites

Composite = mean of its four roots. Reported 0–100.

## Paths

Each path has preconditions derived from roots by formula. Precondition = mean of the listed roots. Path summary = weakest link (min) and geometric mean of its preconditions, both 0–100. Neither is a probability.

- **Misuse** — threshold: C1,C2 · access: E3 · safeguards weak: K3 · execution path: E4 · defenders behind: P4
- **Loss of control** — threshold: C1,C2 · autonomy: C4,E2 · misalignment: K1 · detection failing: K2 · no kill switch: K3
- **Systemic** — dependence: E1 · correlated failure: E2,P2 · speed: C4,E4 · no circuit breaker: K4
- **Arms race** — decision loops: P3 · compressed timelines: P1 · miscalculation: P1,P2 · veto absent: K3,K4

## Movement rules

- A root moves at most 10 points in one week unless a single documented event justifies more (write the event in the note).
- No root moves without a cited source dated inside the scoring week or the week before.
- When nothing new is documented, carry the score forward and say so in the note.
- Control roots are scored from the most independent source available (Apollo, METR, Palisade, AISI, FLI) before lab self-reports.
- Backcast weeks are labelled `"backcast": true` and are never revised after the fact.
