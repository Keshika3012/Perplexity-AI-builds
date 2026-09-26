# AI Product Builds: Perplexity

Ten AI product management builds, applied to a single product.

This repo works through ten recurring problems in AI products (citations,
evals, failure UX, cost, memory, safety, latency) as improvements to one product:
**Perplexity**.

**Why Perplexity:** it's an AI search product where every one of these problems is live and
visible. Its citations, retrieval failures, model choices and pricing are all observable
from the outside, so each spec is grounded in real user complaints and real constraints
rather than invented ones.

One build per week for ten weeks, then two weeks turning the strongest work into case
studies.

## Builds

| # | Build | Problem it solves | Artifact | Status |
|---|---|---|---|---|
| 1 | AI Search with Source Links | Unverifiable answers destroy trust | Spec + Figma flow | In progress |
| 2 | Smart Model Routing | Frontier models on trivial queries burn margin | PRD + cost model + router code | Not started |
| 3 | Product Health & Feedback Dashboard | No signal on where answers fail | Metric spec + sheet | Not started |
| 4 | Speed & Loading UX | Multi-second waits feel broken | Prototype | Not started |
| 5 | Privacy & Memory Controls | Personalization without consent feels invasive | Mockups + microcopy | Not started |
| 6 | Handling AI Mistakes Gracefully | Failure with no recovery path loses the user | Flow + error taxonomy | Not started |
| 7 | Edge-Case Test Suite (Evals) | No way to know if a prompt change broke things | Eval runner + results | Not started |
| 8 | Safety & Polite Refusals | Accusatory refusals damage the brand | Spec + test cases | Not started |
| 9 | Smart Caching | Repeated queries pay full price every time | PRD + latency demo | Not started |
| 10 | Prompting vs Training Decision Guide | Teams over-engineer what a prompt could fix | Decision doc | Not started |

## How each build is structured

Every build folder contains:

- `spec.md`: problem, target user, evidence, proposed solution, success metrics
- `decisions.md`: trade-offs considered and why I chose what I chose
- Artifacts: designs, code or sheets, depending on the build

Where a build can be demonstrated rather than described, it is. Builds 2, 7 and 9 include
working code.

## Repo structure

```
builds/
  01-source-links/
  02-model-routing/
  ...
teardowns/
case-studies/
```

`teardowns/` holds weekly teardowns of other products, written as separate practice in
finding and framing product problems.

## Build log

| Week | Date | What shipped |
|---|---|---|
| 0 | 25 Sep 2026 | Repo set up, product chosen |

---

*Independent portfolio project. Not affiliated with or endorsed by Perplexity AI.*
