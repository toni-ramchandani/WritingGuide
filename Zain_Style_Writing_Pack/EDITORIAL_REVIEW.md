# Zain Style — adversarial review and release gates

Apply to **the latest complete article and its exact linked assets**, never just an earlier draft or review notes. This complements the [technical review gates](../Technical_Article_Editorial_Kit_v1_0/06_EDITORIAL_REVIEW.md).

## Blocker policy

**BLOCKER:** Materially incorrect API/architecture; invented experiment, metric, production observation or code execution; misleading trust boundary; technical conclusion unsupported by primary evidence; a title promising verified implementation that has no reproducible evidence; material copyright misuse.

**MAJOR:** Article lacks the causal story's middle; opens strong but becomes a reference manual; no traced example when the mechanism requires it; missing alternative/negative case; unearned conclusion; malformed or misleading figure; deliberate artificial shortening that removes the central explanation.

**MINOR:** Redundant transition, filler phrase, unnatural rhetorical question, overly dense paragraph, poor mobile label, title or keyword polish.

## Pass A — Truth and source scope

- [ ] All central terminology and mechanism claims checked against the actual latest relevant spec, paper, repo or implementation.
- [ ] Proposed, experimental, recommended, implemented and standardized features are distinguished.
- [ ] Local execution vs simulation vs source inspection vs published third-party result are clearly differentiated.
- [ ] Counterevidence and meaningful unknowns appear beside the claims they qualify.
- [ ] No invented lived experience, benchmark, production run or code output.
- [ ] The article fulfills what its title and subtitle promise.

## Pass B — Story completeness

- [ ] Opening contains actual friction and a question a capable reader cares about.
- [ ] There is a real development from earlier approach to new design, not just multiple definitions.
- [ ] The middle follows actors, interfaces, parameters, state, control flow and errors in causally connected prose.
- [ ] A running example traces input -> execution -> validation/state -> output -> failure -> limitation.
- [ ] At least one technically meaningful counterexample or failure condition is understood.
- [ ] A serious alternative is treated fairly and choice conditions are explicit.
- [ ] The ending provides a new judgment instead of repeating the introduction.
- [ ] No section exists only to add SEO keywords or restate prior claims.
- [ ] Length follows the promised scope. An 8–10 minute feature is not reduced to 1,100 words merely for minimalism.

## Pass C — Visual and practical honesty

- [ ] At least one finished, accurate diagram is used unless a documented exception makes another artifact clearer.
- [ ] Each diagram answers a reader question, uses labeled causal arrows and has readable mobile labels and alt text.
- [ ] Every code example explains a decision; required surrounding names, dependencies and API caveats are supplied.
- [ ] The real execution path is matched against the code, and test claims have receipts.
- [ ] A mocked registry does not imply browser-native tool discovery; a tiny fixture does not imply full framework validation.
- [ ] When demonstrating an agent capability, distinguish application outcome from the agent's narrative of success.
- [ ] Practical appendices contain actual reusable files when the title promises a build.

## Pass D — Editorial sharpness

- [ ] No generic "AI is changing the world" opening, exaggerated adjectives, staged dialogue, or clickbait certainty.
- [ ] Narrative paragraphs flow without artificial paragraph-per-sentence formatting or lists replacing engineering explanation.
- [ ] Define jargon as needed, rather than creating a glossary before the story begins.
- [ ] Each diagram and paragraph advances the argument, not merely decorates it.
- [ ] Duplicates are removed **without** deleting unique mechanism, evidence, or decision context.
- [ ] First-person phrasing accurately reflects what the author actually did.

## Pass E — SEO/AEO/GEO and publication

- [ ] Title identifies subject and true technical promise; subtitle adds a real angle.
- [ ] The opening defines the central entity once, accurately and with required qualifications.
- [ ] H2s reflect substantive reader questions, not keyword variants.
- [ ] Relevant primary sources are linked where technical claims appear.
- [ ] Description, tags, slug and social teaser live outside the manuscript.
- [ ] No promises of search ranking or AI answer-engine citations.
- [ ] Source date, code version and experimental support revalidated before publishing.

## Mandatory change record

| Finding | Severity | ABC: exact source text / actual defect | XYZ: full corrected wording, figure, or action | Reason and source | Dependent sections/files |
| --- | --- | --- | --- | --- | --- |
| Z01 | | | | | |

A defect fix is not complete until the corrected claim, diagram, code example, and dependent paragraphs agree.

## Final verdict

- Manuscript ID/version:
- Source snapshot:
- Author's approved thesis and narrative type:
- Primary technical sources checked:
- Practical execution scope and evidence:
- Unresolved blockers:
- Unresolved major defects:
- Duplicate/shortening audit:
- Visual asset/accessibility audit:
- Publication metadata audit:
- Verdict: **BLOCK / REVISE / READY WITH DISCLOSED LIMITATIONS / READY**.
