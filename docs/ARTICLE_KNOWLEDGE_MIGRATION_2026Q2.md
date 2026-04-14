# MAOS-VISION Article Knowledge Migration (2026 Q2)

Purpose: Capture MAOS Vision System (MVS) concept and component decisions from aerocommons and turn them into repo-owned execution context.

Scope note: This is R&D guidance for Experimental Amateur-Built development. It is not a certification claim.

## Source Articles

- 2026-04-03-mvs-phase1-component-list.md
- 2026-04-12-xplane-as-design-validation-tool.md

## Imported Decisions and Working Baseline

- Phase 1 MVS baseline is a camera/display side-window replacement concept with retained forward direct-view windshield.
- Initial architecture uses multiple external cameras, conversion/multiplexing pipeline, and dual in-cockpit displays.
- Integration must prioritize low end-to-end latency, graceful degradation, and maintainable wiring/power design.

## Vision-System Guidance to Carry Into This Repo

- Treat multiplexer single-point failure as a first-class hazard and design bypass path.
- Treat EMI, vibration, and environmental robustness as core integration criteria.
- Maintain explicit test criteria for latency, readability, and failure behavior before flight use.

## Open Decisions Assigned to MAOS-VISION

- Finalize camera count, placement, and field-of-view overlap requirements.
- Select final display stack with sunlight readability and power compatibility constraints.
- Define bypass/fallback routing when one converter, camera, or multiplexer channel fails.
- Define pilot workload and human-factors acceptance criteria for camera-only side visibility.

## Immediate Work Items

1. Create docs/MVS_ARCHITECTURE_V1.md with signal chain and redundancy map.
2. Create docs/MVS_FAILURE_MODES_AND_FALLBACKS.md.
3. Create docs/MVS_LATENCY_AND_VISIBILITY_TEST_PLAN.md.
4. Create docs/MVS_INSTALLATION_AND_MAINTENANCE_CONSTRAINTS.md.

## Suggested Deliverables to Add Next

- docs/MVS_ARCHITECTURE_V1.md
- docs/MVS_FAILURE_MODES_AND_FALLBACKS.md
- docs/MVS_LATENCY_AND_VISIBILITY_TEST_PLAN.md
- docs/MVS_INSTALLATION_AND_MAINTENANCE_CONSTRAINTS.md
