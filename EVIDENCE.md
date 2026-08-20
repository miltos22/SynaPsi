# SynaΨ — Preliminary Evidence

Empirical signals collected while developing the pipeline that motivates the SynaΨ architecture. These are small, preliminary results on a single machine — included for context, not as claims of general validity.

## 1. Weak-verifier data gating catches confident-wrong traces

A weak, independently-run verifier (a paid DeepSeek flash model) was used to grade reasoning traces produced by frontier open-weight teachers (Qwen3.8-Max-preview, GLM-5.2, Kimi K3). Given a batched-10 protocol with an explicit tricky-question scan, the weak verifier correctly identified trap questions where the frontier teachers answered confidently and wrongly:

- Carwash trap: graded 40 with correct reasoning (a one-pass grader had scored it 70).
- TV trap: graded 28 with correct reasoning (one-pass: 70).

This supports the "verification is easier than generation" asymmetry and the value of a decoupled critic — the runtime counterpart of which is the SynaΨ critic expert.

## 2. Filtered distillate beats its own base

A grade-screened reasoning fine-tune (11,889 graded rows, all > 60/100, math/coding bottom halves removed) on an 8B MoE base scored **68.5 / 100** on a 40-question mobile-assistant benchmark vs the untrained base's **65.0**, including large gains in practical (65→81) and everyday-tech (65→80) categories. Logic dropped (80→52) — an expected trade on the first pass, addressed by category-weighted training in the follow-up round.

## 3. Abstention as a feature

The same fine-tune, without an inference-time clause, became a refusal machine (13/40 answered). Per the SynaΨ value function, abstention on unverifiable content is treated as correct epistemic behavior, not a failure — scored separately as `abstained (good)` vs `confidently-wrong (bad)`.

---

**Status:** raw notes from a private training project. Reproducibility is limited to the described setup. No claims beyond the specific configurations tested.
