# Editorial Standard — Engineering Articles v1.0

**Applies to:** Technical articles on AI, software engineering, systems, protocols, security, data, platforms, infrastructure, architecture and research. Intended default readership: experienced technical practitioners; adjust terminology and depth to the stated audience.

## 1. Publication contract

Our article should do at least one of the following exceptionally well:

- Make a mechanism intelligible that existing summaries obscure.
- Test or challenge an attractive but incomplete engineering assumption.
- Expose a consequential architectural trade-off with evidence.
- Turn a real implementation or experiment into transferable lessons.
- Synthesize conflicting primary sources into a more useful decision model.

**Not sufficient:** an exhaustive list of definitions, a collection of vendor features, a parade of diagrams without analysis, or a polished restatement of introductory documentation.

**Reader transformation:** Write one sentence describing what readers can explain, diagnose or decide after reading that they could not before. If that sentence is weak, the article is not framed yet.

## 2. Three-dimensional technical coverage

### Breadth = necessary context

Show the competing approaches, relevant history, architectural surroundings and boundary conditions **needed to interpret the central argument**. Breadth is *selectivity*, not number of topics. Ask: which alternative would a skilled reader reasonably consider? What adjacent system changes the recommendation?

### Depth = mechanism and causality

Explain how key components, algorithms, decisions and failure paths work. Prefer a causal chain: *condition → internal behavior → observed outcome → design consequence*. Use pseudocode, request traces, small calculations and system diagrams when they clarify. Avoid code without a teaching purpose.

### Height = consequence and judgment

Derive when the method is useful, where it fails, the cost of using it, and how a team might choose among alternatives. State assumptions on workload, scale, trust boundary, cost, latency, operating environment or versions as appropriate. Height is not executive buzzword abstraction.

**Balance test:** Can the reader locate context, inspect the mechanism, and defend a decision? If any answer is no, the article is incomplete.

## 3. Argument spine (conceptual, not mandatory headings)

1. **Problem:** A concrete difficulty, confusion, surprising observation or engineering need.
2. **Tension:** Why the familiar or obvious approach is insufficient under particular conditions.
3. **Mechanism:** The system or technique, explained with its necessary internal detail.
4. **Evidence:** Reproducible example, primary source, experiment, source code, trace, or qualified observation.
5. **Trade-off:** What it improves, what it costs, what remains unsolved; compare with a viable alternative.
6. **Judgment:** Applicability boundary, diagnostic question, migration path or decision criterion.

Sections need not appear in this exact order. They must have a reason to exist and create a reason to read the next one.

## 4. Choose one dominant article archetype

| Archetype | When appropriate | Natural progression | Common failure |
|---|---|---|---|
| Mechanism explainer | Understanding an unfamiliar algorithm, system or technique | Misconception → mental model → internal mechanics → worked example → implications | Definitions with little causal insight |
| Engineering investigation | We have design iterations, implementation experience, measured or observed behavior | Failure/constraint → hypothesis → alternatives → build/test → observations → limitations | Retrofitting a success story and hiding failed trials |
| Research synthesis | Sources disagree, newer evidence changes existing assumptions | Question → literature → comparison of methods → agreement/disagreement → implications | Mistaking paper abstracts for validated facts |
| Architecture decision | Teams need to choose between approaches | Requirements → alternatives → decisive trade-offs → failure modes → choice conditions | Announcing a recommendation before stating constraints |

For some subjects, hybridization is appropriate. Explicitly identify the *dominant* approach to prevent meandering.

## 5. Research, uncertainty and claim ethics

**Evidence hierarchy is context-dependent.** Specifications govern protocol semantics; implementation source governs a specific release; papers support their measured findings and stated assumptions; public engineering blogs report authors' experiences; production results require actual operational evidence. No single type of source is universally superior.

For consequential claims, track:
- What exactly is being claimed? Is it a definition, fact, first-hand observation, reported observation, hypothesis or interpretation?
- Which primary source supports it? Which section or code line? When and for which version?
- What was measured, on what population/sample, with which baseline and controls?
- What contradictory evidence or boundary case exists?
- What is **not** known?

Do **not** invent tests, log output, quotations, usage numbers, datasets, citations or first-person deployment experience. If a synthetic numerical example is useful, label it *illustrative* and show the assumptions. If discussing reported vendor metrics, attribute the owner and setup. Do not turn a single anecdote into a general law.

Keep published dates and version anchors where currency matters. Before final publication, revisit stale claims and URLs. A current API description cannot be assumed valid for an older SDK/version.

## 6. Explanatory paragraphs that earn their space

Prefer this reasoning structure, used flexibly rather than formulaically:

**Claim or observation → mechanism → concrete evidence/example → implication or limitation.**

Weak: “Retries increase resilience. Teams should use exponential backoff.”

Stronger illustrative paragraph: “Retries are useful when a dependency's failure is transient, but they become extra workload when the dependency is saturated. If clients retry immediately, a small failure rate can amplify incoming traffic precisely when the service has less spare capacity. Backoff with jitter spreads attempts over time; retry limits bound additional work. Neither technique by itself makes a non-idempotent operation safe to repeat.”

Do not force four sentences into every paragraph; vary rhythm. Paragraphs should connect, not become isolated slogan lines.

## 7. Visual reasoning policy

Begin visual planning before drafting the mechanism-heavy prose. Only include a figure when it addresses a genuine reader question better than text alone.

Each visual must specify:
- **Question:** what confusion is this figure resolving?
- **Kind:** conceptual model, comparison, architecture, sequence, data flow, failure path, experiment/chart, or decision boundary.
- **Correctness:** nodes, arrows, ordering, boundaries, invariants and exclusions all checked.
- **Source:** original or adapted, with attribution and permission/license requirements checked.
- **Caption:** conclusion or interpretive lens, not “This figure shows the architecture.”
- **Accessibility:** legible at narrow Medium widths; clear labels, alt text, no color-only meaning.

**Do not assert:** a model is actual implementation code when it is merely conceptual; a simulated result is production telemetry; a re-created figure is sourced from a paper without attribution.

## 8. Voice and editorial craft

The tone should be technically confident but calibrated. Prefer concrete verbs, precise nouns and clear transitions. Use first person for genuine author choices or firsthand work only. Use terms of art where they improve accuracy; explain unfamiliar terms at their first consequential appearance.

Avoid:
- Generic opening (“In today's rapidly evolving world…”).
- Empty adjectives (“revolutionary,” “game-changing,” “cutting-edge”) without measurable support.
- Invented authority (“we observed in production”) unless supplied by the author.
- Fake tension, e.g. framing mundane configuration as a dramatic breakthrough.
- Repeated explanations restated in the introduction, each section and conclusion.
- Mechanical sequencing (“Let's dive in”, “It's important to note”, “Here are 10 benefits”).
- Overloaded diagrams, reference dump paragraphs, excessive one-line paragraphs.
- Promotional certainty that exceeds the experiment, source or architecture constraints.

Originality comes from framing, independent synthesis and accountable interpretation—not merely novel adjectives.

## 9. A strong beginning, middle and ending

**Opening (usually 2–5 paragraphs):** establish the problem, stakes, a non-obvious tension and the reader's destination. An anecdote is optional; a precise problem is essential. A striking number requires an attributable source.

**Middle:** deliver the core mechanism, evidence and critical alternatives. Use examples and visualizations near the exact claims they support. Maintain logical handoffs: *why this section matters* should be apparent.

**Ending:** synthesize a decision model, transferable lesson, or unresolved question. Do not merely repeat headings or add a generic call to action.

## 10. Code and worked examples

Code is optional and earns its presence by explaining important control flow, data structure, invariants or failure cases. Prefer the smallest excerpt that proves the point. For runnable examples, document environment and version, distinguish tested from illustrative, and keep code in an accessible repository or appendix if lengthy. Never claim a sample was executed unless verified.

For equations: state variables, assumptions and interpretation. A mathematically true formula can still mislead if it uses unrealistic independence assumptions.

## 11. Medium publishing layer

Optimize for thoughtful reading and mobile display: descriptive headings, restrained boldface, informative figure captions and integrated source links. Set length based on the argument and its audience, not an artificial minutes-read target. Create a defensible title first, then refine for search intent without exaggeration. Use a short subtitle to state the distinct insight, not to repeat the title.

Before publication, check image rights, alt text, diagram widths, hyperlinks, code formatting, citations, authorial attribution, and changes in version-specific claims.

## 12. Non-negotiable publication blockers

1. Materially false mechanism or misleading diagram.
2. Fabricated metric, experiment, citation, quotation or author experience.
3. Core conclusion unsupported by the available evidence.
4. Critical alternative or material counterexample omitted in a way that reverses the recommendation.
5. Reproduced third-party text or figures without appropriate attribution and rights.
6. Sensitive/private/internal information published without authorization.

**Editorial release principle:** Style and readability do not offset any blocker. Fix the earliest broken stage, update dependent artifacts and review again.
