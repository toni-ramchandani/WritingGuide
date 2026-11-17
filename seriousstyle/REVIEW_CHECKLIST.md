# SeriousStyle review and release gates

Check the **complete latest document** against the **actual source materials**. A plain sentence can still be materially wrong. Do the technical checks before changing punctuation.

## Severity

| Level | Meaning | Release action |
| --- | --- | --- |
| **BLOCKER** | Invented evidence, changed technical meaning, missing material permission or limit, false outcome claim, incorrect actor or causal mechanism | Stop. Repair the claim and all dependent text or diagrams. |
| **MAJOR** | Missing decision, failure case, alternative, or reader context; ambiguous ownership; badly ordered explanation | Revise the affected sections and review again. |
| **MINOR** | Empty emphasis, ambiguous non-critical pronoun, decorative formatting, excessive jargon, clumsy heading | Copyedit without changing the technical contract. |

## Pass 1: Evidence and semantic integrity

- [ ] Every consequential statement has a source, observed artifact, or marked inference.
- [ ] Measurements retain their units, baselines, sample scopes, time windows, and uncertainty.
- [ ] Source statements retain modal verbs and negations, such as "may," "must," "only," and "not."
- [ ] Documented behavior, experimental status, local simulation, executed test, and independent outcome have not been conflated.
- [ ] No imagined first-person deployment, production metrics, unobserved tests, or invented owners.
- [ ] A strong counterexample or constraint that changes the conclusion is not omitted.

## Pass 2: Reader's decision and ownership

- [ ] The first paragraph states the outcome, recommendation, status, or reader question.
- [ ] A reader without prior project history knows enough context to understand the result.
- [ ] Every recommendation names an actor or an accountable component.
- [ ] Action, output, and verified consequence are distinguished.
- [ ] Risks, alternatives, non-goals, and next decisions appear when they change what the reader should do.
- [ ] Technical steps follow real causal or temporal order.

## Pass 3: Plain and serious prose

- [ ] Words express a real action or finding, not generic praise.
- [ ] Established technical terms remain stable and are explained when necessary.
- [ ] Subject and verb are explicit wherever a passive construction conceals responsibility.
- [ ] Pronouns have clear antecedents; do not ban every "this" or "it" mechanically.
- [ ] Paragraphs focus on one main claim with its necessary explanation.
- [ ] Lists and tables help the reader scan rather than replace necessary reasoning.
- [ ] No stacked slogans, repetitive rhetorical questions, artificial suspense, or gratuitous analogies.
- [ ] Sentence case and restrained emphasis are used; punctuation suits the medium and exact technical notation.

## Pass 4: Semantic diff

For each substantive change, compare the source wording with the revision. Preserve the following invariants:

| Invariant | Check |
| --- | --- |
| **Actor and action** | Who did what is unchanged, or corrected with evidence. |
| **Conditions and scope** | Preconditions, browser or SDK versions, tenant, role, environment, and sequence remain accurate. |
| **Quantities** | Values, units, baselines, denominators, and dates remain accurate. |
| **Polarity** | Negations and exceptions remain present. |
| **Epistemic status** | "Tested," "reported," "documented," "inferred," and "illustrative" retain their meaning. |
| **Risk and failure** | A critical limitation has not been removed for brevity. |
| **Decision** | Recommendation, owner, timing, and unresolved issues still match the evidence. |

If a statement becomes unsupported after revision, restore the caveat, narrow the assertion, or flag it. Do not publish a smoother false claim.

## Pass 5: Genre-specific acceptance

**Decision memo:** Decision, alternatives, key trade-off, evidence, owner and reversal condition are explicit.

**Architecture/design:** Mechanism, boundaries, state, failures, rollout and non-goals agree with the diagram and source.

**Incident:** Impact and timeline are grounded; trigger, root cause and contributing factors are distinguished; fixes have verification.

**Status update:** Current state, change, risk, next action and known owner are explicit.

**Technical explainer:** Core question is answered, mechanism traced, sourced, and limited to supported conditions.

## Reviewer record

- Document ID and version:
- Reader and requested action:
- Source snapshot and anchors:
- BLOCKER / MAJOR / MINOR findings:
- Semantic changes requiring source verification:
- Completeness check:
- Decision: **BLOCK / REVISE / READY WITH DISCLOSED LIMITATIONS / READY**

Report each material finding using **Actual text or defect -> corrected statement/action -> reason and evidence -> affected passages**. Style compliance never overrides a truth blocker.
