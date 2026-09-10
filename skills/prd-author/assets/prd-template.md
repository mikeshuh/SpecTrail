# Product or feature name

<!-- Recommended starting template, not a verified company standard. Replace prompts with content and remove authoring guidance from the finished PRD. This template has received an independent agent critique but has not yet been evaluated through drafting trials. -->

> **Choose the depth:** For a small, understood change, retain the problem and its basis, scope boundaries, intended behavior and acceptance check, relevant verification/release implications, and consequential unknowns. Combine or omit other sections when they add no decision value; do not invent metrics or a business hypothesis to fill space. For larger work, use the fuller structure below and only relevant optional modules. For an exploratory idea, mark unresolved behavior as proposed or unknown and focus on the next learning decision. Missing information that affects a decision must remain visible at any depth.

**Owner:** [Name or unassigned]  
**Maturity:** [Exploratory draft / scope proposal / accepted delivery baseline; identify any blockers for the requested decision]  
**Decision requested:** [What the reader needs to decide]  
**Last updated:** [Date]  
**Timing:** [Confirmed constraint / proposed target / unknown]  
**Supporting links:** [Inputs, designs, technical proposal, related work]

<!-- Exploratory draft frames the problem and uncertainties; scope proposal presents choices for a decision. Use accepted delivery baseline only when the responsible decision-maker has actually accepted the identified scope/version and its implementation-blocking decisions are resolved. Record who accepted it, when, and the source of that acceptance here; identify any remaining release blockers. A review or comment alone does not establish acceptance. Do not invent a separate approval process. -->

**Summary:** [In a short paragraph: the target user, problem, proposed change, and intended benefit. Identify the largest uncertainty if it changes how this document should be read.]

## 1 Problem and evidence

[Who encounters the problem, when it occurs, how they handle it now, and why the result is inadequate. Explain why addressing it matters now. Distinguish the user from the buyer or administrator if relevant.]

**Evidence:** [Summarize the strongest supplied observations with source references. State limitations, conflicting evidence, and missing research. A request is evidence of a request; it is not automatically evidence of widespread demand.]

**Assumptions:** [List only assumptions that materially affect the problem or proposed direction. Do not manufacture research to fill this section.]

<!-- Optional evidence register when multiple sources need tracking. -->

| ID | Source and location | Observation | Limitation |
| --- | --- | --- | --- |
| E1 | [File, page, line, link, or dated note] | [What the source actually supports] | [Coverage, age, uncertainty] |

## 2 Outcomes and success

**User outcome:** [What the person should accomplish more successfully.]  
**Business or operational outcome:** [Why the organization benefits, if known.]  
**Hypothesis:** [Why the proposed change is expected to produce the outcome.]

| Measure | Definition and population | Baseline | Target and status | Method and review window |
| --- | --- | --- | --- | --- |
| Primary outcome | [Observable signal of benefit] | [Known with source / unknown] | [Proposed / agreed / undecided] | [How and when assessed] |
| Guardrail if relevant | [Adverse effect to monitor] | [Known / unknown] | [Boundary and its basis] | [How and when assessed] |

[Explain what result would support continuing, changing scope, or stopping. If measurement is premature, state the learning objective and what evidence is needed next. A proposed numerical target needs a stated basis in evidence, constraints, or explicit reasoning, plus its assumptions and validation needed. Without a defensible basis, leave it undecided; do not generate a number merely to fill this table.]

## 3 Scope and tradeoffs

**Included now:** [The smallest coherent scope that delivers the intended journey.]  
**Excluded or deferred:** [The exclusions a reader could otherwise reasonably assume are included.]  
**Key tradeoff:** [The important alternative, why the proposed scope is preferred, and the cost of that choice.]  
**Decision status:** [Proposal or actual user decision, with reference if available.]

[Use priorities only when they distinguish choices. Explain what would be cut first if necessary. Do not silently convert agent recommendations into approved requirements.]

## 4 Critical user journeys

### Journey J1

**Actor and trigger:** [Who starts and why.]  
**Preconditions:** [Relevant access, data, or state.]  
**Main flow:** [Short sequence from trigger to meaningful result.]  
**Successful outcome:** [What the user can observe or accomplish.]  
**Relevant exceptions:** [Failure, empty state, cancellation, retry, recovery, or permission boundary.]  
**Design reference:** [Optional prototype, workflow, or integration sequence.]

[Add another journey only when it exposes meaningfully different requirements.]

## 5 Requirements and acceptance criteria

### R1 Requirement title

**Requirement:** [Observable behavior under specified conditions.]  
**Priority and status:** [Priority with meaning; proposed or agreed.]  
**Basis:** [E1 evidence / D1 user decision / A1 assumption / explicit agent proposal.]  
**Journey:** [J1, if applicable.]

**Acceptance criteria:**

- [Given a relevant starting condition, when an action occurs, the observable result is…]
- [Relevant boundary or failure behavior.]

**Verification:** [Test, demonstration, inspection, analysis, or linked evaluation; state missing fixtures or unresolved thresholds.]  
**Open detail:** [Only if unresolved; explain whether it blocks this requirement.]

<!-- Repeat for each distinct requirement. Criteria can also be written in plain language. Keep compound requirements separate when they can fail independently. -->

## 6 Constraints and dependencies

[Record constraints that affect the product: deployment environment, data availability, compatibility, performance, accessibility, privacy, permissions, cost, or supplied policy obligations. Include thresholds with their workload, units, measurement boundary, and status.]

[For each binding constraint, link to a requirement's acceptance criteria or an explicit release check with a verification method. State unresolved verification conditions and whether they block implementation or release; do not duplicate the requirement text.]

**Dependencies:** [What must be supplied or decided elsewhere, owner if known, and impact if unavailable.]  
**Technical design boundary:** [Link detailed architecture. Identify any binding technology choice and why it is required.]

## 7 Evaluation and rollout

**Before further investment:** [Research, prototype, feasibility check, or unresolved assumption to test.]  
**Before release:** [Required behavioral verification and applicable domain checks.]  
**Initial audience and rollout:** [Pilot, preview, phased rollout, direct release, or undecided; explain the choice.]  
**After release:** [Outcome review, relevant monitoring, feedback source, and owner if known.]  
**Recovery:** [When relevant, rollback or fallback behavior and triggers.]  
**Adoption needs:** [Documentation, onboarding, migration, training, or support when needed.]

[For an exploratory PRD, keep this section proportionate to the next decision. A proposed plan is not evidence that testing or rollout occurred.]

## 8 Decisions and open questions

[When consequential inputs conflict, record both positions with their sources, dates, and decision status; identify affected requirements and the decision needed. Do not infer approval or supersession from recency alone. Preserve established decisions unless an explicit change or a decision from the responsible person resolves the conflict. Ask for clarification when it blocks the requested decision; otherwise keep it visible as unresolved.]

| ID | Decision or uncertainty | Basis and status | Impact and next action |
| --- | --- | --- | --- |
| D1 | [Consequential scope decision] | [Who decided and where; or proposal] | [Consequence and affected requirements] |
| A1 | [Material assumption] | [Why assumed; not confirmed] | [How to check and consequence if false] |
| Q1 | [Unanswered question] | [Unknown] | [Blocking or nonblocking; owner if known] |

**Next decision:** [The one most useful decision to move this document forward.]  
**Material revision history:** [What changed, why, and which requirements were affected.]

<!-- OPTIONAL MODULES: Add only relevant content, preferably under the matching core section. The prompts below are not automatic requirements. Delete the modules from the final PRD if unused. -->

## Optional enterprise module

[User, administrator, buyer, approver differences; roles and access; tenant boundaries; audit events; deployment and data restrictions; migration and support. Identify actual sources for policy constraints and unresolved specialist review.]

## Optional API and infrastructure module

[Caller journey; input/output contract; errors and retry behavior; compatibility and versioning; resource limits; representative workload; performance and cost boundaries; operational visibility. Link protocol or architecture detail rather than duplicating it.]

## Optional AI and agent module

**Task and rationale for AI:** [Why AI adds value relative to simpler alternatives.]  
**Human control:** [Allowed actions, confirmation points, correction, cancellation, and fallback.]  
**Quality definition:** [Task-specific correctness, usefulness, and unacceptable failure types.]  
**Evaluation:** [Dataset provenance, representativeness, comparison baseline, rubric, evaluators, repeated runs when needed, and proposed thresholds.]  
**Operational constraints:** [Relevant quality, latency, cost, data-access, and logging boundaries.]  
**Change and monitoring:** [What is re-evaluated when prompts, models, tools, or data change.]

## Optional hardware and embedded module

[Operating conditions, power or resource budgets, interfaces, compatibility, qualification, manufacturing and lifecycle constraints. Identify needed specialist review; do not assume a software template covers the complete assurance process.]

## Author review before sharing

- Every consequential claim is sourced, attributed to a decision, or labeled as an assumption or proposal.
- Scope, journeys, requirements, constraints, and criteria agree with one another; binding constraints have linked verification.
- Conflicting consequential inputs are explicitly resolved by a recorded decision or remain visible with their impact; none were silently discarded.
- Metrics distinguish baselines, proposed targets, and measured results.
- The reader can identify the next decision and any blockers.
- Empty boilerplate has been removed; missing information that matters remains visible.
- Review or acceptance is recorded only if it actually happened; the maturity label matches what was accepted and which blockers remain.

<!-- Adapt this template using the accompanying skill instructions. Its structure is a research-informed recommendation, not a verified company standard. -->
