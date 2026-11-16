# Zain-style technical article worksheet

Complete the information needed to write the article, not generic placeholders. This worksheet stays in the **editorial handoff**, not the reader-facing manuscript.

## A. Reader and thesis

- **Article ID / version / source snapshot date:**
- **Reader (prior knowledge, role, practical question):**
- **Article mode:** mechanism explainer / engineering investigation / research synthesis / architecture decision / reproducible tutorial.
- **Search intent (what a reader actually types):**
- **One-sentence thesis that can be challenged:**
- **What readers will be able to explain, reproduce or decide:**
- **Why this article is different from earlier pieces:** Include existing internal/external article links when relevant.
- **Scope boundaries and promises:** What does the title promise? Does it imply tested code or a production deployment?
- **Likely strongest counterargument or competing design:**

## B. Core technical story

Write 1–2 **complete sentences** for each section, not merely a list of headings:

| Stage | Reader's developing question | Technical content/evidence | Transition to next stage |
| --- | --- | --- | --- |
| Hook and friction | | | |
| Why the previous approach fails under these conditions | | | |
| Main mechanism, including actors and data flow | | | |
| Running example with real parameters and state | | | |
| Failure/negative case and trust boundary | | | |
| Alternative and trade-off | | | |
| Decision boundary and earned conclusion | | | |

This order is adaptable. Two rows are redundant when they make the same claim without adding a new cause, observation, or consequence. Merge them before drafting.

## C. Running example / practical path

- **Owned/authorized system or documented example:** 
- **Initial state and input:** 
- **Actors, operation and interfaces:** 
- **State change and expected output:** 
- **Negative or adversarial input:** 
- **Observed output and reproducibility evidence, if any:** 
- **Remaining unknowns and how to distinguish simulation from native integration:** 

If the article promises an implementation, verify:
- [ ] Environment and versions stated.
- [ ] Complete minimal artifact available (or all relevant code in the article).
- [ ] Exact run commands and expected output.
- [ ] Negative test and cleanup/lifecycle behavior.
- [ ] Evidence of execution actually obtained.
- [ ] External framework/browser/model claims not falsely implied by a mocked test.

## D. Source and claim map

| Consequential claim | Type: spec / documented / reported / tested / inferred / illustrative | Exact source + version/date | Limitation/counterexample | Status |
| --- | --- | --- | --- | --- |
| | | | | |

For empirical claims record who measured what, under which baseline and conditions. Sources are contextual: a spec supports normative interfaces, code supports a release's implementation, paper results support their measured domain, and a local test supports only its execution scope.

## E. Figure storyboard

| Reader's visual question | Placement | Diagram type | Essential nodes and arrow meaning | Caption and alt text | Source / final asset |
| --- | --- | --- | --- | --- | --- |
| | | | | | |

At least one finished explanatory figure is the default. For protocol pieces consider a **sequence** rather than a box collection; for stateful workflows consider a **state machine**; for authorization consider a **trust boundary**. Prefer 1–3 figures with distinct jobs to six decorative ones. Check at phone width.

## F. Publishable narrative and discovery

- **Title (specific subject + true promise):**
- **Subtitle (distinct mechanism/constraint, not repetition):**
- **Working slug:**
- **Page-specific description (roughly 140–165 characters where relevant):**
- **Medium tags (up to 5 relevant terms):**
- **AEO/GEO answering passage:** Where is the first accurate, concise answer to the primary reader question? Does it immediately carry a material qualification?
- **Intended read experience:** Often about 8–10 minutes, but driven by technical scope, not a word quota.
- **Reader-facing references:** Cite primary sources where the claims appear.
- **Planned diagrams and accessibility:** 
- **Editorial handoff / verification record path:**

## G. Release check

- [ ] The opening's question is actually resolved by the ending.
- [ ] The middle contains substantive internal mechanics and a traced representative case.
- [ ] Every section adds a distinct cause, constraint, mechanism, evidence, or consequence.
- [ ] No empty marketing adjectives, invented anecdotes, or theatrical suspense.
- [ ] A capable engineer could trace the critical operation from the text and figures.
- [ ] Alternatives, failure paths, permissions, and practical decision criteria appear where material.
- [ ] Every empirical or implementation claim is evidence-backed and correctly scoped.
- [ ] All figures, captions, alt text, links, and source rights are checked.
- [ ] SEO/AEO/GEO terms describe the article rather than drive its technical claims.
- [ ] Manuscript is separate from review notes, test logs, prompts, and marketing metadata.

Use [EDITORIAL_REVIEW.md](EDITORIAL_REVIEW.md) and the [master review gates](../Technical_Article_Editorial_Kit_v1_0/06_EDITORIAL_REVIEW.md) before declaring an article ready.
