# SeriousStyle: plain, exact, evidence-bound writing

**Version:** 1.0  
**Purpose:** A standalone writing guide for engineers, technical leaders, and decision-makers. It is designed for documents that readers must act on, review, audit, or hand to another person.

SeriousStyle is **not** the repository's [Zain Style](../Zain_Style_Writing_Pack/README.md) and is **not** the [Zen Style](../Zen_Style_Writing_Pack/README.md). It adapts selected lessons from [Plain Writing Skill](https://github.com/docwriter-org/plain-writing-skill) to technically accountable professional communication. The [master playbook](../TECHNICAL_ARTICLE_MASTER_PLAYBOOK_v1_0.md) takes precedence on factual accuracy and evidence.

## 1. The writing contract

An unfamiliar, capable reader should learn **what happened or is proposed, why, the evidence, the limits, and who acts next** without decoding slogans or guessing implicit context.

The first paragraph should deliver the document's main conclusion or required decision. Give the minimum background needed to interpret it. Then present the mechanism or evidence, consequences, and next action in an order the reader can follow.

**SeriousStyle is not synonymous with short.** A complex design review can be long. Length is justified when it resolves a question, explains a mechanism, presents evidence, names a risk, or records a decision.

**It is not a substitute for research.** Clean prose cannot compensate for an invented test, an incorrect API interpretation, or a missing security condition.

## 2. State the point before the background

Use the actual document type to decide what belongs first:

- A **decision memo** begins with the proposed decision, the reason, and the unresolved condition.
- A **status update** begins with the observed state, what changed, and whether the next milestone is at risk.
- An **incident report** begins with the impact, time window, and current resolution status.
- A **technical explanation** begins with the answer to the reader's real question, followed by the mechanism and a relevant limit.

Do not open with generic history, dramatic suspense, five rhetorical questions, or "In today's rapidly evolving landscape." Do not use a headline that promises certainty beyond the source material.

For a sequence, describe events in execution order. Make causal dependencies explicit. **Chronological order** is appropriate for incident timelines; **decision-first order** is usually better for executive summaries.

## 3. Prefer words that carry information

Use familiar words when they express the same technical meaning.

- Prefer "use" to "leverage," "show" to "surface," "change" to "transform," and "because" to vague narrative transitions.
- Avoid unsupported adjectives such as "seamless," "robust," "revolutionary," "world-class," and "production-ready."
- Keep established terms such as *idempotency*, *p95 latency*, *JSON Schema*, or *MCP* when a simpler replacement would be wrong. Define unfamiliar terms when needed.
- Call one concept by one name. Do not alternate between "job," "pipeline," "process," and "workflow" just to avoid repeating a noun.
- Use the same name for a component in the prose, diagram, table, and code example.

Punctuation is an aid to meaning, not a target metric. Default to complete sentences, sentence-case headings, restrained bold, few lists, and normal ASCII punctuation where a publication permits it. Avoid decorative em dashes, artificial colon-driven suspense, invented compound adjectives, and acronym-heavy headings. Do **not** ban necessary hyphens, code identifiers, ranges, or conventional technical notation.

## 4. Make every technical claim inspectable

Ask four questions of each consequential sentence:

1. **Actor:** Who or what performs the operation, owns the decision, or observes the result?
2. **Action and object:** What is called, validated, written, selected, rejected, or changed?
3. **Conditions:** Under which version, scope, permission, time window, input, or environment does the claim hold?
4. **Evidence and effect:** What source or observed result supports it, and what does it actually establish?

Prefer "The service rejected a request missing `tenant_id`" over "The platform handled tenant security." Prefer "The test returned HTTP 403 for an unauthorized role" over "Authorization is secure." A specific observation is narrower and more useful than an unjustified assurance.

Do not personify software needlessly. "The database decides which user can see a record" obscures the authorization mechanism when a policy engine or a query predicate actually performs that check. Ordinary phrases such as "The API returns JSON" are accurate and acceptable.

An observation is not necessarily a cause. "Latency increased after deployment" is not proof "the deployment caused latency to increase." Record the investigation or qualification required to support causation.

## 5. Preserve scope, uncertainty, and the source of truth

Distinguish:

- **Confirmed from execution:** Exact environment, action, and observed output or failure.
- **Documented:** Normative specification or versioned vendor documentation, without claiming it was executed.
- **Reported by another party:** Their benchmark, production account, or measurement with baseline and scope.
- **Inferred:** A conclusion drawn from facts, with its assumptions.
- **Illustrative:** Hypothetical numbers, traces, or scenarios, labeled as such.

Never silently change one into another. Protect negations and quantifiers: "may," "can," "in one experiment," "up to," "only on localhost," "under 100 ms," and "not independently verified" are part of a technical claim. Keep the units, denominator, baseline, version and comparison conditions.

A rewrite must not turn "the mocked callback returned success" into "the browser agent successfully completed the task." Nor may it convert "the vendor reports 18% lower latency" into "latency is 18% lower" without attribution.

When facts are unavailable, identify the gap. Do not fill it with fluent prose.

## 6. Write paragraphs that explain, not perform

A useful paragraph normally has one main claim, followed by the reason, evidence or example that makes it credible. It may end with a practical implication. Paragraphs can contain varied sentence lengths; prefer smooth explanatory prose over stacked fragments and slogan-like one-liners.

When a sentence mixes multiple actors, split it at the change of responsibility:

**Before (illustrative):** "The agent finds the tools, sends the request, verifies the output, and authorizes the transfer."

**After (illustrative):** "The browser exposes registered tools to a compatible agent, and the agent selects an operation. The page executes the callback. The backend then checks whether the user is authorized to transfer funds. A separate outcome check determines whether the transfer succeeded."

The revision is longer because the original falsely concentrated independent responsibilities in one actor. Clarity is not always brevity.

Do not use a chain of rhetorical questions to substitute for analysis. Avoid "not just X, but Y" constructions when a direct definition would do. Remove repeated introductions, recaps, and closing slogans.

## 7. Structure for the document's job

### Decision memo or architecture decision record

Start with **Decision / recommendation** and the relevant scope. Then record the context, requirements, alternatives, decisive evidence, trade-offs, operating risks, and decision owner. Include what could reverse the choice. A table is appropriate when alternatives are compared on identical criteria. Do not bury the decision behind a history lesson.

### Technical design or RFC

State the problem and non-goals. Describe the current system only as needed. Explain the proposed components, interfaces, state transitions, invariants, failure handling, security boundaries, rollout, rollback, metrics, and unresolved decisions. Diagrams must show true ownership and arrow semantics. Include code only when it explains a consequential interface or control path.

### Incident report

Begin with impact, affected users or systems, start and end times, and current state. Present a grounded timeline. Separate **trigger**, **root cause**, and **contributing conditions**. Record evidence and uncertainty; do not assign blame without support. End with corrective actions, owners, deadlines, and verification of the fix. Do not claim an incident resolved merely because an alert cleared.

### Status, review, or executive update

Lead with whether the objective is achieved, at risk, or blocked. State the most important evidence, what changed since the last report, the risk, the next step, and its owner/date when known. Avoid ceremonial phrases and summaries that omit the decision needed.

### Technical research or explanation

Answer the reader's question first. Explain the system's mechanism using a representative trace and relevant primary source. Distinguish the documented behavior from measurements or inference. Finish with the applicability limit. SeriousStyle does not require a new implementation when an authoritative reference demonstrates the mechanism adequately.

## 8. Editing algorithm: protect the facts before polishing the words

Use the following order for significant rewrites:

**Step A: Lock the facts.** Extract the material claims and their source anchors. Record versions, quantities, negations, permissions, conditions, evidence type, and unresolved issues. For a memo, record every decision request and owner.

**Step B: Identify the reader's next decision.** Choose which claim must appear first. Do not assume the reader saw prior emails or conversations.

**Step C: Rewrite for structure.** Group each distinct idea once and arrange steps in causal or chronological order. Introduce necessary context immediately before use, not in a large generic preamble.

**Step D: Rewrite for plain meaning.** Name actors and operations, clarify references, standardize terminology, and remove filler. Preserve conditions and uncertainty. Use lists only when readers need to scan separate items.

**Step E: Diff the meaning.** Recheck the rewritten text against the locked facts and original sources. A deletion is safe only if it removes repetition, an unsupported claim, or material intentionally excluded from the stated scope. Do not remove a failure path just to make the document read faster.

**Step F: Review as an outsider.** Ask what the reader can confidently repeat, what they would need to verify, who acts next, and which conclusion would fail if the assumptions change.

The full [review checklist](REVIEW_CHECKLIST.md) is the release gate; its semantic diff takes priority over style preferences.

## 9. What SeriousStyle does not require

The upstream Plain Writing Skill prefers a consistently "boring" voice and imposes strict bans on imagery, dashes, various pronouns, and multi-clause sentences. SeriousStyle retains its **restrained intent**, but rejects unconditional syntactic bans that harm technical accuracy, document compatibility, or readable engineering prose.

For SeriousStyle, **avoid metaphor, analogy, clever slogans and decorative imagery by default**. Use a short analogy only when an actual reader needs it and its limitations are explicit. Keep necessary technical punctuation. Do not mechanically replace every "this" or "that" when the antecedent is clear.

An editor must never improve compliance with a stylistic checklist at the cost of factual completeness. If a particular publication mandates strict typography or controlled language, apply that as a separate publishing rule.

## 10. Publication and acceptance

For professional documents, success is **correct understanding and action**, not an SEO keyword count or a style score. Put clear subject names in titles and headings. Cite primary sources near important claims and use direct links rather than a long unannotated bibliography. For public technical writing, use truthful page descriptions and headings, but do not promise search rankings or citations by AI answer engines.

A release is blocked when the draft invents results, changes the source's conditions, attributes a decision to the wrong actor, omits a material risk, or represents a proposal as deployed behavior. Clumsy punctuation is a minor concern by comparison.

**Final reader test:** Could someone unfamiliar with the project explain the decision, supporting evidence, critical limit, and next responsibility accurately after one reading?
