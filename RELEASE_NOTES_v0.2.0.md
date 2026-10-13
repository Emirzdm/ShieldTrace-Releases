# ShieldTrace v0.2.0 — Evaluation Release

- **Release date:** 14 October 2026
- **Release type:** Public product/showcase release
- **Platform:** Windows desktop
- **Development status:** Under active development
- **Source code:** Private / closed-source

This release presents the v0.2.0 product and research workflow scope.
v0.2.0 binary distribution is temporarily unavailable.

## Highlights

- Touchstone 1.x `.s2p` and mapped CSV/TXT measurement import.
- Complex S-parameter preservation and native measured frequency-point handling.
- Measurement/sample association, provenance and traceability.
- Measurement quality-control workflow and continuous measured-data plot inspection.
- Shielding metrics derived from imported measured S-parameters.
- Descriptive repeatability analysis, experiment sets and experiment comparison/trends.
- PDF research/report export and reproducible research export bundles.
- Turkish / English interface and Light / Dark / System themes.
- Offline desktop workflow with no telemetry or usage analytics.

The analytical absorption-loss and skin-depth workflow under the good-conductor
approximation remains separate from measurement-derived S-parameter analysis.
Its absorption-loss result is not total shielding effectiveness.

## Research Workflow

Measurement import → provenance → QC → analysis → repeatability →
experiment comparison/trends → reports / research export

The focus is traceability and reproducibility across the research process.
Exported bundles are not claimed to be independently rerunnable without the
original source measurement data.

## Scientific Limitations

- Calculations use imported measured data and preserve measured frequency points.
- Raw A = 1 - R - T is an energy-balance quantity, not the dB quantity SEA.
- Measurement validity depends on the measurement setup and source data.
  Software QC does not establish instrument calibration or experimental validity.
- Repeatability and trends are descriptive, not uncertainty analysis.
- No MIL-STD-461 or MIL-STD-464 compliance, material certification,
  calibrated-instrument status, accredited laboratory validation or certified
  accuracy is claimed.
- Real laboratory VNA validation remains part of ongoing development.

See the [README scientific scope](README.md#scientific-scope) for the
measurement-derived equations and their distinction from the analytical model.

## Distribution Status

Binary distribution for v0.2.0 is temporarily unavailable while third-party
redistribution requirements are being finalized.

No v0.2.0 executable, installer, portable archive or runtime libraries are
distributed with this showcase. Source code remains private.

The historical v0.1.0 Beta Windows binary remains available through
[GitHub Releases](https://github.com/Emirzdm/ShieldTrace-Releases/releases/tag/v0.1.0-beta).
It retains its original scope, files and license; it does not provide the v0.2.0
measurement and research functionality.

The existing LICENSE.txt and THIRD_PARTY_NOTICES.txt remain unchanged.
This showcase does not migrate the historical binary's license.

## AI-Assisted Development Disclosure

ShieldTrace uses AI-assisted development tools under Emir Özdemir's product
direction, requirements, testing criteria and release responsibility.
A substantial portion of implementation work has been assisted by AI coding tools.
AI assistance does not constitute autonomous authorship or scientific validation.
