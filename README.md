# Mordred Studio 1.0.0

Mordred Studio is a standalone Windows interface for calculating molecular
descriptors with Mordred and RDKit. Import molecules, calculate 2D or 3D
descriptors, inspect results, and export CSV files through a desktop GUI.

## Download

**[Download Mordred Studio for Windows](https://github.com/rayx1/Mordred-Studio/releases/)**

Download `Mordred-Studio-1.0.0-windows-x64.zip`, extract it, verify
`Mordred-Studio.exe` against `SHA256SUMS.txt`, and run it on 64-bit Windows.

The executable contains the Windows application, Python/Tk runtime,
Mordred 1.2.0, RDKit, application license, and third-party license notices.
Python installation and a separate backend setup are not required.
Calculations run locally; molecular data is not uploaded.

## Key functions

- Editable SMILES input and SMILES/TXT, CSV, TSV, SDF, and MOL import
- 1,613 2D descriptors; 1,826 total with 3D descriptors enabled
- All descriptor families or one selected family
- Background calculation with progress and cancellation between molecules
- Searchable result columns and complete CSV export
- Invalid-input flags and descriptor issue reports
- Help, About, scientific citation, and license information
- Custom molecular icon and themed startup splash screen

The result table previews up to 80 matching descriptor columns and 500 rows.
CSV export includes all calculated rows and descriptor columns. 3D calculations
require supplied 3D coordinates in SDF/MOL files; conformers are not generated
automatically.

## Attribution and relationship

Windows application contribution: **Rashmiranjan Behera**
([rbehera.in](https://rbehera.in)).

Upstream descriptor calculator:
[Mordred](https://github.com/mordred-descriptor/mordred), release 1.2.0,
BSD 3-Clause. Molecular structure handling is provided by
[RDKit](https://www.rdkit.org/).

Mordred Studio is an independent interface; it is not an official Mordred
release and is not affiliated with or endorsed by the Mordred project.

Scientific reference: Moriwaki H, Tian Y-S, Kawashita N, Takagi T (2018).
*Mordred: a molecular descriptor calculator.* Journal of Cheminformatics 10:4.
[doi:10.1186/s13321-018-0258-y](https://doi.org/10.1186/s13321-018-0258-y).

## License

Mordred Studio application code and original assets are licensed under the
MIT License. See [LICENSE](LICENSE). Bundled components retain their respective
licenses; see [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt).

The notices are also available inside the application under
**Help → Licenses and acknowledgments**.

## Download Mordred Studio

The Windows binary is provided through GitHub Releases:
[Mordred Studio releases](https://github.com/rayx1/Mordred-Studio/releases/).

### Quick download

For version 1.0.0, select `Mordred-Studio-1.0.0-windows-x64.zip` from the
release assets. The ZIP includes the executable, documentation, licenses,
and `SHA256SUMS.txt`.

Visit the [GitHub release page](https://github.com/rayx1/Mordred-Studio/releases/) for the available binary, source,
and checksum assets.

> **Requirements:** 64-bit Windows. No Python installation is required.
> The portable executable extracts its bundled runtime to a temporary folder
> at startup; the first launch can take longer.
>
> **Windows security notice:** The current executable is not digitally signed,
> so Windows SmartScreen may display a warning on first launch. Verify the
> download source and executable checksum before running it.

To verify the extracted executable in PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 .\Mordred-Studio.exe
```

Expected SHA-256 for the **version 1.0.0 executable**:

```text
D546E29EF64CB362CB7C6B36B76F640836772CB31F39E838A508DFF85D6B87AC
```

This checksum applies to `Mordred-Studio.exe`, not the ZIP archive.

Mordred Studio is an independent Windows application developed by
[Rashmiranjan Behera](https://rbehera.in), powered by the upstream
[Mordred](https://github.com/mordred-descriptor/mordred) project.
