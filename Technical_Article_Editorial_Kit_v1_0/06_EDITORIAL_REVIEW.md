# Technical Article Review and Release Gates — v1.0

**Purpose:** Detect technical and editorial defects before they reach Medium. Apply independent review to the **current complete manuscript**, not a single changed paragraph. A satisfying tone or a high aggregate score must never mask a blocker.

## Severity policy

| Severity | Meaning | Required action |
|---|---|---|
| BLOCKER | False mechanism, fabricated evidence, consequential unsupported conclusion, misleading quantitative figure, critical unaddressed risk, improper third-party reproduction | Cannot publish; repair and reverify impacted argument |
| MAJOR | Substantial reasoning gap, missing relevant alternative, ambiguous source attribution, confusing figure, reader transformation not achieved | Rework affected sections; rerun relevant gates |
| MINOR | Wordiness, weak transition, caption polish, redundant sentence, headline optimization | Edit without disturbing correct substance |

## Review passes — perform in order

### Pass A — Technical correctness (blocking)

- [ ] Every central mechanism is technically accurate for the named standard/product/release.
- [ ] Architecture description distinguishes logical model, implementation detail and deployment assumption.
- [ ] Each causal arrow or statement has a defensible explanation, not just correlation.
- [ ] Important error paths, state changes, trust boundaries and invariants are represented correctly.
- [ ] Code is minimal and semantically correct; if claimed tested, there is real verification evidence.
- [ ] Equations have defined variables; example calculations are consistent with assumptions and units.
- [ ] Figures reflect the prose and sources, and vice versa.

### Pass B — Evidence and intellectual honesty (blocking)

- [ ] Consequential claims map to authoritative, accessible sources or reproducible artifacts.
- [ ] Vendor-reported results are attributed, not silently converted into universal truths.
- [ ] Sample sizes, test conditions, baseline fairness and key uncertainty are present where relevant.
- [ ] Reported observation, original experiment, thought experiment and inference are distinguishable.
- [ ] Unverified metrics, experiences, citations and quotes are absent.
- [ ] A good counterexample or competing approach has not been omitted to protect the thesis.
- [ ] Dates, versions and breaking changes were checked recently enough for the topic.

### Pass C — Engineering reasoning (major)

- [ ] Opening establishes a concrete engineering question and a real reason to care.
- [ ] Central thesis is visible and the article actually supports or honestly qualifies it.
- [ ] Breadth supplies useful context and genuine alternatives without digressing.
- [ ] Depth explains the important internals, not just component names and benefits.
- [ ] Height connects technical observations to practical decision conditions.
- [ ] Each section advances the argument; transitions have causal logic.
- [ ] Recommendations identify applicable workloads, failure modes and when not to use the technique.
- [ ] The ending yields a conclusion not already exhausted in the introduction.

### Pass D — Diagram and example quality (major)

- [ ] Figures exist because they answer reader questions; unnecessary figures removed.
- [ ] Diagrams appear at the point they help explanation, often before complex implementation detail.
- [ ] Figures do not mislead on sequencing, data flow, ownership, security boundaries, measurement or scale.
- [ ] Captions give interpretive conclusions; alt text conveys relationships.
- [ ] Content remains readable on mobile; figures do not require zoom to decode every label.
- [ ] All visual/illustration rights and citations are handled.

### Pass E — Voice and Medium publishing (minor unless misleading)

- [ ] No generic scene-setting or hyperbole substitutes for engineering content.
- [ ] Each substantial paragraph contributes definition, mechanism, evidence, qualification or inference.
- [ ] No redundant introduction, transition, summary and conclusion loops.
- [ ] Headings reflect specific questions or concepts rather than a canned SEO outline.
- [ ] Quotes, links, boldface, code blocks and images are readable and restrained.
- [ ] Title promises exactly what the body delivers; subtitle adds an angle.
- [ ] No internal data or sensitive material is exposed without authorization.

## Review findings format — mandatory for changes

| ID | Severity | Location | ABC: actual text/problem | XYZ: exact replacement/action | Reason and evidence | Impacted figures/claims |
|---|---|---|---|---|---|---|
| R01 | ... | ... | ... | ... | ... | ... |

For a diagram defect, provide: incorrect component/arrow → exact correct graph/source → why. For a code defect, provide complete corrected code **where needed**, clearly distinguishing a teaching excerpt from a required repository change.

## Qualitative assessment (optional; never overrides blockers)

Rate each dimension as `STRONG`, `ADEQUATE`, or `WEAK`, with concrete evidence: novelty, breadth, depth, height, narrative, technical accuracy, sourcing, diagram quality, editorial craft. Do not manufacture percentage confidence; explain why a conclusion is justified and what remains unresolved.

## Acceptance record

- Article ID / version:
- Reviewer / date:
- Source snapshot date:
- Blocking issues open: ___
- Major issues open: ___
- Material changes since last approval: ___
- Figure/source reconciliation complete: `YES / NO`
- Final verdict: `BLOCK | REVISE | READY WITH DISCLOSED LIMITATIONS | READY`
- Rationale (specific, not congratulatory): ___

**Re-review rule:** An edit that changes a claim may also invalidate the opening, examples, diagrams, abstract, or conclusion. Reconcile all dependent material after every major technical revision.
