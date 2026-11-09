# Zen Style Guide

Choose a question the reader can answer by understanding how something works. Give them the context, evidence, and practical implications that make the explanation usable.

## Choose the question and the evidence

Write down the reader’s question and what the reader should be able to explain, diagnose, or decide afterward. Look up related articles in the archive and read the relevant sections. Give this piece a distinct job, such as tracing a failure the earlier piece only named or explaining what changed in a new release. Link the earlier treatment when it supplies useful background.

| Reader’s goal | What to show | Role of code |
| --- | --- | --- |
| Understand a mechanism, such as context assembly or cache invalidation | A small worked example, a diagram, and the condition that changes the outcome | Optional. A trace, calculation, or labeled pseudocode may be enough. |
| Compare designs or interpret research | Comparable assumptions, primary evidence, and a decision boundary | Optional. A published result can support a claim within its measured scope. |
| Build or reproduce behavior | The relevant implementation, versioned steps, and the result the reader should check | Include the smallest runnable example the walkthrough requires. Verify results the article presents as observed. |

Use existing code when it serves the lesson. Create a companion repository only if the brief calls for one or a multi-file reproducer is essential to a promised build. If an essential behavior cannot be verified, narrow the claim, attribute it to a reliable source, or scope the piece as an explainer. Keep any remaining evidence gap with the editor.

Check consequential claims against the specification, versioned documentation, source code, original paper, or experiment that supports them. For reported results, name who measured what, the comparison baseline, and the conditions that matter. Label a thought experiment or synthetic example where it begins. Put any limit that changes the reader’s interpretation beside the claim. Recheck time-sensitive details before publication.

## Write in the order the reader needs

- **Open on the subject.** Start with a real constraint, a concrete question, or an explicitly hypothetical input. Get to the central answer early. Use a scene when it gives the reader something to reason about.
- **Show the mechanism.** Name the actors, inputs, state changes, and outcome that matter. Define an unfamiliar term at its first use. Follow a representative example through the part of the system that explains the result.
- **Give each point one home.** Write the job of each section in a line. If two sections make the same claim, keep it with the best evidence and merge or cut the other. Revisit a concept only when the next passage adds a cause, condition, counterexample, or consequence.
- **Finish with something the reader can use.** End on a diagnostic question, a decision criterion, a boundary case, or an open question earned by the explanation. Cut the recap when the article has already made the point.

Use a calm, direct voice. Prefer specific nouns and active verbs. Replace generic praise with a description of what changes and under which conditions. Keep first person for relevant firsthand choices or observations. Remove drafting narration, staged suspense, and paragraphs that announce what the next paragraph will say.

## Draw the relationship the reader needs to see

Include at least one finished explanatory diagram in every article. Give each figure a question and place it beside the passage where that question arises. Use a flow for movement or decisions, a sequence for timing, and a labeled boundary for ownership or trust. Split a busy figure when its parts answer different questions.

Check that arrows have a clear meaning, labels match the article, and the visual distinguishes an illustration from measured behavior. Write alt text that conveys the relationship and a caption that helps the reader interpret it. Verify legibility at phone width and use labels or shapes alongside color. Use an original figure or document the source and rights for an adapted one. Embed the actual figure, keep an editable source when useful, and export a PNG for publishers that need an image upload. [GitHub diagram formatting](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams)

## Make the article discoverable

Pick the query a reader would use to find this explanation. For search engine optimization (SEO), use the recognizable technical term and the specific question or outcome in one clear title. Give the subtitle a different job, such as naming the scenario, the deciding constraint, or the practical consequence. Use descriptive section headings and write a short, page-specific description where the publisher offers a metadata field. [Google’s title guidance](https://developers.google.com/search/docs/appearance/title-link), [Google’s snippet guidance](https://developers.google.com/search/docs/appearance/snippet), [Medium’s title and subtitle controls](https://help.medium.com/hc/en-us/articles/214895188-Custom-titles-subtitles)

For discovery in AI search and answer engines, often called generative engine optimization (GEO), make the answer easy to interpret in context. Name the entity explicitly, put the condition next to the claim it qualifies, and link directly to the evidence. Cut keyword variants that serve no reader purpose. Google applies its regular search practices to AI Overviews and AI Mode. [Google’s guidance on AI features](https://developers.google.com/search/docs/appearance/ai-features)

## Separate the manuscript from the handoff

Put the title, subtitle, article prose, figures, and reader-facing source links in `article.md`. Deliver working image links or attached assets with it. Keep search metadata, fact-check notes, execution attempts, environment errors, and draft history in a separate editorial handoff when they matter. If a failed run is itself the subject of the article, describe the actual setup, the observed failure, and its consequence for the reader.
