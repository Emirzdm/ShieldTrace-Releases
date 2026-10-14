# ShieldTrace

**RF Measurement Analysis Platform**

A Windows desktop research application for RF measurement analysis,
S-parameter-based electromagnetic shielding evaluation, measurement traceability,
quality control and reproducible research workflows.

This repository is the public product showcase and release history for the
closed-source ShieldTrace application. Application source code remains private.

## Current Status

- **v0.2.0 — Evaluation Release**
- Under active development.
- Closed-source Windows desktop application.
- Windows installer and portable package are available for v0.2.0.
- Historical v0.1.0 Beta Windows binary remains available through
  [GitHub Releases](https://github.com/Emirzdm/ShieldTrace-Releases/releases/tag/v0.1.0-beta).

Windows binaries are available from the [v0.2.0 GitHub Release](https://github.com/Emirzdm/ShieldTrace-Releases/releases/tag/v0.2.0).
The release includes the installer, portable archive, SHA-256 checksums, and the corresponding-source package for the LGPL-covered Qt components.

See the [v0.2.0 release notes](RELEASE_NOTES_v0.2.0.md) for the current showcase scope.

## What ShieldTrace Does

### Measurement and research workflows

- Import Touchstone 1.x `.s2p` files and mapped CSV/TXT measurement data.
- Preserve complex S-parameters and native measured frequency points.
- Associate measurements with samples and record measurement provenance and traceability.
- Review measurement quality through a quality-control workflow.
- Inspect measured-data plots with a continuous cursor guide and values tied to actual measured points.
- Derive shielding metrics from imported measured S-parameters.
- Examine repeatability and organize experiment sets for comparison and trend analysis.
- Export PDF research reports and reproducible research export bundles.

Repeatability and trend analysis are descriptive research tools; they do not
establish measurement uncertainty or certified performance.

### Analytical good-conductor workflow

A separate analytical workflow evaluates absorption loss and skin depth under the
good-conductor approximation using material and frequency inputs. Its absorption
loss result is **not total shielding effectiveness**. This model-based workflow is
distinct from the measurement-derived S-parameter analysis described below.

### Desktop experience

- Turkish / English interface.
- Light / Dark / System themes.
- Offline desktop workflow.
- No telemetry or usage analytics.

## Scientific Scope

For the measurement-derived workflow, power fractions and shielding metrics are
calculated from imported complex S-parameter data:

```text
R = |S11|²
T = |S21|²
A = 1 - R - T

SET = -10 log10(T)
SER = -10 log10(1 - R)
SEA = SET - SER
```

R and T are dimensionless reflected and transmitted power fractions under the
measurement model's normalization assumptions. Raw A is an energy-balance
quantity; it is **not the same as SEA**, which is expressed in dB. SET, SER and
SEA use the base-10 power-ratio convention. Logarithmic results require valid
domains, including T > 0 and 1 - R > 0.

Analysis preserves measured frequency points. Measurement validity depends on
the measurement setup and source data; importing a file or passing software QC
does not establish calibration or experimental validity.

ShieldTrace does not claim MIL-STD-461 or MIL-STD-464 compliance, material
certification, calibrated-instrument status, accredited laboratory validation,
uncertainty analysis or certified accuracy. Real laboratory VNA validation
remains part of ongoing development.

## Research Workflow

Measurement import → provenance → QC → analysis → repeatability →
experiment comparison/trends → reports / research export

v0.2.0 focuses on keeping samples, measurements, analysis context and reports
connected, supporting traceability and reproducibility throughout research.
A research export bundle is not claimed to be independently rerunnable without
the original source measurement data. Preserve those data alongside the research
records and reports.

## Screenshots

See the [screenshot guidance](docs/screenshots/README.md) for recommended views
and capture requirements. No application screenshots are included yet.

## Release History

| Version | Status |
|---|---|
| **v0.2.0 — Evaluation Release** | Current version; Windows installer and portable package available. [Release notes](RELEASE_NOTES_v0.2.0.md). |
| **v0.1.0 Beta — Historical Windows binary release** | Still available through [GitHub Releases](https://github.com/Emirzdm/ShieldTrace-Releases/releases/tag/v0.1.0-beta). [Historical release notes](RELEASE_NOTES_v0.1.0.md). |

The historical v0.1.0 Beta binary has the analytical scope documented in its
release notes; it does not contain the v0.2.0 measurement and research workflows.

## AI-Assisted Development Disclosure

ShieldTrace uses AI-assisted development tools under Emir Özdemir's product
direction, requirements, testing criteria and release responsibility.
A substantial portion of implementation work has been assisted by AI coding tools.
Product and release decisions remain Emir Özdemir's responsibility; AI assistance
does not constitute autonomous authorship or autonomous scientific validation.

## License

ShieldTrace remains closed-source. The existing [LICENSE.txt](LICENSE.txt) and
[THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt) are retained unchanged with the
historical v0.1.0 binary material. This showcase does not change the license under
which that binary was distributed or grant access to the private application source.

© 2026 Emir Özdemir. All rights reserved.
