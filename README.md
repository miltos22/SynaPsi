# Project SynaΨ

**Honest-by-architecture.** An integrated cognitive system for personal assistants, published as a defensive disclosure.

**Thesis: the source of truth is never the generator.** The generator authors interpretation; decidable computation is routed to alternate architectures; an independently-trained critic audits; a continuous sentiment memory carries per-user experience without interpretation.

Date of disclosure: 2026-08-20

---

## The Architecture

1. **Generator** — produces the output stream. Demoted from source of truth; it is the author only of interpretation.
2. **Router** — an internal component of the cognitive process that **activates routing authority for decidable spans**. The activation mechanism is intentionally left unspecified; any means of granting the router authority over a span of the generator's process falls within this disclosure.
3. **Alternate architectures** — heterogeneous, non-LLM computation engines (simulators, solvers, checkers; a calculator is one example) to which decidable spans are routed. The result of a routed span is part of the same cognitive process as the generator's own output.
4. **Critic expert** — a component specialized for critique, **trained separately from the generator**, so that its independence is structural rather than nominal. It is part of the thinking process itself: when the system self-criticizes, the critic contributes its own thinking to the self-critique.
5. **Knowledge oracle** — a knowledge database: a pre-compiled, separately-trained expert dedicated to keeping track of the model's overall knowledge, requested regularly during generation.
6. **Continuous sentiment memory** — accumulates polarity over time. It stores no interpretations, only sentiment. The reasoning component interprets; the critic audits.
7. **Value function** — epistemic honesty: **abstain > confidently-wrong**, everywhere.

## Governing Principles

- The source of truth is never the generator.
- Decidable is computed, not generated.
- The critic's independence is trained in, not assumed.
- Memory stores sentiment; reasoning interprets; the critic audits.

## Claimed Novelty

The individual components have prior art (see `PRIOR_ART.md`). This disclosure claims:

1. **The assembly** — the components above combined into one coherent system for a personal assistant, with the generator structurally demoted from source of truth.
2. **Routing to alternate architectures as a general principle** — decidable computation routed to *heterogeneous* non-LLM architectures as an internal part of the cognitive process; the calculator is one instance, not the claim.

## On the Name

Ψ is also used in the epistemic-honesty literature as the **Confidence-Evidence Ratio** (assertoric force proportional to evidential warrant). The name is an intentional fit: this system is built around honesty as its product.
