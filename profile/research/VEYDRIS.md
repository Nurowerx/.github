# VEYDRIS

**Nurowerx | Computer vision and video analysis | Local prototype | November 2026**

## Overview

**VEYDRIS** is a locally running computer-vision research and development application for examining recorded video, detecting visible objects, tracking detections across frames, and reviewing annotated results. The project combines an analysis interface with video replay and structured exports.

### Capabilities reported in the initial local build

- Object detection and temporal tracking on video material.
- Video upload and replay with annotations.
- Export of analysis results.
- User authentication for the local application.
- A **clearly labeled synthetic map demonstration** illustrating possible spatial visualization workflows.
- **36 automated tests passed**, according to the developer's local build summary.

### Current technical and validation boundaries

These are **developer-reported build capabilities**, not results independently audited from the source or model archive. No detection precision, recall, tracking accuracy, real-time latency, field performance, or operational reliability has been independently verified in this public note.

**Do not confuse the synthetic map with verified locations.** The demonstration does not establish live location tracking, real GPS telemetry, or a working drone integration. **Live drone connections and real geolocation are future phases.** Docker/PostGIS configuration is included in the local project package but **has not been runtime-tested**.

Video analysis on uploaded material should not be represented as live airborne sensing, validated autonomous detection, geolocation, or operational deployment.

### Relationship to the Nurowerx Research Stack

The [Nurowerx Research Stack](./RESEARCH-STACK.md) could eventually support VEYDRIS provenance, evaluation, and inspection workflows, but **no VEYDRIS integration has been verified**. This prototype remains distinct from that research platform, and its synthetic map is not verified geolocation.

### Publication and access

The application runs on the developer's computer; it is **not an accessible public website**. The full code, model and sample archive have **not yet been uploaded to this GitHub organization**. Local authentication details are intentionally excluded from public documentation. The project is not offered here as a verified security or surveillance product.

### Release requirements

Before releasing the full implementation, review the archive for access credentials, video and sample-data rights, model licenses, privacy implications, telemetry handling, reproducibility requirements, and whether Docker/PostGIS actually runs. Publish tested installation and access controls only after audit.

**Status:** Local initial build reported; independent inspection and public source release pending.

**Related organization:** [Nurowerx](https://nurowerx.com) · [Technical Work](https://nurowerx.com/technical-work)
