# Research and Claim Evidence — Operating Guide

Use this alongside `03_CLAIM_REGISTER_TEMPLATE.csv`. Copy the CSV into an article workspace, rename it `ART-YYYY-NNN_claims.csv`, and populate a row for **each material claim**. A material claim is one that influences the thesis, the mechanism, a visual, an important numerical assertion, a comparison, or the recommendation. Minor connective prose does not need a row.

## Claim taxonomy

| Type | Meaning | Required language |
|---|---|---|
| `SPEC` | Normative requirement or defined semantics from a standard/specification | Anchor to the exact section and applicable version |
| `IMPLEMENTATION` | Observable behavior in a specific implementation/release | Name component, repository and version/commit if known |
| `RESEARCH` | Finding from a paper or controlled study | Give population/task, experimental setting, methodology and key limits |
| `REPORTED` | Engineering finding reported by another team/company | Attribute to source and describe scope; do not present as independently validated |
| `FIRSTHAND` | Author's direct test, code reading or operational observation | Include reproducer, test setup, date, raw logs/results where publishable |
| `ILLUSTRATIVE` | Invented but logically coherent example for teaching | Label illustrative; no claims of field measurement |
| `INFERENCE` | Our interpretation that joins facts into a conclusion | State premises, reasoning and uncertainties |
| `HYPOTHESIS` | Plausible but unverified candidate explanation | Use tentative language and define a test; do not state as fact |

## Mandatory fields for material claims

`claim_id`, `draft_claim`, `claim_type`, `source_title`, `source_url_or_artifact`, `source_anchor`, `version_or_population`, `method_or_conditions`, `limitation_or_counterevidence`, `verification_status`, `used_in_section_or_figure`.

Other fields help track origin, publication date and editorial edits. Never write “verified” merely because a web page exists. Verify that the **specific** source statement supports the **specific** claim.

Suggested verification statuses: `TO_CHECK`, `SUPPORTED`, `QUALIFY`, `CONFLICTED`, `UNSUPPORTED`, `EXCLUDED`.

## Source selection and triangulation

1. **Start with authoritative ownership.** For semantics, use a specification. For current product behavior, use official versioned docs/source. For effectiveness claims, use empirical studies or transparent field investigations.
2. **Read more than summaries.** Locate the decisive definition, figures, experimental setup, tables, caveats and counterclaims. Avoid using a search-result snippet as the entire evidence base.
3. **Inspect conflicts.** Why do sources disagree? Different versions, populations, definitions, test harnesses, baselines, incentives, or measurement periods?
4. **Check the time axis.** Record source publication/access date and applicable version. Current rules and API behavior may have changed.
5. **Separate the kinds of evidence.** Code inspection confirms current implementation branches, not fleet-wide failure rates. A vendor blog explains its reported case, not all deployments. A synthetic example clarifies logic, not empirical effectiveness.
6. **Use counterevidence deliberately.** An alternative approach can be the right choice under different constraints. Report those conditions instead of arguing for one universal winner.

## Claim escalation policy

- **SUPPORTED:** use a precise claim, cite the source, preserve conditions.
- **QUALIFY:** narrow language until it matches support; remove extrapolation.
- **CONFLICTED:** present disagreement and its plausible causes; no definitive recommendation without a way to resolve it.
- **UNSUPPORTED:** perform an experiment, find a stronger source, mark as hypothesis, or remove it.
- **High-impact result or metric:** check denominator, sample, baseline, methodology, confidence/variability when available, and applicability. Do not invent missing statistical uncertainty.
- **Security/safety guidance:** prioritize the exact threat model and boundary conditions; avoid implying that a mechanism guarantees safety.

## Research deliverable at G2

Produce a 1-page **Evidence Synthesis** with:

1. What is established and why.
2. What source authors report (and under what conditions).
3. What is disputed or uncertain.
4. Which original figure/example/experiment can clarify it.
5. Which claims should be narrowed or excluded.
6. Which citation sources must appear in the published article.

An evidence register is a working control, not a demand to cite every sentence in Medium. Cite close to the claims that require verification, and include links to the most authoritative originals.

## Source reuse, permissions and confidentiality

Paraphrase with proper attribution; do not reproduce extended source passages. Visuals from papers/vendor posts can require explicit licensing or permission. A recreated diagram closely following a source still needs attribution and rights review. Do not use internal project names, customer data, private telemetry or proprietary screenshots without approval. When firsthand access is unavailable, describe a reproducible public demonstration instead.
