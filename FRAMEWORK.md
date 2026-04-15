# The IMPACT-X Framework
## Measuring Human and AI Contribution in an AI-Augmented World

*Version 0.1 — April 2026*

---

## Origin

This framework began with a question about cricket.

In Test cricket, a batsman who survived 300 balls was celebrated. In ODIs, the metric shifted to runs scored. In T20, the only question that matters is: *what did you do while you were there? Did it help the team win?*

Sunil Gavaskar batted 221 balls for 36 runs in a Lord's Test in 1979 — and India celebrated. He was perfect for his era. Sachin Tendulkar scored 49 ODI centuries — perfect for his era. Vaibhav Suryavanshi scores a century off 35 balls at a strike rate of 206 — perfect for his era.

The professional world is at the same inflection point. We are running Test match scorecards in a T20 world. And AI has not just changed the pace of the game — it has introduced a new player onto the field entirely.

IMPACT-X exists to build the scorecard the new game demands. Not just for humans. Not just for AI agents. For the team of both working together.

---

## The Three-Layer Model

```
┌─────────────────────────────────────────────────────┐
│                    COMBINED IMPACT                   │
│              (Human + AI Team Score)                 │
├──────────────────────┬──────────────────────────────┤
│    HUMAN IMPACT      │       AGENT IMPACT           │
│    (Layer 1)         │       (Layer 2)              │
└──────────────────────┴──────────────────────────────┘
```

Every task, project, or work unit is scored across three layers. The layers are designed to be independent — so that each can be measured separately — but the Combined Score captures what neither can reveal alone.

---

## Foundational Principle: Context Before Measurement

Before measuring anything, the framework requires one prior question:

**What does this work actually require in this moment?**

Not all work is the same. A surgeon in theatre, a negotiator in a boardroom, a developer writing code — these are not evaluated identically. Applying a uniform lens across all of them produces scores that are precise but meaningless.

Every job contains tasks that sit in one of three zones:

### The Three Work Zones

**Preparation Zone**
Research, analysis, planning, drafting, processing information. AI is highly relevant here. Measured by speed, quality, and depth of inputs produced.

**Execution Zone**
The core act that requires this specific human — the consultation, the negotiation, the creative decision, the leadership call. AI assistance is minimal or absent. Measured by judgment quality and outcome.

**Integration Zone**
Follow-up, documentation, communication, synthesis, learning transfer. AI is relevant again. Measured by completeness and downstream value created.

The Work Zone Map for each role is established through a **Work Zone Mapping Session** — a structured 2-hour workshop where team members themselves classify their key tasks. See [work-zone-mapping.md](framework/work-zone-mapping.md) for the full workshop guide.

**Key principle:** Almost no role is 100% human-critical or 100% AI-augmented. The real question — for every role, every task — is *at which moments does AI help, and at which moments must the human fully show up?*

---

## Layer 1: Human IMPACT Score

The Human IMPACT Score measures contribution across six dimensions. Each dimension is scored 0–10 and weighted according to role-specific templates.

### I — Intelligence Leverage
*Did this person use the best available tools to amplify their output?*

Not simply "did they use AI" — but whether they deployed the right tools at the right moments, in their Preparation and Integration Zones, so they could be fully present in their Execution Zone.

**Scoring inputs:**
- Tool utilisation rate: tools used / tools available for this task type
- Time compression ratio: baseline time / actual time for equivalent task
- Output quality delta: quality score of AI-assisted work vs. non-assisted baseline

**Formula:** `IL = (Tools Used / Tools Available) × (Baseline Time / Actual Time) × Quality Delta`

**Floor rule:** Intelligence Leverage cannot account for more than 25% of any role's total IMPACT weight. A single dimension cannot be a proxy for the whole.

---

### M — Multiplier Effect
*Did their work make the team faster, cheaper, or more capable?*

Individual performance that doesn't move the team is incomplete. A T20 batter who scores 30 off 15 and keeps a partnership alive contributes more than one who scores 50 off 60 when the team needed acceleration.

**Scoring inputs:**
- Team velocity change: sprint velocity or cycle time before vs. after contribution
- Dependency unblock rate: number of blockers removed for other team members
- Reuse rate: how many times others built on this person's output

**Formula:** `ME = (Team Velocity After / Team Velocity Before) × Reuse Rate`

---

### P — Problem Depth
*Did they solve the stated task or the actual underlying problem?*

AI handles task completion easily now. What remains irreducibly human is problem diagnosis — the ability to question whether the task itself is the right task.

**Scoring inputs:**
- Brief change rate: did the problem statement change between intake and delivery? Who initiated the change?
- Rework rate: percentage of deliverables requiring significant rework within 30 days
- Stakeholder surprise score: post-delivery survey — *did this solve something you didn't know needed solving?* (1–5)

**Formula:** `PD = (1 - Rework Rate) × Stakeholder Surprise Score`

---

### A — Acceleration
*How much faster did this person move the project than baseline expectation?*

Speed without direction is not impact. Acceleration is only meaningful toward the right outcome. This dimension rewards genuine compression of cycle time through intelligent use of tools, preparation, and judgment.

**Scoring inputs:**
- Cycle time compression: (Expected Days - Actual Days) / Expected Days
- First pass quality rate: percentage of deliverables accepted without significant revision

**Formula:** `A = Cycle Time Compression × First Pass Quality Rate`

---

### C — Client and Stakeholder Value
*Did it create real change for the person who needed it?*

The ultimate T20 metric — did the team win? Not just did you play well individually.

**Scoring inputs:**
- Outcome delta: measurable change in the stakeholder's key metric within 60 days
- Repeat request score: *how likely are you to request this person's contribution again?* (0–10)
- Problem recurrence rate: did the same problem return? (lower = better)

**Formula:** `CV = Outcome Delta × (Repeat Request Score / 10) × (1 - Recurrence Rate)`

---

### T — Team Contribution Index
*Did this raise the floor or ceiling for the people around them?*

The highest-impact professionals in an AI-augmented world are not those who produce the most individually. They are those who make the people around them better.

**Scoring inputs:**
- Knowledge transfer rate: documented processes, templates, or guides created and actively used by others
- Capability delta: measurable improvement in team skill scores quarter over quarter
- Mentoring hours: time spent actively developing others

**Formula:** `TCI = Knowledge Transfer Rate × Team Capability Delta`

---

### Human IMPACT Composite

```
Human IMPACT = (IL × w1) + (ME × w2) + (PD × w3) + (A × w4) + (CV × w5) + (TCI × w6)
```

Where w1–w6 are role-specific weights. See [role-weight-templates.md](templates/role-weight-templates.md) for starting templates across common role types.

**Weights must sum to 1.0. No single dimension may exceed 0.25.**

---

## Layer 2: Agent IMPACT Score

The Agent IMPACT Score measures the contribution of an AI agent or tool to the same task. AI agents are not evaluated on capability benchmarks — they are evaluated on whether they actually made the human and the outcome better.

### A1 — Accuracy Rate
*Did the agent's output require significant human correction before it was usable?*

An agent whose output is used with minimal editing scores high. One whose output is consistently rewritten scores low — because the human spent more time correcting than they saved.

**Formula:** `AR = Accepted Output / Total Output × (1 - Average Edit Depth)`

---

### A2 — Task Compression
*How much faster did the task complete with this agent versus without it?*

**Formula:** `TC = Baseline Time / Actual Time With Agent`

A score above 1.0 means the agent saved time. Below 1.0 means the agent cost time — a critical signal that is currently invisible in most organisations.

---

### A3 — Problem Fit
*Was this the right tool for this task?*

An agent deployed on a task it was not suited for creates more friction than value. This dimension captures task-tool alignment — not just whether the agent performed well in isolation, but whether it was the right choice for this specific context.

**Formula:** `PF = Output Quality Score × Task Relevance Score` (both rated 1–5 by the human who used it)

---

### A4 — Reliability Consistency
*Did the agent perform consistently across repeated uses of the same task type?*

High variance in output quality is a reliability problem that erodes human trust and slows teams down. Consistency matters as much as peak performance.

**Formula:** `RC = 1 - (Standard Deviation of Quality Scores across repeated similar tasks)`

Higher is better. An agent that scores 8/10 every time is more valuable than one that scores 10/10 half the time and 4/10 the other half.

---

### A5 — Human Amplification Rate
*Did using this agent make the human measurably better — or did it create dependency?*

This is the most important dimension in Layer 2. It asks whether the agent elevated the human's contribution or diminished it.

**Formula:** `HAR = Human IMPACT Score With Agent / Human IMPACT Score Without Agent`

- HAR > 1.0 = Agent amplifies the human. This is the signal to scale.
- HAR = 1.0 = Agent is neutral. Evaluate cost vs. convenience.
- HAR < 1.0 = Agent is diminishing human contribution. This is a critical warning.

---

### Agent IMPACT Composite

```
Agent IMPACT = (AR × 0.20) + (TC × 0.20) + (PF × 0.20) + (RC × 0.15) + (HAR × 0.25)
```

Agent weights are standardised — not role-specific — because an agent's performance characteristics should be comparable across contexts.

---

## Layer 3: Combined IMPACT Score

The Combined IMPACT Score measures what the human-AI team achieved together — and whether the combination created more value than either could alone.

```
Combined IMPACT = (Human IMPACT × H-weight) + (Agent IMPACT × A-weight) + Synergy Multiplier
```

### H-weight and A-weight

These are determined by the Work Zone classification:

| Work Zone | H-weight | A-weight |
|-----------|----------|----------|
| Preparation-heavy task | 0.40 | 0.60 |
| Execution-heavy task | 0.80 | 0.20 |
| Integration-heavy task | 0.50 | 0.50 |
| Balanced/Hybrid task | 0.60 | 0.40 |

### The Synergy Multiplier

The Synergy Multiplier is the most important innovation in the Combined layer. It captures whether the human-AI combination achieved something neither could have alone.

```
Synergy Multiplier = Combined Output Quality / (Expected Human Output + Expected Agent Output)
```

**Interpreting the Synergy Multiplier:**

- **> 1.0** = Genuine synergy. The combination created more than the sum of its parts. This is the signal every organisation should be optimising for.
- **= 1.0** = Additive. The combination performed as expected. No friction, no magic.
- **< 1.0** = Friction. The combination produced less than expected. Either the wrong agent was used, the human wasn't trained to use it well, or the task wasn't suited to collaboration.

---

## The Living Framework

IMPACT-X is not a static system. It is built to evolve as AI capabilities change through three mechanisms:

**Annual Zone Review**
Every team re-maps their Work Zones once a year. The question is not "where are we?" but "where has the frontier moved since last time?" Tasks that were human-critical last year may be AI-augmented this year.

**Trigger Event Protocol**
Certain events automatically trigger an unscheduled re-mapping: a significant new AI tool enters the market, a competitor demonstrably achieves something faster, a team member discovers a meaningful new application of existing tools.

**Benchmark Drift Principle**
Impact is never measured against a fixed standard. It is measured relative to current best practice in that role, given the tools available today. The benchmark rises automatically as AI raises the floor for everyone.

---

## The Fairness Protocol

Before any organisation implements IMPACT-X scoring, the following prerequisites must be met and documented:

**Access Prerequisite**
Every person being measured must have had equal access to the AI tools relevant to their role. If a tool has not been provided, it cannot be included in Intelligence Leverage scoring.

**Training Prerequisite**
Every person being measured must have received training in the use of relevant tools — or been given adequate time and resources to self-learn. Measurement without training is not measurement; it is penalty.

**Relative Baseline**
All scores are measured against what is available and accessible to that specific person in that specific role. A team in a resource-constrained environment is benchmarked against what is realistic for them — not against a team with unlimited tool access.

**Human Floor**
No person's IMPACT score can fall below a defined threshold solely because of low Intelligence Leverage. The IL dimension has a hard ceiling of 25% of total weight to prevent a single dimension from becoming a proxy for structural inequality.

See [fairness-protocol.md](templates/fairness-protocol.md) for the full checklist.

---

## Implementation: Four Phases

**Phase 1 — Mapping (Weeks 1–2)**
Run a Work Zone Mapping session for one team. Establish baselines. Begin scoring alongside existing metrics — not instead of them.

**Phase 2 — Calibration (Months 1–3)**
Establish role-specific weight templates. Run IMPACT scores retrospectively on completed work. Identify where scores feel wrong and investigate why — the discomfort is data.

**Phase 3 — Integration (Months 3–6)**
IMPACT scores enter the performance conversation. Not to replace existing frameworks overnight, but to sit alongside them and gradually shift the centre of gravity.

**Phase 4 — Adaptation (Ongoing)**
Annual Zone Reviews become standard. Trigger Event Protocol is owned by team leads. Benchmark Drift is built into how targets are set. The framework is no longer something the organisation does — it is something the organisation is.

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 0.1 | April 2026 | Initial release — Human IMPACT, Agent IMPACT, Combined IMPACT |

---

*This framework is a living document. To propose changes, open an issue or pull request. To submit a case study, use the template in [/case-studies](case-studies/template.md).*
