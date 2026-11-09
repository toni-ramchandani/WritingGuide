# Editorial notes for the RAG example

| Decision | Application |
| --- | --- |
| Reader question | Where can the decisive clause disappear when a source is already indexed? |
| Mode | Conceptual explainer for engineers who know the basics of RAG. The fictional policy and two traces make the mechanism visible. |
| General mechanism | The article cites Anthropic’s description of passage selection and prompt input. Its budget and rank assumptions belong to the illustration. |
| Reader test | The last section adds a paired evaluation. It isolates whether the model uses the defect condition after it receives both clauses. |
| Figure handoff | An original diagram compares the two paths. Use the [PNG export](figures/exception-trace.png) for image uploads or edit the [SVG source](figures/exception-trace.svg). The article carries its alt text and caption. |
| Search intent | Why does RAG miss a fact that is in the source document? |
| Search description | When a RAG support assistant gives the wrong answer about a return, check candidate rank, prompt budget, and how it applies the defect clause. |
| Suggested slug | `rag-misses-policy-exception` |
