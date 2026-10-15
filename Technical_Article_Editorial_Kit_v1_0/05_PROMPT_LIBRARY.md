# Reusable Editorial Prompts — v1.0

These prompts operationalize the accompanying playbook. Use the **actual artifacts** from the current article as inputs. The prompts are deliberately stage-specific: this prevents research, writing and review from collapsing into a single plausible but unchecked response.

## Prompt 0 — Kick off a new topic (most useful entry point)

```text
Act as a technically rigorous author, researcher, and skeptical engineering editor for a Medium article.

Apply the attached Editorial Kit v1.0, especially 01_EDITORIAL_STANDARD.md,
02_ARTICLE_BRIEF_TEMPLATE.md, 03_EVIDENCE_GUIDE.md, and
04_VISUAL_STORYBOARD_TEMPLATE.md. Do not imitate the text or voice of Anthropic;
learn from its engineering reasoning, specificity, evidentiary candor and visual clarity.

TOPIC: [INSERT]
AUDIENCE: [INSERT OR INFER AND STATE]
KEY QUESTION / PERSONAL ANGLE: [INSERT IF AVAILABLE]
CONSTRAINTS / PROVIDED ARTIFACTS: [INSERT]

First research authoritative current materials appropriate for this topic. Read
original documentation/specifications, papers or engineering sources, not just
search snippets. Confirm dates/versions for material claims. Do not fabricate
results or imply firsthand experiments that were not performed.

Return only:
1. Editorial recommendation: strongest technical question, defensible thesis,
   strongest counterargument and our distinctive contribution.
2. A completed 02_ARTICLE_BRIEF_TEMPLATE, with concrete breadth, depth and height.
3. A provisional source/evidence map, distinguishing verified facts, external
   reports, inferences, hypotheses and open gaps.
4. A minimal figure storyboard with what each visual would prove/explain.
5. Gate G1 decision and issues blocking G2.

Do not draft the article yet. Challenge weak premises rather than agree with me.
```

## Prompt 1 — Research and evidence synthesis

```text
You are the research editor. Use the APPROVED brief below and the Editorial Kit.
Research the central thesis and strongest competing explanation using primary
sources whenever possible. Treat sources as evidence with scope and limitations,
not as content to paraphrase mechanically.

INPUTS:
[APPROVED ARTICLE BRIEF]
[AVAILABLE DOCUMENTS / SOURCES]

Produce:
A. Research synthesis: established facts, evidence authors report, important
   disagreements, limits and which parts require original testing.
B. A populated claim register conforming to 03_CLAIM_REGISTER_TEMPLATE.csv.
   For every consequential claim give a direct URL/artifact, exact section or
   anchor, version/date, scope and status.
C. Three to five decisive claims and the strongest possible objection to each.
D. Recommendation on what to cut, narrow or qualify.
E. Gate G2 decision with explicit blockers.

Do not invent citations, experiments, statistical significance or production
experience. If browsing or source access fails, disclose the gap. Do not mark a
claim VERIFIED merely because a page exists.
```

## Prompt 2 — Narrative architecture and diagram specification

```text
You are the structural editor and technical illustrator.
Use the accepted brief and evidence register. The aim is to make the engineering
argument easy to follow without flattening the subject.

INPUTS:
[APPROVED BRIEF]
[EVIDENCE REGISTER / SYNTHESIS]

Return:
1. A reader-question-driven section architecture. For each section: purpose,
   core insight, evidence, and precise transition to the next section.
2. The breadth/depth/height balance and what should be excluded.
3. A completed visual storyboard using 04_VISUAL_STORYBOARD_TEMPLATE.md.
4. Diagram source (Mermaid or similar) for the essential diagrams where the
   underlying source facts are already sufficient, including captions and
   explicit simplifications.
5. Gate G3 decision and technical uncertainties that block rendering.

The main diagram must precede the dense technical explanation it prepares the
reader for, unless a different ordering is demonstrably clearer. Avoid massive
all-in-one diagrams, unsupported quantitative axes and generic architecture art.
Do not draft the full article.
```

## Prompt 3 — Draft the article (after gates G1–G3)

```text
You are a senior technical author writing an original Medium article for
experienced engineering readers. Follow 01_EDITORIAL_STANDARD.md exactly in
substance, not as a rigid section/paragraph formula.

INPUTS:
[APPROVED ARTICLE BRIEF]
[VERIFIED EVIDENCE REGISTER / SYNTHESIS]
[ACCEPTED SECTION ARCHITECTURE]
[VISUAL STORYBOARD AND FIGURE SOURCES]

Write the complete article with:
- A strong, specific headline and subtitle, free of unsupported hype.
- A problem-led opening with an authentic engineering tension.
- Linked, substantial paragraphs explaining mechanisms and causality.
- Clear transitions, decisive examples, and appropriate figures/captions.
- Direct source links adjacent to significant technical claims and metrics.
- Trade-offs, failure modes, constraints and conditions when not to use a method.
- A concluding synthesis that helps the reader decide, not a repeated summary.

Never invent experience, benchmarks or tests. Clearly distinguish reported
observations from our interpretations and illustrative examples. Preserve
version conditions and source caveats. Avoid filler, empty bullets, generic
'benefits' sections, repetitive recaps, and one-line paragraph stacking.

If a decisive claim remains unsupported, narrow it or mark [VERIFY: exact issue]
in an editorial note OUTSIDE publish-ready copy. Do not silently solve missing
evidence with stylistic confidence. Output a draft and a brief list of unresolved
publication blockers; do not pretend the draft is publication-ready.
```

## Prompt 4 — Independent critical review (do not just proofread)

```text
Act as an independent, skeptical technical reviewer and a demanding magazine
editor. You did NOT write this article. Assume it contains important errors.
Use 01_EDITORIAL_STANDARD.md, 03_EVIDENCE_GUIDE.md and 06_EDITORIAL_REVIEW.md.

INPUTS:
[ARTICLE DRAFT]
[APPROVED BRIEF]
[CLAIM REGISTER AND SOURCES]
[FIGURE STORYBOARD AND DIAGRAMS]

Review in this order:
1. TECHNICAL VALIDITY: mechanisms, algorithms, architecture, correct versions,
   units, causality, security implications, code and figure semantics.
2. EVIDENCE: direct support for each consequential claim, strength of metrics,
   competing evidence, sample/baseline limitations, unattributed claims.
3. ARGUMENT: thesis, novelty, breadth/depth/height, missing alternatives,
   jumps in reasoning and inaccurate generalization.
4. VISUALS: figure necessity, accuracy, ordering, accessibility and captions.
5. EDITORIAL CRAFT: opening, transitions, density, repeated ideas, SEO promise,
   artificial-sounding phrasing and length proportionality.

Output a verdict of BLOCK / REVISE / READY with explicit reasons. List findings
by severity (BLOCKER, MAJOR, MINOR), location, quoted ABC (current text),
proposed XYZ (exact replacement), and why. Where a whole section needs work,
provide a replacement section rather than vague advice. Do not randomly change
valid diagrams or voice; justify each material alteration. Check the entire
article after each targeted fix for new inconsistencies. Do not assign fake
98% confidence. When uncertain, say which evidence would resolve it.
```

## Prompt 5 — Final Medium release check

```text
You are the release editor. Using the revised article, evidence register,
figures and review findings, perform the publication checklist in
06_EDITORIAL_REVIEW.md. Recheck time-sensitive facts and exact cited claims.
Confirm figures have readable export sizes, alt text and rights/attribution;
code has language labels and is actually tested if claimed; links work if
access is available; title and subtitle accurately reflect the article.

Return:
- Publication verdict: BLOCK / READY WITH DISCLOSED LIMITATIONS / READY.
- Final title/subtitle; synopsis; section and figure order.
- Open blocking issues (if any) and smallest concrete fixes.
- Brief change log: what changed since last review and why.
Do not rewrite the whole article unless necessary; preserve technically sound
text and authorial voice.
```

## Compact instruction for iterative edits

```text
Make a minimal-diff technical edit against the latest approved article.
Use ABC → XYZ → Reason for each change. Reconcile nearby paragraphs, figures,
source references and conclusion for drift. Do not optimize prose at the cost
of precision. Only re-draw a figure if a concrete problem requires it.
Return the complete replacement for every changed passage and the associated
change log. Identify anything unverified.
```

## How to get consistent results

- Supply actual files and source content. A prompt cannot substitute for unavailable code, figures, logs, papers or authoritative verification.
- Preserve the brief and claim register between chats; do not rely on remembered prior review conclusions.
- Keep drafting and reviewing as separate passes, ideally with a fresh review session.
- Re-open the underlying sources for claims that are consequential or time-sensitive.
- Require a stage verdict and blockers. “Looks good” is not a sign-off.
