# Reusable Zain-style article prompts

These are **original editorial instructions** based on the author's requirements, not prompts to impersonate a person or copy another creator's wording.

## 1. Research and plan (do this before the prose)

```text
Use the attached Zain Style Writing Pack as the NARRATIVE authority and the
Technical Article Editorial Master Playbook as the FACTUAL and RELEASE authority.

Topic: [TOPIC].
Reader: [AUDIENCE].
Article mode: [MECHANISM / INVESTIGATION / RESEARCH / ARCHITECTURE / TUTORIAL].
Known source links/artifacts: [SOURCES].
Relevant previous article: [LINK, IF ANY].

Retrieve and read the supplied artifacts, not your memory of them. Research
authoritative up-to-date specifications, code, papers, implementation docs, and
meaningful competing evidence. Distinguish official behavior from proposals,
vendor-reported results, local observations, and illustrative examples.

Write the central thesis, reader transformation, counter-thesis, scope and
distinct contribution. Plan an engineering story in complete sentences:
curiosity -> friction -> earlier approach and its limits -> internal mechanism ->
one running example -> failure case -> alternative -> earned judgment.
Use headings that describe substantive technical turns, not a rigid template.

Select 1–3 explanatory figures with exact semantics, captions and alt text.
Choose practical work only if it serves the thesis. For promised code, specify
what must be implemented, run and checked. Track gaps honestly.

Output the completed ARTICLE_WORKSHEET and unresolved BLOCKERS. Do not draft
article prose until research and the central story are defensible.
```

## 2. Write the full article

```text
Using the approved article worksheet and verified sources, write an ORIGINAL,
publishable Zain-style Medium technical article. It should feel like an
engaging technical story told by an experienced practitioner, not an API
reference, checklist, sales piece, or compressed summary.

Opening: one concrete, truthful engineering friction; establish an interesting
question immediately.
Development: connected, rich paragraphs that progressively explain why this
exists, how actors and state interact internally, why the obvious solution fails,
and how a representative case behaves. Place diagrams precisely where they
resolve confusion; introduce code only when it explains necessary behavior.
Analysis: include source-backed claims, a realistic negative case, meaningful
alternative, limits, and conditions under which to choose or reject the design.
Ending: deliver a decision or insight earned through the mechanism, not a recap.

Maintain breadth (context), depth (mechanism), height (judgment), evidence, and
clear limitations. Prefer 8–10 minutes as a starting experience only if the
brief supports it; DO NOT cut mechanisms for brevity. Every paragraph and
section must do a unique job. No artificial suspense, generic hype, endless
bullets, or imitation of any person's exact wording.

Give one SEO-aware true title and a complementary subtitle. State important
definitions close to their first use. Identify the actor, operation, conditions,
and observable result. Keep technical terms stable; resolve ambiguous pronouns;
remove unsupported emphasis. Preserve the source's scope and uncertainty.
Do not flatten useful storytelling into mechanical short sentences.

For a reference-led explainer, use authoritative public demonstrations or
source traces rather than creating a new implementation or installation guide.
Put GEO/AEO metadata and verification notes outside the manuscript. Produce
article.md, complete figures, and a separate editor-handoff.md. Do not claim
tests you did not execute.
```

## 3. Write one section at a time (when requested)

```text
Continue the approved Zain-style manuscript at the NEXT APPROVED SECTION
ONLY, using the current complete article, source register, and storyboard.
Preserve the thesis, examples, terminology, and transitions. Introduce the
new mechanism/evidence that this section alone is responsible for; do not
reintroduce the story or summarize previous sections. Verify important source
claims. Stop after that single complete section; do not promise background
work or request information already provided.
```

## 4. Independent adversarial review

```text
Act as a skeptical senior engineering editor. Re-read the COMPLETE latest
manuscript alongside its original approved brief, Zain Style Guide, Master
Playbook, sources, tested code, and all figures. Critique in this order:

1. False mechanisms, wrong spec/version semantics, insecure or misleading
   diagrams, fabricated/unsupported evidence, and mismatch between test scope
   and article claims. These are blockers.
2. Narrative completeness: does the story have its causal middle, an actual
   trace, meaningful failure/counterexample, and decision boundary? A short
   summary passed off as a feature article is a major defect.
3. Thin/duplicate content: label each section's unique job; quote exact
   redundant passages and propose consolidation without removing unique
   technical content.
4. Practical credibility: can someone reproduce promised results? Distinguish
   executable fixture, mock, external tool execution, and production proof.
5. Diagrams and mobile presentation: semantics, caption, alt text, placement.
6. SEO/AEO/GEO: truthful query intent, accurate title/subtitle, explicit
   sources, no keyword stuffing or ranking guarantees.
7. Final precision review: verify actor clarity, stable terminology, explicit
   conditions, and unambiguous references. Confirm that edits did not remove
   permissions, version limits, uncertainty, negative cases, or evidence scope.
   Do not mechanically ban analogies or stylistic rhythm.

Return findings as ABC (actual text or defect) -> XYZ (specific replacement)
-> reason/evidence and severity. Provide a corrected complete manuscript
when asked to revise, not isolated editorial fragments.
Declare BLOCK / REVISE / READY WITH DISCLOSED LIMITATIONS / READY.
```

## 5. Final publication audit

```text
Check the finished Medium manuscript as a reader: engaging and precise opening,
continuous technical argument, a representative worked example, at least one
finished necessary diagram, accurate primary links, limitations in context,
non-repeating final judgment. Ensure metadata is separate and title matches
the evidence. Check all source versions and factual claims one final time.
No invented tests, performance numbers, or firsthand experience. Publish
status only after confirming the actual asset files are accessible.
```
