<div align="center">

<img src="./assets/nurowerx-github-banner.svg" width="100%" alt="NUROWERX — THE NEXT FRONTIER IS HUMAN. Charcoal and warm-orange editorial banner with a schematic of context, inference, and human agency." />

**ARTIFICIAL INTELLIGENCE · HUMAN SYSTEMS · INFORMATION SCIENCE · ADAPTIVE COMPUTING**

</div>

---

Nurowerx is an independent research and technology corporation exploring the relationship between people, information, and intelligent systems. Our work connects human–computer interaction, explainable AI, intelligent infrastructure, and adaptive computation with a human-centered perspective.

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

**[Resident Model Lab](./research/RESIDENT-MODEL-LAB.md)** is a working local software research system investigating memory-bounded inference in an existing OLMoE mixture-of-experts model. It manages expert loading and GPU residency, with exact and adaptive execution modes and instrumentation for memory, transfers, latency, and answer correctness.

**What works:** In exact mode, generated tokens matched the reference implementation on tested requests. In an initial eight-task evaluation, exact execution and an ordinary quantization baseline each passed **5/8** tasks; tested 16-expert adaptive configurations passed **2/8**.

**What remains unresolved:** Reliable expert selection that preserves answer quality. These early results do not establish broad capability parity, speedups, measured hardware cost savings, or production readiness.

[Read the preliminary technical research note](./research/RESIDENT-MODEL-LAB.md) for methods, limitations and next experiments.

### Public technical work

This organization provides a deliberately limited public view of Nurowerx's research and engineering directions. Public repositories will be selected for clarity, reproducibility, and suitability for release.

Proprietary implementations, experimental systems, confidential engagements, and unpublished research remain private unless deliberately cleared for publication.

---

<sub>NUROWERX · Colorado, United States · Independent research and technical development</sub>
