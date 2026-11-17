# SeriousStyle writing prompts

Use with [SERIOUSSTYLE_GUIDE.md](SERIOUSSTYLE_GUIDE.md) and [REVIEW_CHECKLIST.md](REVIEW_CHECKLIST.md). The prompts specify the intended reader and source contract. They are original adaptations of the upstream [Plain Writing Skill](https://github.com/docwriter-org/plain-writing-skill).

## Draft a new document

```text
Write a SeriousStyle [DOCUMENT TYPE] for [READER AND DECISION] about [SUBJECT].

Use the supplied source materials: [FILES / LINKS / FACTS]. Read the actual
sources rather than recalling them from memory. Begin with the conclusion,
recommendation, current status, or answer appropriate to the document type.

Name the component or person responsible for each action. Use simple words
without replacing precise technical terms. Explain essential context in
reading order. Keep numbers, conditions, versions, permissions, uncertainty,
and negative evidence next to the claims they qualify. Define technical
terms only where a capable reader needs help.

Use the matching structure in SERIOUSSTYLE_GUIDE.md. Give each substantive
idea one home. Prefer paragraphs to decorative lists. Avoid marketing
adjectives, slogans, artificial suspense, and unearned analogies.

Do not invent sources, tests, decisions, owners, dates, or outcomes.
If essential evidence is missing, state the limitation explicitly.

Run the REVIEW_CHECKLIST.md after drafting. Deliver the complete document,
with factual or editorial blockers listed separately.
```

## Revise without changing the claim

```text
Revise this material in SeriousStyle:
[TEXT]

First, extract material claims, actors, actions, scope, evidence type,
numbers, dates, versions, permissions, negations, and unresolved questions.
Treat them as a locked semantic contract.

Rewrite for a reader who is technically capable but has not read earlier
messages. Put the main conclusion first, follow causal and temporal order,
and use precise, consistent technical terms. Replace empty emphasis and
ambiguous pronouns. Do not compress away a substantive failure mode,
qualification, or competing interpretation.

After editing, compare the rewrite against the locked claims. Report any
factual gap that cannot be resolved from the source. Return a complete,
standalone revised text; provide a short change summary only if requested.
```

## Deslopify a draft

```text
Apply a SeriousStyle clarity pass to the text below. Keep its original
substantive intent and evidence. Remove generic openings, vague abstract
claims, needless synonyms, rhetorical flourishes, repeated sentences,
promotional adjectives, and unnecessary bold or lists.

Identify actors and actual effects. Keep every material condition and
limitation. Do not invent new evidence. If an analogy is needed to prevent
misunderstanding, allow a short, accurate one rather than enforcing a
blanket stylistic ban. Preserve technical terms and code as given.

Then apply the semantic-preservation audit from REVIEW_CHECKLIST.md.
[TEXT]
```

## Independent factual and editorial review

```text
Review the COMPLETE latest SeriousStyle document together with its cited
sources and requirements. Challenge the conclusions rather than praising
fluency.

In order:
1. Test truth: every quantified, version-specific, causal, security, and
   execution claim matches evidence. Find missing limits and counterexamples.
2. Test completeness: an unfamiliar reader has the necessary context,
   alternative, decision or outcome, and next responsible action.
3. Test mechanism: actors and state changes are accurate and consistent.
4. Test readability: plain words, complete sentences, stable terms, one
   claim per paragraph, meaningful headings, restrained formatting.
5. Test semantic preservation: no rewritten claim lost a negation, permission,
   number, condition, uncertainty, unit, or evidence label.

Produce severity-ranked findings with EXACT text/problem -> exact replacement
or action -> source/reason. Assign BLOCK / REVISE / READY WITH DISCLOSED
LIMITATIONS / READY. Do not invent a quality score or imply an evaluation
experiment occurred.
```

## Apply clarity only to a Zain-style feature

```text
Run ONLY the SeriousStyle precision pass on this Zain-style article.
Improve vague actors, ambiguous references, unstable terminology, inflated
claims, and unsupported certainty. Do not replace the narrative structure,
running example, diagrams, pacing, analogy, or authorial voice with a dry memo.
Preserve all conditions and evidence limits and report substantive edits.
```

For initial drafting, prefer the complete style. For long-form Zain articles, use only the final prompt unless the author explicitly requests a SeriousStyle rewrite.
