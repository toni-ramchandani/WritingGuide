# Source Pattern Notes — Why We Built This Editorial System

**Analysis scope:** The three Anthropic Engineering articles supplied as models for editorial quality. These notes distinguish observations about *writing design* from technical claims within the source articles. They are not a style guide published by Anthropic and do not grant a license to reuse its prose or art.

**Primary editorial references:**

1. [John Hughes, “How we built Claude Code auto mode: a safer way to skip permissions,” Anthropic Engineering, Mar 25, 2026](https://www.anthropic.com/engineering/claude-code-auto-mode).
2. [“Demystifying evals for AI agents,” Anthropic Engineering, Jan 9, 2026](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents).
3. [Prithvi Rajasekaran, “Harness design for long-running application development,” Anthropic Engineering, Mar 24, 2026](https://www.anthropic.com/engineering/harness-design-long-running-apps).
4. [Anthropic Engineering index](https://www.anthropic.com/engineering/).

## Pattern A — Engineering decision narrative (auto mode)

**What the source does:** opens with a concrete usage observation (93% approval rate), compares permission modes, explains why neither fully solves the problem, introduces the design, exposes threat models and implementation choices, publishes classifier performance and discusses residual risk. The source reports a 0.4% false-positive rate on real internal traffic and a 17% false-negative rate on its 52-example set of real overeager actions for the two-stage pipeline; these are *source-reported results under different test sets*, not an independent validation or universal performance estimate.

**Editorial lesson:** Make the design's constraints and disadvantages visible. Metrics can increase trust if their denominators, conditions and remaining failure modes are explained; cherry-picked metrics cannot.

**Figure roles visible in source:** trade-off map, system architecture, visibility/input boundary, two-stage classifier pipeline. Each answers a different reader question.

**What not to copy:** Anthropic's product-centered architecture structure, its exact phrasing, or its metrics as evidence for other security tools.

## Pattern B — Layered conceptual methodology (agent evals)

**What the source does:** establishes why the subject is hard, defines a precise vocabulary (tasks, trials, graders, transcripts, outcomes, harnesses), contrasts single-turn with agent evaluation, compares grading methods and develops a practical methodology. It includes source-linked examples and figures to distinguish evaluation objects and outcomes.

**Editorial lesson:** Introduce terminology immediately before it becomes necessary to reason about the system. Use conceptual figures early so later methodology is interpretable. Breadth works when readers can map each part to the central mental model.

**Risk to avoid:** Copying broad survey structure blindly. On an otherwise focused topic, too many categories dilute the central technical thesis.

## Pattern C — Transparent engineering investigation (long-running harness)

**What the source does:** names shortcomings in earlier approaches, explains the generator/evaluator design, reports a concrete application-building attempt and its observed behavior, discusses self-evaluation problems and new trade-offs as models change. The article reports a six-hour / $200 full-harness run against a 20-minute / $9 solo run, but the compared applications differed in scope and implementation. These observations are meaningful practitioner evidence, **not** a cost-normalized controlled study demonstrating universal superiority.

**Editorial lesson:** Show what broke, what was tried, what changed and what remained imperfect. A credible case study distinguishes witnessed results from the author's interpretation.

**Risk to avoid:** Retrofitting a first-person investigation where none occurred, or treating a single case study as an industry-wide benchmark.

## Combined editorial synthesis

Our reusable writing mental model is:

> **Investigate → Explain → Substantiate → Synthesize**, using **Breadth → Depth → Height** to balance context, causal mechanism and practical judgment.

That is **our** editorial model distilled from the readings, not terminology or a formal method claimed by Anthropic. It is expressed operationally through the brief, claim register, storyboard, independent review and release gates.

## How to credit the sources responsibly

When discussing this writing method publicly, say it was *informed by studying engineering articles including Anthropic Engineering posts*. Do not imply Anthropic approved this playbook or created its specific forms. In any published topic article, cite original technical sources needed for that topic independently of these editorial references.
