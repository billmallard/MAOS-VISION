# MAOS-VISION

Open-source external-vision and camera-driven window system development for MAOS aircraft concepts.

## Status

Concept and architecture phase.

## Safety Notice

This repository is for research and experimental development only. It is not approved for manned flight and must not be used as-is in safety-critical operation without formal system safety assessment, verification, validation, and regulatory compliance.

This project targets the Experimental Amateur-Built category. FAA certification is not a current design constraint, but engineering decisions should still follow conservative aerospace and safety-critical best practices where practical.

## Role in MAOS Multi-Project Architecture

This repository owns the MAOS external-vision domain.

- Camera-driven outside-visibility architecture and display concepts.
- Sensor, compute, and display pipeline requirements.
- Vision subsystem software, integration rules, and verification artifacts.

Related repositories:

- MAOS-DESIGN owns aircraft-level geometry, packaging, and integration constraints.
- MAOS-FCS owns flight-control computation and flight-critical control paths.
- MAOS-ECS owns environmental control and pressurization subsystem development.
- aerocommons is the website and program-level communications hub.

## Mission

Develop a practical camera-driven visibility system that improves operational awareness while preserving deterministic behavior, graceful degradation, and builder-realistic implementation pathways.

## Scope

In scope:

- External camera architecture and placement trade studies.
- Display and human-interface concepts for outside-scene presentation.
- Video transport, synchronization, and latency budgeting.
- Degraded-mode behavior for sensor, link, or display failures.
- Vision subsystem software/firmware tooling and verification harnesses.

Out of scope:

- Primary flight-control laws and actuator command authority (owned by MAOS-FCS).
- Airframe geometry governance and top-level configuration control (owned by MAOS-DESIGN).

## Interface-First Rules

Before detailed implementation, freeze and version:

- Sensor interfaces: frame rates, resolutions, dynamic range assumptions.
- Transport interfaces: protocol, bandwidth allocation, timestamping, and loss behavior.
- Display interfaces: update rates, rendering constraints, symbology ownership boundaries.
- Fault semantics: stale-frame handling, sensor dropout flags, fallback display behavior.
- Timing budgets: sensor-to-display end-to-end latency and jitter limits.

Starter template: `INTERFACE_CONTROL_DOCUMENT_TEMPLATE.md`

## Suggested Repository Layout

- docs  Architecture, requirements, and verification plans
- firmware  Embedded or edge-device software
- libs  Shared codecs, transport, and processing libraries
- sim  Playback and scene simulation tools
- tests  Unit, integration, and scenario test suites
- tools  Analysis, calibration, and log-processing utilities
- configs  Camera/display profiles and deployment presets
- data  Calibration, sample captures, and reference datasets

## Verification Strategy

- Requirements-to-test traceability for vision-critical behaviors.
- Deterministic timing and latency budget validation.
- Sensor fault injection and degraded-mode validation.
- Human-factors-oriented test scenarios for visibility and workload.
- Regression evidence for every interface-impacting change.

## Current Milestones (As of 2026-04-14)

Current repository maturity is bootstrap-level.

Near-term milestones:

1. Establish baseline repo structure (`docs`, `firmware`, `libs`, `sim`, `tests`, `tools`, `configs`, `data`).
2. Publish top-level vision subsystem requirements and failure-mode assumptions.
3. Draft first ICD covering camera ingest, transport timing, and display output contracts.
4. Stand up a minimal playback pipeline for latency and dropout experiments.
5. Define first scenario-based verification matrix for degraded visibility modes.

## Knowledge Migration

- Article-derived subsystem migration notes: `docs/ARTICLE_KNOWLEDGE_MIGRATION_2026Q2.md`

## Licensing

This repository uses a dual-license model:

- Source code: PolyForm Noncommercial 1.0.0 (`LICENSE-CODE`)
- Documentation and non-code design content: CC BY-NC-SA 4.0 (`LICENSE-DOCS`)

Commercial use is not granted by default. For commercial licensing, contact `contact@aerocommons.org`.

Contribution and file classification guidance: `CONTRIBUTING.md`

## Program Context

MAOS is an open-source experimental aircraft development effort. The aircraft has not yet flown. All design and performance values are targets subject to revision as analysis and testing mature.
