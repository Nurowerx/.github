# Resident Model Lab
## Preliminary technical research note
**Nurowerx | Active research | Version 0.1 | November 2026**

> **Disclosure:** This note describes a working experimental software tool and an initial, very small evaluation, based on the project's reported development summary. It is not a peer-reviewed paper, independent replication, released implementation, or a claim of proven improvements to model capability, speed, or hardware cost.

### Summary

Resident Model Lab studies the tradeoff between **fast GPU-resident model components** and slower component retrieval in local language-model inference. The current implementation operates on an existing **OLMoE** mixture-of-experts model; Nurowerx has developed the software controlling and evaluating expert residency, **not the underlying foundation model**.

The program is a local command-line research system. It is not yet a consumer assistant, general-purpose deployment, downloadable application, or validated demonstration that a powerful model can retain its full capability on significantly cheaper hardware.

### Research question

Can selective expert residency and task-stage selection reduce the amount of model state held in fast accelerator memory, while keeping the quality and latency of local inference within useful bounds?

An *expert* is a mathematical component in a mixture-of-experts (MoE) architecture. Expert IDs are not necessarily interpretable skills such as "mathematics" or "programming".

### Implemented execution modes

| Mode | Mechanism | Expected tradeoff |
| --- | --- | --- |
| **Exact execution** | Fetches the experts requested by the original model, limiting the number kept resident in fast GPU memory. | Preserves the model's original expert-selection computation, but transfers and loading can increase latency. |
| **Adaptive execution** | Restricts active computation to a selected set of 16 experts across a generated span, reconsidering selection every eight generated tokens. | May reduce component movement, but changed expert choices can cause answer-quality degradation. |

In adaptive mode, the runtime can either **recompute the conversation context using the newly selected experts** or **continue with the existing internal history**. These alternatives are part of the research design, not demonstrated equivalences.

### Working implementation and observables

The software includes mechanisms to control which experts are loaded and resident, plus instrumentation intended to evaluate GPU/host memory behavior, component loading and transfers, response latency, and task correctness.

**Exact execution matched the reference implementation's generated tokens on the tested requests.** This is a bounded functional check, not proof of equality over all prompts, decoding configurations, or model workloads.

### Preliminary task-evaluation results

Reported outcomes from an initial set of **eight tasks**:

| Method | Tasks passed | Tasks not passed |
| --- | ---: | ---: |
| Exact execution | 5 | 3 |
| Ordinary quantization baseline | 5 | 3 |
| Adaptive execution, tested 16-expert configurations | 2 | 6 |

The adaptive configurations performed worse on this small task set. The reported result is meaningful as a **failure signal for the current approach**, but the sample is too small to establish comparative effectiveness or generalize to other tasks.

These counts measure task passes, **not** measured peak VRAM savings, total host memory, model loading volume, energy use, tokens per second, or dollar cost. No numerical performance claims for those other quantities are made here.

### What is established vs. unresolved

**Implemented / reported observations**
- A functional local research runtime and CLI exist.
- Exact and restricted adaptive execution modes have been implemented.
- Exact-mode output matched reference tokens on tested requests.
- Preliminary 8-task testing exposed quality degradation with the tested adaptive mode.

**Not established**
- Reliable adaptive expert choice that preserves general task quality.
- A demonstrated speed improvement after accounting for expert transfers and context recomputation.
- A specific reduction in peak GPU memory with acceptable quality and latency at comparable settings.
- Generalization to diverse tasks, larger models, devices, or deployment environments.
- A commercial product or production-grade personal assistant.

### Next experiments

1. Preserve the exact path as a reproducible correctness reference.
2. Freeze and document hardware, software versions, model checkpoint, quantization, generation settings, seeds, task prompts, scoring and run logs.
3. Expand quality evaluation beyond eight tasks; include repeated runs, broader task types and robust failure analysis.
4. Compare distinct adaptive-selection policies and selection intervals, including whether full context recomputation helps.
5. Measure GPU/host residency, transferred bytes, expert-load time, end-to-end latency, and throughput *alongside* quality.
6. Compare against realistic alternatives, including ordinary quantization, conventional offloading, and smaller models under comparable hardware and task conditions.
7. Explore trained or learned selection policies only after establishing reliable evaluation baselines.

### Public release and evidence policy

This note intentionally contains no unpublished source code, private experimental fixtures, confidential model artifacts, credentials or implementation details beyond the disclosed research summary. A dedicated project repository may be established privately while provenance, licenses, reproducibility materials, and release readiness are reviewed.

**Source of current status:** project team's supplied implementation and evaluation summary. Independent inspection of execution logs, hardware measurements, code and benchmark fixtures has not yet been performed for this note.

---

*Nurowerx · Independent research and technical development · Colorado, USA*
