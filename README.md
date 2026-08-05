# ShieldTrace

**Official binary releases for ShieldTrace**

ShieldTrace is a Windows desktop application for frequency-sweep analysis of absorption loss and skin depth using the good conductor approximation.

## AI-Assisted Development Disclosure

ShieldTrace was created using AI-assisted development tools under the product direction, requirements, testing criteria, and validation of Emir Özdemir. A substantial portion of the code was generated and developed with the assistance of AI coding tools. Product scope, decisions, testing, validation, and release responsibility belong to Emir Özdemir.

## Features

- Absorption Loss frequency-sweep chart
- Skin Depth frequency-sweep chart
- Built-in material presets and custom materials
- Deterministic analysis report
- PDF report export
- Turkish and English interface
- Dark and light themes
- Windows x64 desktop package

## Installation

1. Download the Windows x64 ZIP file from the Releases page.
2. Extract the entire ZIP archive.
3. Open the extracted folder.
4. Run `ShieldTrace.exe`.

Do not move `ShieldTrace.exe` away from the `_internal` folder. To place it on the desktop, create a shortcut instead of copying the EXE alone.

## Model Scope and Limitations

ShieldTrace v0.1.0 Beta calculates the absorption component under the good conductor approximation.

It does not calculate:

- Reflection loss
- Multiple-reflection effects
- Total shielding effectiveness
- Apertures, joints, surface roughness or real geometry
- Multilayer shielding structures

The results must not be interpreted as total shielding effectiveness or as a replacement for professional simulation, measurement or certification.

## License

ShieldTrace is free to evaluate but is not open-source software. Commercial use, redistribution, resale, modification and repackaging require prior written permission from Emir Özdemir.

See `LICENSE.txt` and `THIRD_PARTY_NOTICES.txt`.

© 2026 Emir Özdemir. All rights reserved.
