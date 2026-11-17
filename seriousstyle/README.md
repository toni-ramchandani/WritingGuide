# SeriousStyle

**SeriousStyle v1.0** is a separate writing mode for technical and business documents that must be easy to understand on the first read. It favors concrete claims, explicit ownership, complete explanations, and restrained language.

SeriousStyle draws on [docwriter-org/plain-writing-skill](https://github.com/docwriter-org/plain-writing-skill), especially its attention to plain vocabulary, complete sentences, consistent terms, and removing empty emphasis. It is a **selective, original adaptation**, not a verbatim copy or an official release of that skill. See [source decisions and evaluation](SOURCE_AND_EVALUATION.md) and [upstream MIT license](THIRD_PARTY_LICENSE.md).

## Which writing mode should I choose?

| Mode | Main job | Typical output |
| --- | --- | --- |
| [SeriousStyle](SERIOUSSTYLE_GUIDE.md) | Explain facts, decisions, risks, changes, and responsibilities plainly | Architecture decision, incident report, RFC, technical memo, project status, research summary |
| [Zain Style](../Zain_Style_Writing_Pack/README.md) | Teach a complex idea through original technical storytelling | Medium feature, deep engineering essay, conference article |
| [Zen Style](../Zen_Style_Writing_Pack/README.md) | A restrained, question-led conceptual explanation | Focused conceptual guide, shorter technical explainer |
| [Technical master playbook](../TECHNICAL_ARTICLE_MASTER_PLAYBOOK_v1_0.md) | Set factual, sourcing, visual, and verification gates | Applies to all modes when discussing engineering facts |

**Default for SeriousStyle:** concise but complete, formal without legalistic wording, sober without being cryptic. It is not the default for Zain articles. Do not silently apply SeriousStyle's restrictions to Zain writing.

## Files

- [SERIOUSSTYLE_GUIDE.md](SERIOUSSTYLE_GUIDE.md) explains the style, information order, evidence rules, editing method, and genre-specific structure.
- [WRITING_PROMPTS.md](WRITING_PROMPTS.md) contains ready-to-use prompts for drafting, revising, and reviewing.
- [REVIEW_CHECKLIST.md](REVIEW_CHECKLIST.md) defines blocking issues, an explicit semantic-preservation audit, and the acceptance standard.
- [EXAMPLES.md](EXAMPLES.md) shows before-and-after passages and distinguishes SeriousStyle from Zain Style.
- [SOURCE_AND_EVALUATION.md](SOURCE_AND_EVALUATION.md) audits upstream rules, documents intentional departures, and defines a useful evaluation protocol without inventing results.
- [THIRD_PARTY_LICENSE.md](THIRD_PARTY_LICENSE.md) preserves the upstream MIT notice.

## Quick start

> Read `seriousstyle/SERIOUSSTYLE_GUIDE.md`. Write a SeriousStyle `[document type]` for `[reader]` about `[topic]`. State the main fact or decision first. Preserve every source-backed claim, condition, number, scope limit, and uncertainty. Name who performed or must perform each action. Use clear, consistent technical language and remove promotional wording. Use the relevant document structure. Then apply `seriousstyle/REVIEW_CHECKLIST.md` and report unresolved factual gaps separately.

Use **SeriousStyle as a complete mode** for professional documents, or as a **selective clarity pass** for other modes when requested. A selective pass must not flatten Zain's narrative voice.

## Status

Version 1.0. Source review: 17 November 2026. Upstream source was reviewed, not executed as an installed agent skill. No claim is made that this guide outperforms its source or other guides.
