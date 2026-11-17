# Source audit, adaptation decisions, and evaluation plan

## Primary source and license

**Reviewed source:** [docwriter-org/plain-writing-skill](https://github.com/docwriter-org/plain-writing-skill), especially [skills/plain-writing/SKILL.md](https://github.com/docwriter-org/plain-writing-skill/blob/main/skills/plain-writing/SKILL.md), [evals/README.md](https://github.com/docwriter-org/plain-writing-skill/blob/main/evals/README.md), and [LICENSE](https://github.com/docwriter-org/plain-writing-skill/blob/main/LICENSE).

Source snapshot: **17 November 2026**. The repository's MIT license lists **Copyright (c) 2026 Shreya Shankar**. The MIT notice is preserved in [THIRD_PARTY_LICENSE.md](THIRD_PARTY_LICENSE.md). SeriousStyle is a distinct, original guide; it is not an upstream release or a verified extension of the original skill.

## Critical rule audit

The original skill has 25 numbered rules. Its central idea is deliberate plainness. SeriousStyle adopts the parts that make professional documents easier to act upon, while avoiding rigid rules that can damage engineering meaning.

| Upstream rules | Assessment | SeriousStyle policy |
| --- | --- | --- |
| 1–4: simple words, established terms, no puffery, consistent terminology | High value; works in technical writing with precision exceptions | **Adopt**, preserve technical terms |
| 5–7: contractions, invented compounds, intentionally boring voice | Useful tone control, but no universal style | **Adapt** to restrained, matter-of-fact tone; contractions optional |
| 8–10: complete sentences, sequence, supporting paragraphs | High value for technical and operational instructions | **Adopt** with natural flow and appropriate genre structure |
| 11–12: strict clause limit alongside preference for longer explanatory sentences | These prescriptions conflict in some contexts and do not measure correctness | **Reject hard limits**; split at change of actor or responsibility |
| 13–14: specificity, contextual continuity in chat | Strong for status, reviews, and handoffs | **Adopt**, including context for readers without chat history |
| 15–18: no dashes/colon joins, straight quotes, minimal formatting | Avoid decorative punctuation; rigid bans may damage standard notation or publisher requirements | **Adapt**, not universal syntax prohibitions |
| 19: few lists | Valuable for sustained prose; some operational docs need checklists | **Adapt** to document purpose |
| 20: avoid false agency | High value when responsibility, authorization, or causal claims are unclear | **Adopt** |
| 21: no analogies or imagery | Appropriate default for formal reports, not an absolute rule for explanation | **Adapt**: avoid by default; allow concise necessary analogy |
| 22–23: avoid canned negative parallelism and repeated rhetorical questions | Strong anti-filler guidance | **Adopt as preference**, not text-pattern bans |
| 24: ban vague demonstrative pronouns and entire paragraph openings | Ambiguity is the real problem, not a particular word | **Reject absolute ban**; fix unclear referents only |
| 25: avoid count-based openings | A list of counts can be informative in operational summaries | **Adapt**; lead with finding or decision, use counts when meaningful |

The policy intentionally does **not** copy the 25 rules as a second checklist. Instead it organizes the reader's task, truth conditions, actor clarity, decision responsibility, and a semantic-preservation review.

## What the upstream evaluation proves and does not prove

The upstream evaluation README reports **65 skill wins out of 67 tasks (approximately 97%)** in a comparison against an unskilled baseline, with **705 skill rule wins, 232 baseline rule wins, and 738 ties**. The evaluation uses the skill's own rules as the judging criteria and reports **gpt-5.5 as both the writer and the judge model**. These are results **reported by the repository**, not reproduced here.

The tests support a narrower claim: when judged using its authored rules, the upstream skill's outputs tended to follow those rules more often than the comparison outputs. They do **not** independently establish:
- semantic or factual correctness;
- completeness of a technical document after rewriting;
- human preference among technical readers;
- faster engineering decisions or reduced misunderstanding;
- a quality advantage over the Zain or Zen guides.

The upstream judge description explicitly prioritizes a particular writing rule even when a version drops important task content, except when both break the rule equally. That is appropriate for *rule adherence*, but not an adequate method for our **factual preservation** gate. SeriousStyle therefore uses the master playbook's blockers and the [semantic diff checklist](REVIEW_CHECKLIST.md) before stylistic preferences.

## Proposed SeriousStyle evaluation (not yet run)

Compare SeriousStyle drafts against a **neutral clarity baseline** using identical sources and instructions. Keep the model, temperature/options, context length, and allowed evidence consistent. Randomize which candidate the reviewer reads first.

Use a small, varied set of **six source-backed scenarios**, for example:
1. an incident report containing timestamps, cause uncertainty, and open actions;
2. a security architecture memo with authorization boundaries;
3. a product or technical status update with one unresolved dependency;
4. a protocol explainer requiring version and experimental-status qualifiers;
5. a decision record with two plausible alternatives;
6. a long research summary with reported results and contradictory evidence.

Have a knowledgeable reviewer grade **truth first**. A fabricated or materially altered claim fails regardless of prose. For passing candidates, judge completeness, clarity, responsibility, and reader actionability against a fixed rubric. Do not ask a judge to count words, punctuation, or banned phrases as a proxy for correctness.

Suggested rubric, as an **untested proposal**: factual preservation (pass/fail gate), then completeness 30%, clarity 30%, responsibility/actionability 25%, and appropriate tone 15%. Record concrete reviewer comments and disagreements, not a meaningless aggregate number alone. If possible, ask a target reader to answer a short comprehension question before seeing the sources.

**Status:** No comparison against SeriousStyle has been executed. The guide has been source-reviewed and checked for structure and source attribution, not empirically validated.
