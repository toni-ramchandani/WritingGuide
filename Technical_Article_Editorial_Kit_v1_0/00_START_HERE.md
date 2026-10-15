# Technical Article Editorial Kit — v1.0

**Purpose:** Turn a topic into an original, evidence-grounded, technically substantial Medium article. Adapted from analysis of Anthropic Engineering posts; **not** an Anthropic template, endorsement, or reproduction of its wording.

**Editorial promise:** Every article should help an experienced reader understand a mechanism, recognize a meaningful trade-off, or make a better technical decision. Breadth supplies context; depth explains mechanisms; height produces judgment. Evidence makes the argument defensible. Figures make the reasoning visible.

## What is in this kit?

| File | When to use it | Output / decision |
|---|---|---|
| `01_EDITORIAL_STANDARD.md` | Before every new article or when reviewing one | Shared quality bar, article archetypes, writing principles |
| `02_ARTICLE_BRIEF_TEMPLATE.md` | Stage 1: plan the article | Approved one-page-to-two-page editorial brief |
| `03_EVIDENCE_GUIDE.md` + `03_CLAIM_REGISTER.csv` | Stage 2: research and source validation | Traceable claims, contradictory evidence and gaps |
| `04_VISUAL_STORYBOARD_TEMPLATE.md` | Stage 3: diagram planning | Figure specifications tied to reader questions |
| `05_PROMPT_LIBRARY.md` | To run each stage in ChatGPT or another writing assistant | Independent prompts for researcher, drafter, reviewer, editor |
| `06_EDITORIAL_REVIEW.md` | Before any draft is accepted for publication | Blocking defects, severity-ranked revisions, sign-off |
| `07_WORKED_EXAMPLE_RETRIES.md` | See how the system works on a non-AI topic | Filled brief + sample evidence/figures; **not** an article |
| `08_SOURCE_PATTERN_NOTES.md` | Revisit source-inspired techniques | Auditable editorial observations and original links |

## Minimal operating sequence

1. **Frame:** Fill `02_ARTICLE_BRIEF_TEMPLATE.md`. State one falsifiable or at least challengeable thesis, target audience, one genuine engineering tension, scope boundary, expected takeaway, and article archetype.
2. **Research:** Complete the relevant rows in `03_CLAIM_REGISTER.csv`. Resolve claims that would affect the article's recommendation; preserve dissenting findings and version assumptions.
3. **Storyboard:** Complete `04_VISUAL_STORYBOARD_TEMPLATE.md` for the figures actually needed. Draft figure logic **before** writing detailed technical sections. A text-only article is acceptable if figures would not help.
4. **Draft:** Use the drafting prompt in `05_PROMPT_LIBRARY.md`, passing the actual brief, source register and storyboard. The body must advance an engineering argument, not mechanically follow a generic benefits/use-cases template.
5. **Review:** Use `06_EDITORIAL_REVIEW.md` in an independent pass. Report factual and conceptual defects before copyediting. Provide precise replacements for significant issues. Iterate until all release blockers are resolved.
6. **Publish:** Verify the final title, sources, captions, image rights, mobile figure legibility, Medium formatting, and any time-sensitive facts.

## Stage gates and handoffs

| Gate | Must be true to proceed |
|---|---|
| G1 — Brief accepted | One thesis; audience; reader transformation; problem/tension; scope; and section-to-argument map |
| G2 — Evidence ready | Critical claims sourced or marked clearly as hypotheses; important disagreements addressed; no invented tests, metrics or firsthand experience |
| G3 — Visual architecture ready | Every proposed figure has one explanatory job, underlying facts and a caption/alt-text plan |
| G4 — Draft ready to review | Technical mechanism is present, sections progress causally, examples are identified as measured or illustrative, source citations are attached |
| G5 — Publication ready | No blocking defects in `06_EDITORIAL_REVIEW.md`; final sources, visuals, headline and copy verified |

**If a gate fails:** Return to the earliest affected artifact. Do not fill a source or experimental gap with fluent prose. When evidence is unavailable, narrow the claim, add a clear qualification, design a reproducible experiment, or omit the claim.

## Quick start for a new chat

Attach `01` through `06` and say:

> Apply this editorial kit to **[TOPIC]** for **[AUDIENCE]**. Start with an evidence-backed editorial brief, not a complete article. Challenge the thesis, choose an appropriate article archetype, map breadth/depth/height, identify sources and uncertainties, and propose a minimal figure storyboard. Stop at Gate G1 and tell me what remains unverified for Gate G2.

When advancing stages, pass the **actual latest version** of the previous artifacts. Do not assume an assistant still has the same source materials from another conversation.

## Versioning and change discipline

At the top of every active article brief, record `Article ID`, `Version`, `Date`, `Status`, and `Source snapshot date`. Preserve decisions and unresolved issues in the brief. When updating, state what changed and why. Changes to the thesis require revisiting evidence, section structure and diagrams.

## Source-derived inspiration

Three primary readings:
- [Anthropic Engineering — Claude Code auto mode](https://www.anthropic.com/engineering/claude-code-auto-mode)
- [Anthropic Engineering — Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
- [Anthropic Engineering — Harness design for long-running applications](https://www.anthropic.com/engineering/harness-design-long-running-apps)

Use these to study editorial craft, not as universal evidence for an unrelated technical claim. The article's own subject requires its own sources.
