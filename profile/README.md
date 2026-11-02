<div align="center">

<img src="./assets/nurowerx-github-banner.svg" width="100%" alt="NUROWERX — THE NEXT FRONTIER IS HUMAN. Light graphite-and-copper editorial typography with a schematic of context, inference, and human agency." />

**ARTIFICIAL INTELLIGENCE · HUMAN SYSTEMS · INFORMATION SCIENCE · ADAPTIVE COMPUTING**

</div>

**Website:** [nurowerx.com](https://nurowerx.com) · **Contact:** [swalker@nurowerx.com](mailto:swalker@nurowerx.com)

---

Founded in 2022 by Spencer H. Walker, Nurowerx is an independent Colorado-based research and technology company exploring the relationship between people, information, and intelligent systems. Our work connects human–computer interaction, explainable AI, intelligent infrastructure, and adaptive computation with a human-centered perspective.

### Areas of inquiry

**Human–AI Interaction & Explainability**  
Understanding how context, explanations, uncertainty, and intelligent interfaces influence human judgment, trust, and agency.

**AI Infrastructure & Adaptive Computing**  
Exploring model execution, local inference, resource-aware architectures, and the systems that make intelligent computation accessible.

**Perception & Autonomous Systems**  
Research directions in environmental interpretation, sensing, machine-assisted decisions, and meaningful human oversight.

**Information Science & Human Systems**  
Investigating how information is represented, interpreted, communicated, and acted upon across human and artificial systems.

### Featured research: Resident Model Lab

**[Resident Model Lab (RML)](https://github.com/Nurowerx/resident-model-lab)** is Nurowerx's experimental research program for **memory-bounded local inference** with existing mixture-of-experts models. Its latest **selection v2** cache keeps the original model router's expert choices intact while improving which weights reside in GPU memory.

**Latest tested result:** Compared with the previous 256-slot default, the new 128-slot configuration used **38.3% less peak GPU tensor memory** (2.42 vs. 3.92 GiB) at **11.4% higher mean response latency** (16.19 vs. 14.53 seconds). At a matched 128-slot capacity, the new cache policy was **6.3% faster** than the previous cache. An audit matched generated tokens across **128 requests**, full next-token logits were bitwise equal on three selected prompts, and **24 tests passed**.

**Scope:** This is a small, controlled OLMoE engineering study, **not** a claim of universal model compression, broad capability equivalence, or lower total system cost. The full expert store remains local, and raw results have not been independently audited here. Earlier approximate expert substitution degraded some answers; selection v2 instead preserves native routing.

**Explore:** [RML canonical project repository](https://github.com/Nurowerx/resident-model-lab) (**private; collaborators only**) · [Public RML research note, v0.2](./research/RESIDENT-MODEL-LAB.md) (**accessible without repository access**).

### Public technical work

This organization provides a deliberately limited public view of Nurowerx's research and engineering directions. Public repositories will be selected for clarity, reproducibility, and suitability for release.

Proprietary implementations, experimental systems, confidential engagements, and unpublished research remain private unless deliberately cleared for publication.

---

<sub>NUROWERX · Colorado, United States · [Official website](https://nurowerx.com) · Independent research and technical development</sub>
