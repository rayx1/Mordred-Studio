# Mordred Studio 1.0.0

Windows desktop GUI developed by Rashmiranjan Behera (https://rbehera.in), powered by the original Mordred 1.2.0 engine and RDKit. This is an independent interface, not an official Mordred release.

## Run
Open `dist/Mordred-Studio.exe`. Python installation is not required. Windows x64. The portable executable includes its dependencies and extracts them to a temporary directory on launch. It is not digitally signed.

## Features
- Custom molecular icon and branded startup splash.
- Editable SMILES input and SMILES/TXT, CSV, TSV, SDF and MOL import.
- 1,613 2D descriptors; 1,826 total with 3D enabled.
- All descriptor families or one selected family.
- Background calculation, progress and cancellation between molecules.
- Searchable result-column preview (80 descriptors, 500 rows); full CSV export.
- Invalid molecule rows preserved. Missing descriptors remain blank, with reasons in the Issues tab and companion issues CSV.
- About, author website, upstream source, scientific citation, licenses and quick guide.

CSV/TSV requires a `SMILES` column. `name` or `id` is optional. Plain text uses one SMILES string per line followed by an optional name. To return from file mode to editable text, use Load example / edit SMILES.

3D mode requires supplied 3D conformers in SDF/MOL. Coordinates are not generated automatically. Descriptor availability depends on molecule structure; a partial status does not mean all values failed. Cancellation exports completed rows only. Data stays on this computer.

## Build from source
Use Python 3.11 on Windows x64 and run `./build_windows.ps1` in PowerShell. Dependencies are pinned in requirements.txt. The original Mordred package is unmodified. A compatibility adapter restores NetworkX biconnected_component_subgraphs using biconnected_components and copied subgraphs; older NumPy and NetworkX versions preserve its compatibility. The build script prepares the icon and license notices, runs the engine tests and produces a single-file executable.

## Validation
`test_engine.py` checks known molecular values, direct upstream parity, descriptor counts, invalid SMILES, cancellation, 3D SDF and CSV round-tripping. `test_gui.py` exercises the splash, calculation button, result table, About, licenses and guide. The packaged executable supports `--self-test OUTPUT.json` for a dependency and calculation smoke test.

## Licensing and citation
GUI and custom branding: MIT, copyright 2026 Rashmiranjan Behera.
Mordred: BSD-3-Clause. Full runtime dependency notices are bundled in THIRD_PARTY_NOTICES.txt and available inside Help > Licenses.
Upstream: https://github.com/mordred-descriptor/mordred
Moriwaki H, Tian Y-S, Kawashita N, Takagi T (2018). Mordred: a molecular descriptor calculator. Journal of Cheminformatics 10:4. https://doi.org/10.1186/s13321-018-0258-y

Results are held in memory; very large inputs and graph-intensive descriptors may require substantial time and memory. The GUI is tested on the build computer; testing on a separate clean Windows machine is recommended before public distribution.
