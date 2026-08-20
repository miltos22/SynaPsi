# SynaΨ — Prior Art Map

This document is part of the defensive disclosure. It maps each component of the SynaΨ architecture to the closest known prior art, and states precisely what is *not* covered by prior art. Being honest about antecedents strengthens the disclosure: it claims only the integration and the generalization, not the parts.

## Components vs. Prior Art

| Component | Closest prior art | Status |
|---|---|---|
| Critic expert(s) — separately-trained, contributing thinking to self-critique within the generation process | LLM-as-Judge (Zheng et al., 2023); self-recognition / self-preference bias (Panickssery et al., 2024); cross-model judging; self-refine / external-feedback reflection; reward models trained separately from the generator (RLHF); RL Tango (joint generator-verifier RL, NeurIPS 2025) | Established |
| Verification is easier than generation; weak verifiers | Weaver / "Shrinking the Generation-Verification Gap" (Saad-Falcon et al., 2025); Hard2Verify (Salesforce, 2025); GenRM; "Mind the Gap" (self-correction fails) | Established |
| Knowledge database oracle — tracks the model's overall knowledge, requested during generation | "Knowing What LLMs Know" (Kadavath et al., 2022); RAG knowledge bases; knowledge-probing literature | Established / partial |
| Continuous sentiment memory — weight-based (in the model's weights, not context), applied in real time when reasoning touches a subject | Fast weights / memory-augmented networks (Schmidhuber); parameter-efficient adapters (LoRA) and adapter-fusion personalization; test-time training; DAM-LLM "Dynamic Affective Memory Management" (2025); emotional-memory / Affective Field Theory implementations (2026) | Established (mechanism) / partial (weight-encoded per-subject sentiment injected in real time) |
| Calculator integrated into the LLM's own process, no external tool call | IGC "Integrated Gated Calculator" (2025) — calculator emulated inside the model, gated, discrete; Rune (activation-routed calculator without prompt parsing, 2026) | Established (calculator instance) |
| Routing / tool dispatch | Semantic routers, tool-selection routing, agent tool frameworks | Established |
| Non-LLM neural world / physics predictors as routable experts | World models (Ha & Schmidhuber 2018; Dreamer); learned simulators (GNN-based, DeepMind); physics-informed neural networks (PINNs) | Established (the predictors) — routing them as alternate-architecture experts within an LLM cognitive process is part of the assembly claim |
| Epistemic honesty, abstain-when-uncertain, knowledge-aware refusal | Alignment for Honesty (2023); Epistemic Integrity (2024); Knowledge-Aware Refusal (Pan et al., 2025); MASK benchmark; calibration/abstention literature; Ψ as Confidence-Evidence Ratio ("The Polite Liar", 2025) | Established (extensive) |

## Claimed Novelty (not found as prior art in the searches performed, as of 2026-08-20)

1. **The assembly** — no single published system was found combining generator-demoted-from-truth + internal router (routing authority for decidable spans) + alternate architectures + independently-trained critic + continuous sentiment memory + knowledge oracle + honesty value function, as one coherent personal-assistant architecture.

2. **Routing to alternate architectures as a general principle** — IGC and Rune cover the *calculator* instance and activation-sourced routing; the generalization — routing decidable computation to *heterogeneous non-LLM systems of different architectures* (simulators, solvers, checkers, calculators, and learned non-LLM world/physics predictors) as an internal part of the same cognitive process — was not found stated as such.

3. **Sentiment-only storage principle** — affective memory exists, but the explicit design rule "store only polarity, never interpretations, to minimize the storage's error surface and avoid entrenching misattributed causes" was not found stated as an architectural principle.

## Method

Searches performed 2026-08-20 over web/arXiv/GitHub. This map is a good-faith snapshot, not an exhaustive legal analysis. Verify before relying on it for anything beyond defensive publication.
